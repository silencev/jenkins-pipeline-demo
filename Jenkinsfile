pipeline {
  agent none
  stages {
    stage('Build') {
      agent {
        dockerfile {
            filename 'Dockerfile'
            additionalBuildArgs  '--build-arg version=1.0.2 -t epas:flask'
        }
      }
      steps{
        sh 'python -c "import sys;print(sys.executable, sys.version)"'
      }
    }
  }
}
