# cleverwar
Java achival file (WAR) used in deploying to apache-tomcat web severs.

1.  Download source file from a URL and save it under ${JENKINS_HOME}/${PROJECT_NAME}/*.war
    e.g. wget http://aesclever.com/aftp/.linux3.0/TcpipLinux.war

2.  Deploy war file to authorized node under ${CATALINA_HOME}/webapps
    e.g. scp -O ${JENKINS_HOME}/${PROJECT_NAME}/*.war [target/http://host_ip/fullpath_to_webapps/]
    
    Example:
        sh 'scp -o StrictHostKeyChecking=no target/TcpipLinux.war admin@192.168.100.12:/usr/share/tomcat/webapps/'
