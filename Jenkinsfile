pipeline {
  agent any
  stages {
    stage('checkoutGit') {
      steps {
        git(url: 'https://github.com/elestopadov/jenkins-example-app.git', branch: 'main')
      }
    }

    stage('build') {
      steps {
        echo 'this is build'
      }
    }

    stage('deploy') {
      parallel {
        stage('deploy_dev2') {
          steps {
            sleep 30
            echo 'completed'
          }
        }

        stage('deploy_dev1') {
          steps {
            sleep 10
            echo 'finised'
          }
        }

      }
    }

    stage('Test') {
      steps {
        echo 'testing'
      }
    }

  }
}