pipeline {
    agent any
    tools { 
        maven 'maven' 
        //jdk 'jdk8' 
    }
    stages {
        stage ('Initialize') {
            steps {
                sh '''
                    echo "PATH = ${PATH}"
                    echo "M2_HOME = ${M2_HOME}"
                ''' 
            }
        }

        stage ('Clean') {
            steps {
                sh 'mvn clean'
            }
        }
        stage ('Clean') {
            steps {
                sh 'mvn install'
            }
        }
        stage ('Clean') {
            steps {
                sh 'mvn package'
            }
        }
    }
}
