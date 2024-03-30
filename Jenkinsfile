pipeline {
  agent any
  stages {
    stage('check out / Git') {
      steps {
        git(branch: 'master', url: 'https://github.com/raksha-shanbhag/maven-samples')
      }
    }

    stage('run') {
      steps {
        sh '''mvn clean
mvn test
mvn verify'''
      }
    }

  }
  tools {
    maven 'DHT_MVN'
    jdk 'DHT_SENSE'
  }
}