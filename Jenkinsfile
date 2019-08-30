node {
   stage('Preparation') {
      git 'https://github.com/jglick/simple-maven-project-with-tests.git'
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
