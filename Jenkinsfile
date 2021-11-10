pipeline {
  agent any
  stages {
    stage('Build') {
      steps {
        echo 'this is the Build job'
        sh 'npm install'
      }
    }

    stage('Test') {
      steps {
        echo 'this is the Test job'
        sh 'npm test'
      }
    }

    stage('Package') {
      steps {
        echo 'this is the third job'
        sh 'npm run package'
      }
    }

    stage('Archive') {
      steps {
        archiveArtifacts '**/distribution/*zip'
      }
    }

  }
  tools {
    nodejs 'nodejs'
  }
  post {
    always {
      echo 'this pipeline has completed...'
    }

  }
}