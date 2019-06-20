pipeline {
  agent {
    docker {
      image 'node:6-alpine'
      args '-p 3000:3000'
    }

  }
  stages {
    stage('Build') {
      parallel {
        stage('Build') {
          steps {
            echo 'build start'
          }
        }
        stage('Test') {
          steps {
            sleep 5
          }
        }
      }
    }
    stage('hahah') {
      agent {
        docker {
          image 'goalng'
          args 'echo $test'
        }

      }
      environment {
        test = '11'
      }
      steps {
        sh './jenkins/scripts/test.sh'
      }
    }
  }
}