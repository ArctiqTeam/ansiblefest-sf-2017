pipeline {
  agent any
  stages {
    stage('Git Clone') {
      steps {
        git branch: 'lab', url: 'https://github.com/ArctiqTeam/ansiblefest-sf-2017'

          }
      }
    stage ('Test Connectivity'){
      steps {
        ansiblePlaybook colorized: true, inventory: '${WORKSPACE}/ansible/inventory/lab/hosts', playbook: '${WORKSPACE}/ansible/test.yml', sudoUser: null
      }
    }
  }
}
