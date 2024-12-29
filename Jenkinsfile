pipeline {
    agent any
    environment {
        MAVEN_HOME = '/opt/maven'
        PATH = "${MAVEN_HOME}/bin:${PATH}"
    }
    stages {
        stage('Build') {
            steps {
                sh 'mvn clean install -Denforcer.skip=true'
                sh 'mvn enforcer:enforce'
            }
        }
    }
}

