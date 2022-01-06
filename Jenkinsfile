pipeline {
  agent any
  stages {
    stage('Stage1') {
      steps {
        sh 'grep user /etc/passwd'
      }
    }

    stage('Stage2') {
      steps {
        sh '''if test `grep -c orsys /etc/passwd` -ne 0
then 
find / -user orsys > /tmp/orsys 
fi '''
      }
    }

  }
}