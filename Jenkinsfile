pipeline {
    agent any

    tools {
        maven 'maven'
        jdk 'jdk'
    }

    stages {

        stage('Checkout') {
            steps {
                git branch: 'main', url: 'https://github.com/Devansha-Awasthi/sample-maven-project.git'
            }
        }

        stage('Build') {
            steps {
                bat 'mvn clean package'
            }
        }

        stage('Run') {
            steps {
                bat 'java -jar target/sample-maven-app-1.0-SNAPSHOT.jar'
            }
        }

    }
}
