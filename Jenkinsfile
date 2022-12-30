pipeline {
    agent {
        docker {
            image 'eclipse-temurin:8-jdk-jammy'
        }
    }
    options {
        skipStagesAfterUnstable()
    }
    stages {
        stage('Build') {
            steps {
                sh './gradlew build -x test'
            }
        }
    }
}