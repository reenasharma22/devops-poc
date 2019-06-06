pipeline {
  agent any
  stages { 
 stage('build') {
      steps {
       bat 'mvn clean test'
      }
    }  
    stage('Deploy CloudHub') {
      steps {
        bat 'mvn deploy -DmuleDeploy -Dcloud.env=Sandbox -Danypoint.businessGroup=public -Dcloudhub.workerType=Small -DcloudhubAppName=firstapplication4 -Dmule.version=4.1.5 -Dcloud.user=reena220786 -Dcloud.password=Sharma22@'
      }
    }
  }
}