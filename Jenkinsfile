pipeline {
  agent any

  stages {
    stage('Clone') {
      steps {
        sh "git clone git@github.com:Inblade/jenkins.git"
      }
    }
    stage('Create tag1') {
      steps {
        sh "git tag v0.1"
      }
    }
    stage('Create branch') {
      steps {
        sh "git branch v0.2-rc1"
        sh "git push"
        sh "git push --tag"
      }
    }
  }
}
