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
        bat 'mvn deploy -P cloudhub -Dmule.version=4.1.5 -Danypoint.username=reena220786 -Danypoint.password=Sharma22@'
      }
    }
  }
}
