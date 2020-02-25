pipeline {
  agent any
  stages {
    stage("run prowler") {
      steps {
    //Use Jenkins UsernamePassword credentials information (Username: AccessKeyId, Password: SecretAccessKey):    
withAWS(credentials:AWS_CREDENTIALS) {
sh "cd prowler"
sh "./prowler"

     }
    }
  }  
 }
}
