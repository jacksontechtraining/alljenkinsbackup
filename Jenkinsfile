pipeline{
    agent any

    stages{
        stage('check java version'){
            steps{
                echo 'checking the java version'
                bat 'java --version'    
            }
                    
        }
        stage('checkout from git'){
            steps{
                echo 'downloading source code'
                checkout scmGit(branches: [[name: '*/master']], extensions: [], userRemoteConfigs: [[url: 'https://github.com/jacksontechtraining/piplinejava40000']])
            }            
        }
        stage('compiling the application'){
            steps{
                echo 'checking the java version'
                bat 'mvn compile'            
            }
            
        }
        stage('packaging the application'){
            steps{
                echo 'checking the java version'
                bat 'mvn package'            
            }            
        }
        stage('installing dependency'){
            steps{
                echo 'checking the java version'
                bat 'mvn install'            
            }            
        }
        stage('testing the application'){
            steps{
                echo 'checking the java version'
                bat 'mvn test'            
            }            
        }
    }
}