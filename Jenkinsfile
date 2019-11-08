pipeline {
    agent any 
    stages {
        stage('Build') { 
            steps {
                 wget http://apache.mirror.iweb.ca/tomcat/tomcat-8/v8.5.47/bin/apache-tomcat-8.5.47.zip
                 unzip apache-tomcat-8.5.47.zip
                 cd apache-tomcat-8.5.47/bin
                 chmod u+x *.sh
                 sh -x startup.sh
                 
            }
        }
        stage('Test') { 
            steps {
                // 
            }
        }
        stage('Deploy') { 
            steps {
                // 
            }
        }
    }
}
