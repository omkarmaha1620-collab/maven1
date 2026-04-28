pipeline {
    agent any

    tools {
        maven 'Maven'   // must match Jenkins tool name
        jdk 'jdk21'
    }

    stages {
        stage('Checkout') {
            steps {
                git branch: 'main', url: 'https://github.com/omkarmaha1620-collab/maven1.git'
            }
        }

        stage('Build') {
            steps {
                sh 'mvn clean package'
            }
        }

        stage('Run Application') {
            steps {
                sh 'java -jar target/*.jar'
            }
        }
    }
}
