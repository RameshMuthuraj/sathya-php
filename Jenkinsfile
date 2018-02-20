pipeline {
  agent any
  stages {
    stage('checkout') {
      parallel {
        stage('checkout') {
          steps {
            git(url: 'https://github.com/RameshMuthuraj/Sathya.git', branch: 'master', changelog: true, credentialsId: 'githubjenkins', poll: true)
          }
        }
        stage('') {
          steps {
            sh '''env
echo $user'''
          }
        }
      }
    }
    stage('build') {
      steps {
        echo 'build success'
      }
    }
    stage('complete') {
      steps {
        echo 'completed'
      }
    }
  }
}