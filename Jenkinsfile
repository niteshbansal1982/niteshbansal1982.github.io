pipeline {
  agent any
  stages {
    stage('checkout') {
      steps {
        build(job: 'firstbuild', quietPeriod: 30)
      }
    }
    stage('test') {
      steps {
        echo 'hello test'
      }
    }
    stage('deploy') {
      steps {
        node(label: 'UAT') {
          sh 'abc.sh'
        }
        
      }
    }
    stage('promote') {
      steps {
        echo 'promote to main'
      }
    }
  }
}