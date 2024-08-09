pipeline {
    agent any
    stages {
      stage('Build') {
            steps {
                echo 'hello'
            }
      }
   
    post {
        success {
            echo 'Completed Successfully!'
        }
        failure {
            echo 'Deployment failed!'
        }
    }
}
}
