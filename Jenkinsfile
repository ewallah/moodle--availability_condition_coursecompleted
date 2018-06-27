pipeline {
  agent any
  stages {
    stage('phpunit init') {
      steps {
        sh '''psql -U moodle -h localhost -d postgres -c "DROP DATABASE IF EXISTS phpunit;"
psql -U moodle -h localhost -d postgres -c "CREATE DATABASE phpunit ENCODING \'utf8\' OWNER moodle;"
'''
      }
    }
    stage('config') {
      steps {
        writeFile(file: 'config.php', text: 'txt')
      }
    }
  }
}