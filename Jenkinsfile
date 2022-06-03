pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
                script{
                sh 'rm -rf /var/www/html/*'
 
                sh 'scp -r /var/lib/jenkins/workspace/test_main/* /var/www/html/'    
                
                }
            }
        }
        stage('Test') {
            steps {
                echo 'Testing..'
            }
        }
        stage('Deploy') {
            steps {
                echo 'Deploying....'
            }
        }
    }
}

