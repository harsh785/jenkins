pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
                script{
                sh 'rm -rf /var/www/html/*'
 
                sh 'scp -r /var/lib/jenkins/workspace/test_main/* /var/www/html/'
                sh 'scp -r /var/lib/jenkins/workspace/test_main/* jenkins@54.177.60.31:/var/www/html/'
                
                }
            }
        }
        stage{
            ('Test') {
            steps {
                echo 'Testing..'

}
            }
        }
        stage('Deploy') {
            steps {
                echo 'Successfull'
            }
        }
    }
}

