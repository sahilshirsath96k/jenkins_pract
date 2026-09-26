pipeline {
  agent any
  stages {
    stage("Build ") {
      steps {
        echo "Building"
      }
    }
    stage("Test") {
      steps {
        echo "Testing"
      }
    }
   
    stage('Test Agent') {
      steps {
        sh 'mkdir -p new-folder'
        sh 'echo "Hello from Jenkins Agent!" > new-folder/jenfile'
        sh 'whoami >> new-folder/jenfile'
        sh 'hostname >> new-folder/jenfile'
        sh 'java --version >> new-folder/jenfile'
      }
    }
    stage("Deploy") {
      steps {
        echo "Deploying"
      }
    }
  }
}
