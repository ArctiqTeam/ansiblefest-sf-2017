pipeline {
  agent any
  stages {
    stage('Git Clone') {
      steps {
        git branch: 'lab', url: 'https://github.com/ArctiqTeam/ansiblefest-sf-2017'

          }
      }
    stage ('Clean up local env'){
      steps {
        sh '''#!/bin/bash
        rm -rf /root/.ansible/*'''
      }
    }
    stage ('Test Connectivity'){
      steps {
      ansiblePlaybook colorized: true, extras: inventory: '${WORKSPACE}/ansible/inventory/jenkins/hosts', playbook: '${WORKSPACE}/ansible/test.yml', sudoUser: null
      }
    }
  }
}
