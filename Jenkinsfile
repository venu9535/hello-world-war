pipeline {
    agent { label 'java' }
    stages {
        stage('setting parameters to the job') {
            steps {
                script {
                    properties([ 
                        parameters([ 
                            choice( 
                                choices: ['testing', 'development'],
                                name :'environments'
                            )
                        ])
                    ])
                }
				}
				}
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
              sh 'sudo cp /home/venu1/workspace/testing/target/hello-world-war-1.0.0.war /opt/apache-tomcat-9.0.64/webapps'
            }
        }
    }
}

      
