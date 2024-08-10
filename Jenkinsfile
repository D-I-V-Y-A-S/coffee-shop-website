pipeline {
  agent any
  stages {
    stage('Terraform Init') {
      steps {
        script {
          echo 'Initializing Terraform...'
          sh 'terraform init'
          echo 'Terraform initialization complete.'
        }
      }
    }
    stage('Terraform Plan') {
      steps {
        script {
          echo 'Planning Terraform changes...'
          sh 'terraform plan'
          echo 'Terraform plan complete.'
        }
      }
    }
    stage('Terraform Apply') {
      steps {
        script {
          echo 'Applying Terraform changes...'
          sh 'terraform apply -auto-approve'
          echo 'Terraform apply complete.'
        }
      }
    }
    stage('Verify IIS') {
      steps {
        script {
          echo 'Verifying IIS installation...'
          def result = sh(script: 'powershell -Command "Get-Service -Name W3SVC"', returnStatus: true)
          if (result != 0) {
            echo 'IIS Service is not running.'
            error('IIS Service verification failed.')
          } else {
            echo 'IIS Service is running.'
          }
        }
      }
    }
  }
}
