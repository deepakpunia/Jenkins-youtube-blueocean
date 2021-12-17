pipeline {
  agent any
  stages {
    stage('Build') {
      steps {
        sh '''pwd
date'''
      }
    }

    stage('test') {
      parallel {
        stage('test') {
          steps {
            sleep 10
            echo 'test step'
          }
        }

        stage('test par') {
          steps {
            echo 'test par'
          }
        }

        stage('test par1') {
          steps {
            sh 'echo \'jai baba ki\''
          }
        }

      }
    }

    stage('deploy') {
      steps {
        echo 'deploy'
      }
    }

  }
}