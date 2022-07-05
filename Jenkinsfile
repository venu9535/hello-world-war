properties([ parameters([ choice( choices: ['ONE', 'TWO'], name: "")])])
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
   stage('deploy step') {
            steps {
                sh 'sudo mv /home/venu1/workspace/helloworld2/target/hello-world-war-1.0.0.war /home/venu1/workspace/helloworld2/target/parameter_pipeline.war
                sh 'sudo cp /home/venu1/workspace/helloworld2/target/parameter_pipeline.war.war /opt/apache-tomcat-9.0.64/webapps'
            }
        }
    }
}
      
