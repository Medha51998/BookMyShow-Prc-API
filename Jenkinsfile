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
            bat "mvn clean package deploy -DmuleVersion=4.4.0 -Dusername=sumedha_Jan -Dpassword=Lambda=mc2  -DapplicationName=bms-process-api -Denvironment=Sandbox -Dworkers=1 -DworkerType=Micro -Danypoint.platform.client_id=8394fb286e66430fb781885d87be8992   -Danypoint.platform.client_secret=dE9bcac36d38479fB99C650BC3Db8591 -DmuleDeploy"
            echo "deploy success"
      }
    }
  }
}