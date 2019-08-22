pipeline {
  agent none
  stages {
    stage('fetch sources') {
      steps {
        git(url: 'git@github.com:kpoissonnier/simple-python-pyinstaller-app.git', branch: 'master', credentialsId: '5ee8b52a75df71b1600dd0d1deede8ef0bf9ea36')
      }
    }
    stage('Build') {
      steps {
        sh 'python -m py_compile sources/add2vals.py sources/calc.py'
      }
    }
  }
}