pipeline{
    agent any

    stages{
        stage('check java version'){
            echo 'checking the java version'
            bat 'java --version'            
        }
        stage('checkout from git'){
            echo 'downloading source code'
            checkout scmGit(branches: [[name: '*/master']], extensions: [], userRemoteConfigs: [[url: 'https://github.com/jacksontechtraining/piplinejava40000']])
        }
        stage('compiling the application'){
            echo 'checking the java version'
            bat 'mvn compile'            
        }
        stage('packaging the application'){
            echo 'checking the java version'
            bat 'mvn package'            
        }
        stage('installing dependency'){
            echo 'checking the java version'
            bat 'mvn install'            
        }
        stage('testing the application'){
            echo 'checking the java version'
            bat 'mvn test'            
        }
    }
}