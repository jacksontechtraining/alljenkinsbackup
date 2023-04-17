pipeline{
    agent any

    stages{
        stage('check java version'){
            step{
                echo 'checking the java version'
                bat 'java --version'    
            }
                    
        }
        stage('checkout from git'){
            step{
                echo 'downloading source code'
                checkout scmGit(branches: [[name: '*/master']], extensions: [], userRemoteConfigs: [[url: 'https://github.com/jacksontechtraining/piplinejava40000']])
            }            
        }
        stage('compiling the application'){
            step{
                echo 'checking the java version'
                bat 'mvn compile'            
            }
            
        }
        stage('packaging the application'){
            step{
                echo 'checking the java version'
                bat 'mvn package'            
            }            
        }
        stage('installing dependency'){
            step{
                echo 'checking the java version'
                bat 'mvn install'            
            }            
        }
        stage('testing the application'){
            step{
                echo 'checking the java version'
                bat 'mvn test'            
            }            
        }
    }
}