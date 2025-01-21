pipeline {
    agent any
    tools {
        jdk '11.0.1' 
        maven '3.9.9' 
    }
    stages {
        stage('Build') { 
            steps {
                sh 'mvn -B -DskipTests clean package' 
            }
        }
    }
}
