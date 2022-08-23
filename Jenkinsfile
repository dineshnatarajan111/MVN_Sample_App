pipeline{
  agent any
  stages{
    stage("build"){
      steps{
        bat "mvn package"
      }
    }
    stage("test"){
      steps{
        echo "testing stage"
      }
    }
    stage("deploy"){
      steps{
        deploy adapters: [tomcat8(credentialsId: '81c6cf5b-fed9-4567-a185-4a93e68778bd', path: '', url: 'http://localhost:8081')], contextPath: 'MVN_Web_App', war: '**/*.war'
      }
    }
  }
}
