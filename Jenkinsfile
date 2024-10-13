pipeline { agent any

environment {
    NODEJS_HOME = /usr/bin/node
    PATH = "${NODEJS_HOME}/bin:${env.PATH}"
}

stages {
    stage('Checkout') {
        steps {
            https://github.com/BernardDog03/nodejs_test.git
        }
    }

    stage('Install Dependencies') {
        steps {
            sh 'npm install'
        }
    }

    stage('Run Tests') {
        steps {
            sh 'npm test'
        }
    }
}
}
