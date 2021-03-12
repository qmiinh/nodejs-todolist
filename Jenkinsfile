pipeline {
    stages {
        stage('test') {
            steps {
            git 'https://github.com/handuy/nodejs-todolist.git'
		}
        }
       stage('build') {
            steps {
            which 'docker'
            sh 'ls -lrt'
            sh 'docker build -t nodejs .'
		}
        } 
    }
}
