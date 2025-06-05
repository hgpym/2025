pipeline {
    agent any
    stages {
        stage('Disk Usage') {
            steps {
                echo " Диски:"
                sh 'df -h'
            }
        }
        stage('Top Memory Process') {
            steps {
                echo " Топовый процесс по памяти:"
                sh '''
                ps -eo pid,comm,%mem --sort=-%mem | head -n 2
                '''
            }
        }
    }
}