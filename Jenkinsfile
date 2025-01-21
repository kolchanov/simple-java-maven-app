pipeline {
    agent any
    tools {
        jdk '11.0.1' 
        maven '3.9.9' 
    }
    stages {
        stage ('Initialize') {
            steps {
                sh '''
                    export JAVA_HOME=/var/jenkins_home/tools/hudson.model.JDK/11.0.1
                    echo "JAVA_HOME = ${JAVA_HOME}"
                ''' 
            }
        }        
        stage('Build') { 
            steps {
                sh 'mvn -B -DskipTests clean package' 
            }
        }
    }
}
