pipeline {
    agent any
    tools {
        gradle 'gradle-7.4.2'
        jdk 'jdk1.8'
    }
    stages {
        stage('cloning git') {
            steps{
            git credentialsId: '41221fdb-cc3b-417a-86fc-d83abd7fd46f', url: 'https://github.com/Abhishek226-ii/gradle-app.git'
            }
        }
        stage('Build') {
            steps {
                sh './gradlew assemble'
            }
        }
        stage('Test') {
            steps {
                sh './gradlew test'
            }
        }
    }
}
