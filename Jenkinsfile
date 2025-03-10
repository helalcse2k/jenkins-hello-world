pipeline {
    agent any

    tools {
        // Install the Maven version configured as "M3" and add it to the path.
        maven "M398"
    }

    stages {
        stage('Echo Version') {
            steps {
                sh 'echo Print Maven Version'
                sh 'mvn -version'
            }
            
        }
        
        stage('Build') {
            
            steps { 
                //get some code from github repo
               // git branch: 'main', changelog: false, poll: false, url: 'https://github.com/helalcse2k/jenkins-hello-world.git'
                
                // Run maven package CMD
                sh "mvn clean package -DskipTests=true"
            }  
        }
        
        stage('Unit Test') {
            
            steps {
                sh "mvn test"
            }
            
        }
        
        
        
       
    }
}
