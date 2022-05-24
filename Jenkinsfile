pipeline {
    agent any

    stages {
        stage('Git clone') {
            steps {
                git branch: 'main', url: 'https://github.com/svdevops07/cert_proj.git'
            }
        }

        stage('Copy file with variables') {
            steps {
                sh 'cp /home/ann/proj/variables.tf /var/lib/jenkins/workspace/proj_pipeline_main/'
            }
        }

        stage('Terraform init') {
            steps {
                sh "cat /root/.terraformrc"
                sh "/bin/terraform init"
//                sh 'terraform init'
            }
        }

        stage('Terraform Action') {
            steps {
//                echo "Terraform action is ---> ${action}"
//                sh 'terraform ${action} --auto-approve'
                sh 'terraform apply'
            }
        }
    }
}