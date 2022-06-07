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
        stage('Test') {
            steps {
       publishHTML (target: [
      allowMissing: false,
      alwaysLinkToLastBuild: false,
      keepAll: true,
      reportDir: 'coverage',
      reportFiles: 'index.html',
      reportName: "RCov Report"
    ])

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

