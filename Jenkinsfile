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
            sh 'docker build -t registry.gitlab.com/qminhh/demo-gitlab-ci-nodejs:test1 .'
		}
       }
    }
        post {
	    success {
	    emailext body: '${DEFAULT_CONTENT}', subject: '${DEFAULT_SUBJECT}', to: 'ducminh96@gmail.com'
	    }
	}
}
