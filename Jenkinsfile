pipeline {
  agent any
  stages {
    stage('Git Clone') {
      steps {
        rocketSend channel: 'general', message: 'START RESET'
        git branch: 'reset', url: 'https://github.com/ArctiqTeam/ansiblefest-sf-2017'

          }
      }
    stage ('Clean up local env'){
      steps {
        sh '''#!/bin/bash
        rm -rf /root/.ansible/*'''
      }
    }
    stage ('Reset Router Configs'){
      steps {
      ansiblePlaybook inventory: '${WORKSPACE}/ansible/inventory/jenkins/hosts', playbook: '${WORKSPACE}/ansible/reset.yml', sudoUser: null
      rocketSend channel: 'general', message: 'RESET COMPLETE'
      }
    }
  }
}
