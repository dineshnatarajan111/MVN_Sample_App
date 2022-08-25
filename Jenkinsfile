pipeline{
  agent any
  triggers {
    cron('H/10 * * * * *')
  }
  stages{
    stage("build"){
      input {
        message "Should we continue?"
        ok "Yes, we should."
        submitter "alice,bob"
        parameters {
            string(name: 'PERSON', defaultValue: 'Mr Jenkins', description: 'Who should I say hello to?')
        }
      }
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
