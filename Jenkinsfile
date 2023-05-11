pipeline {
  agent any
  stages {
    stage('stage 1') {
      steps {
        sh 'sudo apt -y update && sudo apt -y upgrade'
      }
    }

    stage('stage 2') {
      steps {
        sh 'dpkg -l > /tmp/paquets'
      }
    }

    stage('stage 3') {
      steps {
        sh '''if [ `grep -c git /tmp/paquets` -ne 0 ]
then
dpkg -s git
else
sudo apt install -y git
fi'''
      }
    }

  }
}