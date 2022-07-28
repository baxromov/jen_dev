pipeline {
    agent any
    stages {
        stages ('Setup Python virtual environment'){
            steps{
                ssh '''
                        chmod +x ./envsetup.sh
                        ./envsetup.sh
                    '''

            }
        }
        stages ('Setup Gunicorn service') {
            steps {
                ssh '''
                        chmod +x ./gunicorn.sh
                        ./gunicorn.sh
                    '''
            }
        }
        stages ('Setup Nginx service') {
            steps {
                ssh '''
                        chmod +x ./nginx.sh
                        ./nginx.sh
                    '''
            }
        }
    }
}