pipeline {
    agent any
    stages {
        stage('Build') {
           steps{
                sh '''
                        chmod +x ./initial-setup.sh
                        ./initial-setup.sh
                    '''

            }
        }
        stage ('Setup Python virtual'){
            steps {
                sh '''
                        chmod +x ./envsetup.sh
                        ./envsetup.sh
                    '''

            }

        }
        stage ('Setup Gunicorn service') {

            steps {
                sh '''
                        chmod +x ./gunicorn.sh
                        ./gunicorn.sh
                    '''
            }

        }
        stage ('Setup Nginx service') {

            steps {
                sh '''
                        chmod +x ./nginx.sh
                        ./nginx.sh
                    '''
            }

        }
    }
}