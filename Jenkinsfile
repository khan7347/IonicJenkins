pipeline {

    agent any

    environment {
        PATH='/usr/bin:/usr/bin:/bin'
    }

    stages {

        stage('NPM Setup') {
            steps {
                sh 'npm install'
            }
        }

        stage('IOS Build') {
            steps {
                sh 'ionic cordova build ios --prod'
            }
        }

        stage('Android Build') {
            steps {
                sh 'ionic cordova build android --prod'
            }
        }
    }
}

