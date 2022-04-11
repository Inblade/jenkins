pipeline {
    agent any

    stages {
        stage('Add tag') {
            steps {
                sh 'git config --global user.email "dkocheto@gmail.com"'
                sh 'git config --global user.name   "Inblade"'
                sh 'git tag -a v0.1 -m "v0.1"'
            }
        }
        stage('Add branch'){
            steps {
                sh 'git checkout -b v0.2-rc1 '
            }
        }
        stage('Git push repo') {
            steps {
                sh 'git push --all'
                sh 'git push --tag'

            }
        }
    }
}
