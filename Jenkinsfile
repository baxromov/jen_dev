pipeline {
    agent any
    stages {
        stage ('Setup Python virtual A'){
            steps{
                sh '''
                        chmod +x ./initial-setup.sh
                        ./initial-setup.sh
                    '''

            }
            steps{
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