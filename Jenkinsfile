pipeline {
    agent { label 'slave'}
    stages {
        stage('test') {
            steps {
            git 'https://github.com/handuy/nodejs-todolist.git'
		}
        }
       stage('build') {
            steps {
            sh 'docker build -t registry.gitlab.com/qminhh/demo-gitlab-ci-nodejs:test .'
		}
       }
        stage('run') {
            steps {
            sh 'docker run -p 80:80 registry.gitlab.com/qminhh/demo-gitlab-ci-nodejs'
		}
        }

    }
}
