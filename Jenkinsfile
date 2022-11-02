pipeline {
    agent any

    stages {
        stage('AWS STS') {
            steps {
                echo 'AWS STS'
                sh 'aws sts get-caller-identity'
            }
        }
        stage('AWS s3 list') {
            steps {
                echo 'AWS STS'
                sh 'aws s3 ls'
            }
        }
        stage('GIT git clone') {
            steps {
                echo 'Git clone'
                sh 'rm -rf jenkins-bootcamp'
                sh 'git clone https://github.com/cbarragan995/jenkins-bootcamp.git'
            }
        }
        stage('Upload to s3') {
            steps {
                sh 'aws s3 cp jenkins-bootcamp s3://jenkins-bucket-bootcamp --recursive'
            }
        }
    }
}
