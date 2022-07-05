pipeline {
    agent { label 'java' }
    stages {
        stage('clone step') {
            steps {
                sh 'rm -rf hello-world-war'
                sh 'git clone https://github.com/venu9535/hello-world-war.git'
            }
        }
      stage('build step') {
            steps {
                sh 'mvn package'
            }
        }
  
    }
}
      
