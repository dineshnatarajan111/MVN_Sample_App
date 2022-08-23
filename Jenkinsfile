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
  }
}
