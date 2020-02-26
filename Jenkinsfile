pipeline {
    agent any
    stages {
        stage('run_prowler') {
            steps {
                withAWS(credentials: 'AWS_CREDENTIALS', region: 'us-east-1') {
                    sh './prowler -c check722 -M mono | aws s3 cp - s3://collabralink-jenkins-test1-state-bucket/prowler-report.txt'
                    
                }
            }
        }
    }
}
