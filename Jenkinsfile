pipeline {
    agent any

    tools {
        maven 'Maven-3.9'
    }

    stages {
        stage('Clone projet Maven') {
            steps {
                dir('mvn-helloword') {
                    git branch: 'main',
                        url: 'https://github.com/anis-dvp/mvn-helloword.git'
                }
            }
        }

        stage('Build Maven') {
            steps {
                dir('mvn-helloword') {
                    sh 'mvn clean package'
                }
            }
        }

        stage('Build image Docker') {
            steps {
                dir('mvn-helloword') {
                    sh 'docker build -t anis/mvn-helloword:latest .'
                }
            }
        }
    }
}
