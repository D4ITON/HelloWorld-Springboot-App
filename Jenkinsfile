pipeline{
    agent any
    stages{
        stage('Git clone'){
            steps{
                git 'https://github.com/shazforiot/HelloWorld-Springboot-App.git'
            }
        }
        
        stage('maven build'){
            withMaven(maven: 'mvn') {
                sh 'mvn package'
            }
        }
        stage('Create Dockerimage'){
            steps{
                sh 'docker build -t thetips4you/springboot:latest .'
            }
        }
        
    }
}
