pipeline{
  agent any
  stages{
    stage("build"){
      steps{
        mvn clean
      }
    }
    stage("test"){
      steps{
        echo "testing stage"
      }
    }
  }
}
