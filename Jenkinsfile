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
                git 'https://github.com/ikaudanaveen/Simple-DevOps-Project.git'
            }
        }
        stage('build'){
            steps{
                sh 'mvn clean install'
            }
        }
    }    
}

