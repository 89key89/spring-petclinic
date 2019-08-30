node {
   stage('Preparation') {
      git 'https://github.com/89key89/spring-petclinic.git'
   }
   stage('Build') {
        sh './mvnw clean verify'
   }
   stage('Results') {
      junit '**/target/surefire-reports/TEST-*.xml'
      archiveArtifacts 'target/*.jar'
      echo 'OMFG IT IS WORKING'
   }
}
