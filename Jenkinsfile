pipeline {
    agent any

    stages {
        stage('Checkout') {
            steps {
                echo 'ShopSphere source code checked out successfully'
            }
        }

        stage('Verify Project') {
            steps {
                sh 'echo "Verifying ShopSphere project..."'
                sh 'find . -maxdepth 2 -name pom.xml'
            }
        }
    }

    post {
        success {
            echo 'ShopSphere pipeline completed successfully!'
        }

        failure {
            echo 'ShopSphere pipeline failed.'
        }
    }
}
