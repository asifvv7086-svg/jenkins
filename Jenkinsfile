pipeline {
    agent any

    stages {

        stage('checkout') {
            steps {
                echo "Building Started"

                deleteDir()

                sh '''
                    git clone https://github.com/asifvv7086-svg/jenkins.git
                    ls -l
                '''
            }
        }

        stage('deploy') {
            steps {
                echo "Deployment Started"

                sh '''
                    rm -rf /var/www/html/*
                    cp -r jenkins/* /var/www/html/
                    ls -l /var/www/html
                '''
            }
        }
    }
}
