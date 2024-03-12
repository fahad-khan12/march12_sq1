pipeline {
  agent any 
  
  stages {
    stage('Checkout') {
      steps {
        git branch: 'master', url: 'https://github.com/fahad-khan12/sonarqube-codecoverage-example.git'
      }
    }
    stage('SonarQube Analysis') {
      steps {
        loadSonarProperties 'com.examples.school/sonar-project.properties'
        sh 'mvn sonar:sonar'
      }
    }
  }
}
