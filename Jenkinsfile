
pipeline{
    agent any

    tools{
        maven 'maven3'
    }

    stages{
        stage('clone'){
            steps{
           git 'https://github.com/akashjena9208/Devops_Deployee_WebChat.git'
                
            }
        }
        stage('compile'){
            steps{
                sh 'mvn clean compile'
            }
        }
        stage('test'){
            steps{
                sh 'mvn test'
            }
        }
        
        stage('package'){
            steps{
                sh 'mvn package'
            }
        }
        stage('run the application'){
            steps{
                sh 'cd target && mv *.war /usr/local/tomcat/webapps/ROOT.war'
            }
        }
    }
}
