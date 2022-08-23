pipeline{
  agent any
  stages{
    stage("build"){
      steps{
        mvn cleanmvn package
      }
    }
    stage("test"){
      steps{
        echo "testing stage"
      }
    }
  }
}
