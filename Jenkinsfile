pipeline {
  agent any
  stages {
    stage('syntax') {
      steps {
        sh 'python -m py_compile program.py'
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
        sh 'echo "data_subor" > generatedFile.txt'
      }
    }

    
  }
  post {
    always {
      archiveArtifacts artifacts: 'generatedFile.txt', onlyIfSuccessful: true
    }
  }
  
}    
  
