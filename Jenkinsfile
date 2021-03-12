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
            sh 'docker build -t nodejs .'
		}
        } 
    }
}
