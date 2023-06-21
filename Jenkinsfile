pipeline {
  agent any
  stages {
    stage('Fetch Code') {
      steps {
        git(url: 'https://github.com/mahesharimalla/BlueoceanRepo.git', branch: 'main')
      }
    }

    stage('Install Apache2') {
      steps {
        sh '''sudo apt install apache2 -y


'''
      }
    }

    stage('Deploy Application') {
      agent any
      steps {
        sh 'sudo cp -R * /var/www/html'
      }
    }

  }
}