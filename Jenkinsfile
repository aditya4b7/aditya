pipeline {
    agent any 
    stages {
        stage('Build') { 
            steps {
                sh ''' 
                 wget http://apache.mirror.iweb.ca/tomcat/tomcat-8/v8.5.47/bin/apache-tomcat-8.5.47.zip
                 unzip apache-tomcat-8.5.47.zip
                 cp server.xml apache-tomcat-8.5.47/conf/
                 cd apache-tomcat-8.5.47/bin
                 chmod u+x *.sh
                 sh -x startup.sh
                 '''
            }
        }
        stage('Test') { 
            steps {
                sh ' netstat -ant | grep 8081 '
            }
        }
        stage('Deploy') { 
            steps {
                sh  ' echo tomcat installation successful ' 
            }
        }
    }
}
