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
    stage('Test') {
      steps {
        echo 'Unit tests'
        echo 'Integration tests'
      }
    }
    stage('Code Quality Check') {
      steps {
        echo 'Check the quality of the code'
      }
    }
    stage('Deploy') {
      steps {
        echo "Deploy the application to testing environment: $TESTING_ENVIRONMENT"
      }
    }
    stage('Approval') {
      steps {
        sleep time: 10, unit: 'SECONDS'
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
