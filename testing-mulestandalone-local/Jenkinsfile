pipeline {
  agent any
  stages { 
 stage('build') {
      steps {
       bat 'mvn clean install'
      }
    }  
    stage('Deploy CloudHub') {
      steps {
        bat 'mvn deploy -DmuleDeploy -Dcloud.env=Sandbox -Danypoint.businessGroup=PublicBiz -Dcloudhub.workerType=Small -DcloudhubAppName=testing-mulestandalone-local -Dmule.version=4.1.5 -Dcloud.user=reena220786 -Dcloud.password=Sharma22@'
      }
    }
  }
}