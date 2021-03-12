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
            sh 'ls -lrt'
            sh 'pwd'
            sh 'docker login registry.gitlab.com'
            sh 'docker build -t registry.gitlab.com/qminhh/demo-gitlab-ci-nodejs .'
            sh 'docker ps && docker images'
            sh 'docker push registry.gitlab.com/qminhh/demo-gitlab-ci-nodejs'
		}
        } 
    }
}
