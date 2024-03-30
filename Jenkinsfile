pipeline {
  agent any
  tools { 
      maven 'DHT_MVN' 
      jdk 'DHT_SENSE' 
  }
  stages {
    stage('check out / Git') {
      steps {
        git(branch: 'master', url: 'https://github.com/raksha-shanbhag/maven-samples')
      }
    }

    stage('run') {
      steps {
        sh 'mvn verify'
      }
    }

  }
}
