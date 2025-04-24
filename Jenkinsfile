
 		pipeline {
    agent any

    stages {
        stage('Checkout') {
            steps {
                git 'https://github.com/im-faix/Quality-Check-Project.git'
            }
        }

        stage('Run Shell Check Script') {
            steps {
                sh 'chmod +x check.sh'
                sh './check.sh'
            }
        }
    }

    post {
        success {
            echo '✅ Pipeline completed successfully.'
        }
        failure {
            echo '❌ Pipeline failed.'
        }
    }
}

