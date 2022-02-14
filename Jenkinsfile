pipeline {
  agent any
  stages {
    stage('Build') {
      steps {
           echo "build success"
      }
    }
    stage('Test') {
      steps {
          echo "mvn test starts"
      }
    }
    stage('Deploy Development') {
      steps {
            bat "mvn clean package deploy -DmuleVersion=4.4.0 -Dusername=sumedha_Jan -Dpassword=Lambda=mc2  -DapplicationName=bms-process-api -Denvironment=dev -Dworkers=1 -DworkerType=Micro -Danypoint.platform.client_id=f285ab05d02b4f37b1409bfcffdcdecc   -Danypoint.platform.client_secret=ED20687772D14485b0a781b6b36897a8 -DmuleDeploy"
            echo "deploy success"
      }
    }
  }
}