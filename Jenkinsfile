pipeline {
    agent any
    stages {
        stage('run_prowler') {
            steps {
                withAWS(credentials: 'AWS_CREDENTIALS', region: 'us-east-1') {
                    //sh './prowler -M mono | aws s3 cp - s3://bucket-name-here/prowler-report.txt'
                    sh './prowler -M mono > prowler-report.txt'
                    
                }
            }
        }
    }
}
