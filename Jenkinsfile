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

    stage('sucess_display') {
      steps {
        emailext(subject: 'build sucessful', body: 'dummy', from: 'prateek.student20@gmail.com', to: 'prateek.yadav2006@gmail.com')
      }
    }

  }
}