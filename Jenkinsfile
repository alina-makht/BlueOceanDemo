pipeline {
  agent any
  stages {
    stage('CheckOutGit') {
      steps {
        git(url: 'https://github.com/elestopadov/jenkins-example-app.git', branch: 'main')
      }
    }

    stage('Build') {
      steps {
        echo 'This is build'
      }
    }

    stage('Deploy to Dev1') {
      parallel {
        stage('Deploy to Dev1') {
          steps {
            sleep 30
            echo 'Finished'
          }
        }

        stage('Deploy to Dev2') {
          steps {
            sleep 50
            echo 'Completed'
          }
        }

      }
    }

    stage('Test') {
      steps {
        echo 'Testing...'
      }
    }

  }
}