pipeline {
    agent any
    
    stages{
        
        stage('Git Clone or Pull'){
            
            steps {
                git 'https://github.com/asquarezone/spring-petclinic.git'
            }
        }
        
        stage('Maven Build'){
            steps{
                sh 'mvn clean install'
            }
        }
        
        stage('Publish'){
            steps{
                archiveArtifacts 'target/springboot-petclinic-1.4.1.jar'
                junit 'target/surefire-reports/*.xml'
                
            }
        }
    }
}