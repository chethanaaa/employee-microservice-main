pipeline{
  agent any
  tools{
    maven "3.6.0"
  }
  stages{
    stage("build"){
      steps{
        echo 'building the application......'
        sh "mvn -version"
        sh "mvn clean install"
      }
    }
    stage("test"){
      steps{
        echo 'testing the application........'
      }
    }
    stage("deploy"){
      steps{
        echo 'deploying the application......'
      }
    }
  }
  post{
    always{
    cleanWs()
    }
  }
}
