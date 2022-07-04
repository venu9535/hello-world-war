pipeline {
    agent { label 'java' }
    stages {
        stage('clone step') {
            steps {
                sh 'rm -rf hello-world-war'
                sh ' git clone https://github.com/sudarshan1912/hello-world-war.git'
            }
        }
      stage('build step') {
            steps {
                sh 'mvn package'
            }
        }
       stage('deploy step') {
            steps {
              sh 'sudo cp /home/slave1/workspace/Hello_WorldWar_Job/target/hello-world-war-
