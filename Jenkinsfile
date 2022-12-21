pipeline{
    agent any
    tools {
         maven 'maven'
    }
    options {
        buildDiscarder logRotator(artifactDaysToKeepStr: '', artifactNumToKeepStr: '', daysToKeepStr: '7', numToKeepStr: '7')
    }
    stages{
        stage('checkout'){
            steps{
                git 'https://github.com/ikaudanaveen/hello-world.git'
            }
        }
        stage('unit test'){
            steps{
                sh 'mvn test'
            }
        }
        stage('Integration testing'){
            steps{
                sh 'mvn verify -DskipUnitTests'
            }
        }
        stage('build'){
            steps{
                sh 'mvn clean install'
            }
        }
    }    
}

