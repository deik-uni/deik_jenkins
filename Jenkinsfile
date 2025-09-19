pipeline {
  agent any
  environment {
    DIRECTORY_PATH         = 'src'
    TESTING_ENVIRONMENT    = 'staging'
    PRODUCTION_ENVIRONMENT = 'Daniel Eikelis'
  }
  stages {
    stage('Build') {
      steps {
        echo "Fetch the source code from the directory path: $DIRECTORY_PATH"
        echo 'Compile the code and generate any necessary artefacts'
      }
    }
    stage('Unit & Integration Tests') {
      steps {
        echo 'Unit tests'
        echo 'Integration tests'
      }
    }
    stage('Code Analysis') {
      steps {
        echo 'Check the quality of the code'
      }
    }
    stage('Security Scan') {
      steps {
      }
    }
    stage('Deploy to Staging') {
      steps {
        echo "Deploy the application to testing environment: $TESTING_ENVIRONMENT"
      }
    }
    stage('Integration Tests on Staging') {
      steps {
      }
    }
    stage('Deploy to Production') {
      steps {
        echo "Deploying the application to the production environment: $PRODUCTION_ENVIRONMENT"
      }
    }
  }
  post {
    success {
      echo 'Pipeline completed successfully.'
    }
  }
}
