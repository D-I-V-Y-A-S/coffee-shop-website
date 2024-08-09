pipeline {
    agent any
    stages {
      stage('Hello') {
            steps {
                echo 'hello'
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
}
