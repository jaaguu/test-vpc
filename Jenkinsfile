pipeline{
    agent any
stages{
    stage('Git checkout'){
        steps{
            git branch: 'main', credentialsId: 'github', url: 'https://github.com/jaaguu/Terraform_AWS_VPC.git'
        }
    }
    stage('Terraform Init'){
        steps{
            sh '''terraform init'''
        }
    }
    stage('Terraform Plan'){
        steps{
            sh '''terraform plan'''
        }
    }
    stage('Terraform Apply'){
        steps{
            sh '''terraform destroy -auto-approve'''
        }
    }
}
}
