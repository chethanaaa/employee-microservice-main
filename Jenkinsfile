pipeline {
    agent any
    environment{
    
    }
    stages {
        stage('Test') { 
            steps {
                echo 'building the application......'
                sh 'mvn --version'
                sh 'mvn clean install'
            }
        }
    }
}
