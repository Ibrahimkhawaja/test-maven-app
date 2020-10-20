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
        stage ('Install') {
            steps {
                sh 'mvn install'
            }
        }
        stage ('Package') {
            steps {
                sh 'mvn package'
            }
        }
    }
}
