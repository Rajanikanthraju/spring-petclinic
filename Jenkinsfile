node('jdk11') {
    stage('source code') {
        // git repo
        git branch: 'sprint_develop', url: 'https://github.com/Rajanikanthraju/spring-petclinic.git'
    }
    stage('build') {
         sh 'mvn package'
    }
    stage('Test results and artifacts') {
         junit '**/surefire-reports/*.xml'
         archiveArtifacts artifacts: '**/*.war', followSymlinks: false
    }
}