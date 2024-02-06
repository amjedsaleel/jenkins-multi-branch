pipeline {
    agent any

    stages {
        stage('Unit testing') {
            steps {
                echo 'Echo Unit testing'
                sh 'sleep 10'
            }
        }

        stage('Sonarqube analysis') {
            steps {
                echo 'Sonarqube analysis'
                sh 'sleep 5'
            }
        }

        stage('For PR') {
            when {
                branch 'PR-*'
            }
            steps {
                echo 'Echo PR test'
                sh 'sleep 30'
                publishChecks name: 'PR-testing', title: 'PR-testing'
            }
        }

        stage('Deploy to dev') {
            when {
                branch 'dev'
            }
            steps {
                echo 'Deploying to dev'
                sh 'sleep 14'
            }
        }  

        stage('Deploy to staging') {
            when {
                branch 'staging'
            }            
            steps {
                echo 'deploying to staging'
                sh 'sleep 14'
            }
        }

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
