pipeline {
  agent any
  stages {
    stage('phpunit init') {
      steps {
        sh 'psql -U moodle -h localhost -d postgres -c "CREATE DATABASE $JOB_NAME OWNER moodle;"'
      }
    }
  }
}