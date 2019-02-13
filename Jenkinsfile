pipeline {
    agent any

    stages {
        stage('Build'){
          steps {
            sh 'mvn clean package'
          }
          post {
           success {
             echo 'Now Archicing'
             archiveArtifacts artifacts: '**/target/*.war'
           }
          }

        }



    }
}
