stage('Build') {
  agent {
    docker {
      image 'mcr.microsoft.com/dotnet/sdk:8.0'
      args '-u root:root'
    }
  }
  steps {
    sh 'dotnet --version'
    sh 'dotnet build HelloApi.csproj'
  }
}
pipeline {
  agent any

  stages {
    stage('Checkout') {
      steps {
        deleteDir()        // clean workspace
        checkout scm
      }
    }

    stage('Build') {
      agent {
        docker {
          image 'mcr.microsoft.com/dotnet/sdk:8.0'
          args '-u root:root'
        }
      }
      steps {
        sh 'dotnet --version'
        sh 'dotnet build'
      }
    }
  }
}
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

