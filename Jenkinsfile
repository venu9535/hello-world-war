pipeline {
    agent { label 'venu123' }
    stages {
        stage('clone step') {
            steps {
                sh 'https://github.com/venu9535/hello-world-war.git'
                
            }
        }
  stage('build step') {
            steps {
                sh 'mvn package'
                
            }
        } 
    
    }
}
