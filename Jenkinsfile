pipeline {
    agent any
    stages {
        stage('---clean---') {
            steps {
             withMaven(maven : 'maven3.6.2'){
             sh "mvn clean"
             }
             }
        }

        stage('--test--') {
            steps {
            withMaven(maven : 'maven3.6.2'){
                sh "mvn test"
            }
            }
        }

        stage('--package--') {
            steps {
                sh "mvn package"
            }
        }
    }
}
