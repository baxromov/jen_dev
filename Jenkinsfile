pipeline {
    agent any
    stages {
        stage ('Setup Python virtual environment'){
            steps{
                ssh '''
                        chmod +x ./envsetup.sh
                        ./envsetup.sh
                    '''

            }
        }
        stage ('Setup Gunicorn service') {
            steps {
                ssh '''
                        chmod +x ./gunicorn.sh
                        ./gunicorn.sh
                    '''
            }
        }
        stage ('Setup Nginx service') {
            steps {
                ssh '''
                        chmod +x ./nginx.sh
                        ./nginx.sh
                    '''
            }
        }
    }
}