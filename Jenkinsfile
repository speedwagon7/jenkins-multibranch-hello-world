pipeline {
    agent any
    
    tools {
        maven "M3" // Assumes Maven is set up in Jenkins with the name "M3"
    }
    
    stages {
        stage('SCM') {
            steps {
                // Check out the current branch's code
                git branch: "main", url: 'https://github.com/speedwagon7/jenkins-multibranch-hello-world.git'
            }
        }
        
        stage('Build') {
            steps {
                // Run Maven build
                sh 'mvn clean install'
            }
        }
        
        stage('Test') {
            steps {
                // Run any tests if needed
                sh 'mvn test'
            }
        }
    }
}
