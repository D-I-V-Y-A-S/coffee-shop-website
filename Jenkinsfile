pipeline {
  agent any
  stages {
    stage('Terraform Init') {
      steps {
        script {
          sh 'terraform init'
        }
      }
    }
    stage('Terraform Plan') {
      steps {
        script {
          sh 'terraform plan'
        }
      }
    }
    stage('Terraform Apply') {
      steps {
        script {
          sh 'terraform apply -auto-approve'
        }
      }
    }
   stage('Verify IIS') {
  steps {
    script {
      def result = sh(script: 'powershell -Command "Get-Service -Name W3SVC"', returnStatus: true)
      if (result != 0) {
        error('IIS Service is not running')
      }
    }
  }
} 
  }
}
