pipeline {
  agent none
  stages {
    stage('fetch sources') {
      steps {
        git(url: 'git@github.com:kpoissonnier/simple-python-pyinstaller-app.git', branch: 'master')
      }
    }
    stage('Build') {
      steps {
        sh 'python -m py_compile sources/add2vals.py sources/calc.py'
      }
    }
  }
}