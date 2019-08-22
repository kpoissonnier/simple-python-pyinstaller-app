pipeline {
  agent none
  stages {
    stage('fetch sources') {
      steps {
        git(url: 'git@github.com:kpoissonnier/simple-python-pyinstaller-app.git', branch: 'master', credentialsId: '36c95e230b0f0fcb8a4ccc2467bb0c5fd0e6d98b')
      }
    }
    stage('Build') {
      steps {
        sh 'python -m py_compile sources/add2vals.py sources/calc.py'
      }
    }
  }
}