pipeline {
    agent any

    stages {
        stage('Build'){
            steps {
                bat 'docker-compose build'
            }

        }

        stage('Test') {
            steps {
                bat 'docker-compose run web python manage.py test'
            }
        }
    }

    post{
        success{
            echo 'Everthing passed'
        }
        failure{
            echo 'Something failed'
        }
    }
}