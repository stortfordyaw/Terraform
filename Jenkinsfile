pipeline {
  agent none
  stages {
    stage('Pull Code') {
      steps {
        git(url: 'https://github.com/stortfordyaw/PaaS', credentialsId: ' ')
      }
    }

    stage('Terraform init') {
      steps {
        sh '''Terraform init
Terraform apply'''
      }
    }

  }
  environment {
    Azure = 'kubernetes/main.tf'
  }
}