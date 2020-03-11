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

        stage('IOS Build') {
            steps {
                sh 'ionic capacitor build ios --prod'
                
            }
        }

        stage('Android Build') {
            steps {
                sh 'ionic capacitor build android --prod'
                
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

