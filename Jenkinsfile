pipeline {
    agent any
    stages {
        stage('Hello') {
            steps {
                echo 'Hello World !'
            }
        }
        stage('Checkout') {
            steps {
                git branch: 'main',
                    url: 'https://github.com/ranimsouissi/spring-petclinic-pipeline.git'
            }
        }
        stage('Build') {
            steps {
                // Maven build sans tests pour aller plus vite
                sh 'mvn clean install -DskipTests'
            }
        }
    }
}
