pipeline {
  agent any
  stages {
    stage('Build') {
      steps {
        echo 'This is the Introduction of Blue Ocean Pipeline Editor'
        sh 'mvn \'clean package\''
      }
    }
    stage('PastBuild') {
      steps {
        archiveArtifacts '**/target/*jar'
        junit '**/target/surface-reports/.*xml'
      }
    }
  }
}