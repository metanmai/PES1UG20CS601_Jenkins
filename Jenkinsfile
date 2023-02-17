pipeline {
  agent any
  stages {
    stage('Build') {
      steps {
        sh 'g++ test.cpp'
        build job: 'PES1UG20CS601-1'
        echo 'Built Successfully 🤌'
      }
    }
    stage('Test') {
      steps {
        sh './a.out'
        echo 'Test Passed 😳'
      }
    }
    stage('Deploy') {
      steps {
        echo 'Deployed Successfully 😎'
      }
    }
  }
  post{
    failure{
        echo "Pipeline failed 🤬"
    }
  }
}
