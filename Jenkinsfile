node(){

   stage("Git Checkout"){
   //checkout([$class: 'GitSCM', branches: [[name: '*/main']], extensions: [], userRemoteConfigs: [[credentialsId: 'repo3git', url: 'https://github.com/muraliphani/rentalcarsv1.git']]])//
   checkout([$class: 'GitSCM', branches: [[name: '*/master']], extensions: [], userRemoteConfigs: [[credentialsId: 'repo4git', url: 'https://github.com/MOHAN-999/rentalcarsv1.git']]]) 
   }
   
   stage("Maven Build"){
   sh "mvn package"
   } 
   stage("sonarqube"){
      scannerHome = tool 'SonarQubeScanner'
      withSonarQubeEnv('sonarqube') {
         sh "${scannerHome}/bin/sonar-scanner"
      }
   }    
   //stage("Upload to nexus"){
   //nexusArtifactUploader artifacts: [[artifactId: '$BUILD_ID', classifier: '', file: 'target/RentalCars.war', type: 'war']], 
   //credentialsId: 'nexusrepologin', groupId: 'prod', nexusUrl: '3.238.253.14:8081', nexusVersion: 'nexus3', protocol: 'http', repository: 'repo6test', version: '$BUILD_ID'
  
  //}
}
