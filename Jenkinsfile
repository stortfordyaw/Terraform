pipeline {
  agent none
  stages {
    stage('Pull Code') {
      steps {
        git(url: 'https://github.com/stortfordyaw/Terraform', credentialsId: '30c2da097a7d8d5ba4407b2a49d395e0fadbcb48', branch: 'paas', changelog: true, poll: true)
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