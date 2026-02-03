pipeline {
  agent {
    docker {
      image 'mcr.microsoft.com/dotnet/sdk:8.0'
      args '-u root:root'
    }
  }
  stages {
    stage('Build') {
      steps {
        sh 'dotnet --version'
        sh 'dotnet build'
      }
    }
  }
}
pipeline {
  agent any
  stages {
    stage('Build') {
      steps {
        sh 'dotnet build'
      }
    }
  }
}

