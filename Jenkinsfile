pipeline{

  agent any
    environment { 
        registry = "coreofatom/spring-boot-docker" 
        registryCredential = 'coreofatom' 
        dockerImage = '' 
    }
    stages {
          
        stage ('Testing ') {
            steps {
                script{
                  if (isUnix()){
                    sh 'mvnw test'
                               }
                  else{
                        bat '.\\mvnw test'
                      }
                      }
                  }
                            }
            post {
                    always {
                        junit '**/target/surefire-reports/TEST-*.xml'
                            }
                  }
    }
    
        
