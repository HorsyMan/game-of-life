pipeline {
  agent any
  stages {
    stage('Intro') {
      steps {
        echo 'This is the Introduction of Blue Ocean Pipeline Editor'
        tool(name: 'maven', type: '/bin/mvn clean package')
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