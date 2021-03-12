pipeline {
    agent any
    stages {
        stage('test') {
            steps {
            git 'https://github.com/handuy/nodejs-todolist.git'
		}
        }
       stage('build') {
            steps {
            sh 'ls -lrt'
            sh 'sudo docker ps'
            sh 'docker build -t nodejs .'
		}
        } 
    }
}
