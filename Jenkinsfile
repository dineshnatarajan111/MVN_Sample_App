pipeline{
  agent any
  stages{
    stage("build"){
      steps{
        sh '''
            mvn clean
            mvn package
        '''
      }
    }
    stage("test"){
      steps{
        echo "testing stage"
      }
    }
  }
}
