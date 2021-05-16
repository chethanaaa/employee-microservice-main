pipeline{
  
  
  environment{
    JAVA_TOOL_OPTIONS="-Duser.home=/var/maven"
  }
  agent{
    docker{
      image "maven:3.8.1-jdk-11"
      label "docker"
      args "-v /tmp/maven:/var/maven/.m2 -e MAVEN_CONFIG=/var/maven/.m2"
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
