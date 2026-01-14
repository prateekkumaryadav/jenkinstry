pipeline {
  agent any
  stages {
    stage('update_file') {
      steps {
        git(url: 'https://github.com/prateekkumaryadav/jenkinstry', branch: 'main')
      }
    }

    stage('log') {
      parallel {
        stage('log') {
          steps {
            sh 'ls -la'
          }
        }

        stage('log2') {
          steps {
            sh 'ls -l'
          }
        }

      }
    }

  }
}