pipeline {
    agent any
    stages {
        stage('test') {
            steps {
            git branch: 'main', url: 'https://github.com/qmiinh/nodejs-todolist.git'
		}
        }
       stage('build') {
            steps {
            sh label: '', script: 'docker build -t nodejs .'
		}
        } 
    }
}
