pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
                script{
                sh 'rm -rf /var/www/html/*'
 
                sh 'scp -r /var/lib/jenkins/workspace/test_main/* /var/www/html/'
                sh 'scp -r /var/lib/jenkins/workspace/test_main/* jenkins@54.183.152.123:/var/www/html/'
                
                }
            }
        }
        stage('Test') {
            steps {
                echo 'Success'
            }
        }
        stage('Deploy') {
            steps {
                echo 'Successfull'
            }
        }
    }
}

