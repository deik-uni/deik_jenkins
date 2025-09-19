pipeline {
  agent any
  environment {
    DIRECTORY_PATH         = 'src'
    TESTING_ENVIRONMENT    = 'staging'
    PRODUCTION_ENVIRONMENT = 'Daniel Eikelis'
  }
  stages {
    stage('Build') { 
      steps { echo "Build: compile & package (tool: Maven)" } 
    }
    stage('Unit & Integration Tests') { 
      steps { echo "Unit & Integration Tests: run tests (tools: JUnit, Cypress)"} 
    }
    stage('Code Analysis') { 
      steps { echo "Code Analysis: static analysis (tool: SonarQube/SonarCloud)"} 
    }
    stage('Security Scan') { 
      steps { echo "Security Scan: vulnerability scan (tool: OWASP Dependency-Check)"} 
    }
    stage('Deploy to Staging') { 
      steps { echo "Deploy to Staging: push app to staging (tools: Docker + Ansible)"} 
    }
    stage('Integration Tests on Staging') { 
      steps { echo "Integration Tests on Staging: E2E checks (tool: Postman/Newman)"} 
    }
    stage('Deploy to Production') { 
      steps { echo "Deploy to Production: promote release (tool: Ansible/Kubernetes)"} 
    }
  }
  post {
    success {
      echo 'Pipeline completed successfully.'
    }
  }
}
