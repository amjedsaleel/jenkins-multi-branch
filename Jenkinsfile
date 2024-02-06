pipeline {
    agent any

    stages {
        stage('Unit testing') {
            steps {
                echo 'Echo Unit testing'
                sh 'sh sleep 10'
            }
        }
    }

    stages {
        stage('Sonarqube analysis') {
            steps {
                echo 'Sonarqube analysis'
                sh 'sleep 5'
            }
        }
    }

    stages {
        stage('For PR') {
            steps {
                echo 'Echo Unit testing'
            }
        }
    }        

    stages {
        stage('Deploy to dev') {
            when {
                branch 'dev'
            }
            steps {
                echo 'Deploying to dev'
                sh 'sleep 14'
            }
        }
    }

    stages {
        stage('Deploy to staging') {
            when {
                branch 'staging'
            }            
            steps {
                echo 'deploying to staging'
                sh 'sleep 14'
            }
        }
    } 

    stages {
        stage('Deploy to production') {
            when {
                branch 'production'
            }              
            steps {
                echo 'deploying to production'
                sh 'sleep 14'
            }
        }
    }        
}
