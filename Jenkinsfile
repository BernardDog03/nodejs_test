pipeline { agent any

environment {
    NODEJS_HOME = /usr/bin/node
    PATH = "${NODEJS_HOME}/bin:${env.PATH}"
}

stages {
	stage('Parallel Execution'){
		parallel {
			stage('Test on NodeJS 14') {
				steps {
					script {
						env.NODE_VERSION = '14'
						sh 'nvm install 14'
						sh 'npm install'
						sh 'npm test'
					}
				}
			}
			stage('Test on NodeJS 16') {
				steps {
					script {
						env.NODE_VERSION = '16'
						sh 'nvm install 16'
						sh 'npm install'
						sh 'npm test'
					}
				}
			}
		}
	}
}
}
