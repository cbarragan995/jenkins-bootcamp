pipeline {
    agent any

    stages {
        stage('Listar Buckets') {
            steps {
                echo 'Tenemos los siguientes Buckets: '
                sh 'aws s3 ls'
            }
        }
    }
}
