node(){

   stage("Git Checkout"){
   //checkout([$class: 'GitSCM', branches: [[name: '*/main']], extensions: [], userRemoteConfigs: [[credentialsId: 'repo3git', url: 'https://github.com/muraliphani/rentalcarsv1.git']]])//
   checkout([$class: 'GitSCM', branches: [[name: '*/master']], extensions: [], userRemoteConfigs: [[credentialsId: 'repo4git', url: 'https://github.com/MOHAN-999/rentalcarsv1.git']]]) 
   }
   
   stage("Maven Build"){
   sh "mvn package"
   } 
  // stage("Upload to nexus"){
   //nexusArtifactUploader artifacts: [[artifactId: '$BUILD_ID', classifier: '', file: 'target/RentalCars.war', type: 'war']], 
   //credentialsId: 'nexusrepologin', groupId: 'prod', nexusUrl: '35.174.204.118:8081', nexusVersion: 'nexus3', protocol: 'http', repository: 'devtest1', version: '$BUILD_ID'
  
 // }
}
