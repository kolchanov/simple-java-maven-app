pipeline {
    agent any
    tools {
        jdk '17' 
        maven '3.9.9' 
    }
    stages {      
        stage('Build') { 
            steps {
                sh '''
                    export JAVA_HOME=/var/jenkins_home/tools/hudson.model.JDK/17/jdk-17.0.13+11
                    echo "JAVA_HOME = ${JAVA_HOME}"
                    mvn -B -DskipTests clean package
                ''' 
            }
        }
    }
}
