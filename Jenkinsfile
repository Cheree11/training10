pipeline {
  agent any
  stages {
    stage('syntax') {
      steps {
        sh 'python -m py_compile python.py'
      }
    }
    stage('Testing') {
      steps {
        sh 'bash test.sh'
      }
    }
    stage('Deploy') {
      steps {
        sh 'echo "Deploy to server"'
      }
    }
  }
}  