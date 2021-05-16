pipeline{
  
  
  environment{
    JAVA_TOOL_OPTIONS="-student.home=/var/maven"
  }
  agent{
    dockerfile{
      //image "maven:3.8.1-jdk-11"
      label "docker"
      args "-v /tmp/maven:/var/jenkins/.m2 -e MAVEN_CONFIG=/var/jenkins/.m2"
    }
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
