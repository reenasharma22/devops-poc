pipeline {
  agent any
  stages {
    stage('Unit') {
      steps {
       bat 'mvn clean test'
      }
    }    
    stage('Deploy CloudHub') {
      steps {
        bat 'mvn deploy -DmuleDeploy -Dcloud.env=Sandbox -Danypoint.businessGroup=PublicBiz -Dcloudhub.workerType=Small -DcloudhubAppName=testing-mulestandalone-local -Dmule.version=4.1.5 -Dcloud.user=reena220786 -Dcloud.password=Sharma22@'
      }
    }
  }
}