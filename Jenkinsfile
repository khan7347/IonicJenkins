pipeline {

    agent any

    environment {
        PATH='/usr/local/bin:/usr/bin:/bin'
    }

    stages {

        stage('NPM Setup') {
            steps {
                sh 'npm install'
            }
        }

        stage('Android Build') {
            steps {
                sh 'ionic cordova build android --prod --no-confirm=true --gradleArg=--no-daemon'
                
            }
        }

        stage('IOS Build') {
            steps {
                sh 'ionic cordova build ios --prod --no-confirm=true'
                
            }
        }

        stage('APK Sign') {
            steps {
            // sh 'jarsigner -storepass your_password -keystore keys/yourkey.keystore platforms/android/app/build/outputs/apk/release/app-release-unsigned.apk nameApp'
                echo "Android"
            }
        }


        stage('Stage Web Build') {
            steps {
                sh 'npm run build --prod'
            }
        }

    }
}

