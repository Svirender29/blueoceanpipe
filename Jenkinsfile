pipeline {
  agent any
  stages {
    stage('Start Build') {
      steps {
        sh '''pwd
date
ls
tree'''
      }
    }

    stage('Test Build') {
      parallel {
        stage('Test Build') {
          steps {
            echo 'testing step'
          }
        }

        stage('Test par') {
          steps {
            echo 'Test par'
          }
        }

      }
    }

    stage('Deploy ') {
      parallel {
        stage('Deploy ') {
          steps {
            echo 'Deployment'
            sh '''pwd
cat /etc/passwd
ls'''
          }
        }

        stage('error') {
          steps {
            sleep 7
          }
        }

      }
    }

    stage('Finish') {
      steps {
        echo 'Build Completed'
      }
    }

  }
}