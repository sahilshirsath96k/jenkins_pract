pipeline {
  agent {
    label 'pract_agent'
  }
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
        sh 'cd new-folder'
        sh 'touch jenfile'
        sh 'echo "Hello from Jenkins Agent!" >> jenfile '
        sh 'whoami >> jenfile'
        sh 'hostname >> jenfile'
        sh 'java -version >> jenfile'
      }
    }
    stage("Deploy") {
      steps {
        echo "Deploying"
      }
    }
  }
}
