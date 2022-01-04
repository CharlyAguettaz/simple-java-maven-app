pipeline {
    agent {
        docker {
            image 'maven:3.8.1-adoptopenjdk-11' 
            args '-v /root/.m2:/root/.m2' 
        }
    }

    stages {
        stage('Build') {
            steps {
            git branch: 'master',
                credentialsId: 'bb03cce7-668d-4102-b207-83d498cbb66f',
                url: 'git@github.com:alisnake62/simple-java-maven-app.git'

            sh "ls -la"
            sh "pwd"
            sh "java -jar HelloWorld.jar myargument3"
            }

        }
    }
}
