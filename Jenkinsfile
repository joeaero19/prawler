/*pipeline {
  agent any
  stages {
    stage("run prowler") {
      steps {
    //Use Jenkins UsernamePassword credentials information (Username: AccessKeyId, Password: SecretAccessKey):    
withAWS(credentials:AWS_CREDENTIALS) {
sh "./prowler"

     }
    }
  }  
 }
}
*/

pipeline {
    agent any
    stages {
        stage('run_prowler') {
            steps {
                withAWS(credentials: 'AWS_CREDENTIALS', region: 'us-east-1') {
                    sh './prowler'
                    
                }
            }
        }
    }
}
