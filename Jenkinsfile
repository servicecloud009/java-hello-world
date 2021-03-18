pipeline{
    agent any
    
    environment {
       PATH = "/opt/apache-maven-3.6.3/bin:$PATH"
    }
    stages{
        stage("Git Checkout"){  
           steps{
            git branch: 'main', credentialsId: 'github', url: 'https://github.com/servicecloud009/myweb.git'
            }
        }
        stage("Maven Build"){
           steps{
              sh "mvn clean install"
           }
        }
    }
}
