pipeline {
    agent any

    stages {
      stage('Pull from GitHub') {
            steps {
                git branch: 'main', url: 'githubreponame'
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
