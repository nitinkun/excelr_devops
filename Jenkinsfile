pipeline {
  agent any
  stages {
    stage('fetch code') {
      steps {
        git(url: 'https://github.com/nitinkun/excelr_devops.git', branch: 'main', poll: true)
      }
    }

    stage('install apache') {
      steps {
        sh 'sudo apt install apache2 -y'
      }
    }

    stage('Deploy App') {
      steps {
        sh 'sudo cp * /var/www/html/'
      }
    }

  }
}