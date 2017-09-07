pipeline {
  agent any
  stages {
    stage('Git Clone') {
      steps {
        rocketSend channel: 'general', message: 'Config Deploy Started'
        git branch: 'master', url: 'https://github.com/ArctiqTeam/ansiblefest-sf-2017'

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
      ansiblePlaybook inventory: '${WORKSPACE}/ansible/inventory/jenkins/hosts', playbook: '${WORKSPACE}/ansible/test.yml', sudoUser: null
      }
    }
    stage ('Configure OSPF'){
      steps {
      ansiblePlaybook inventory: '${WORKSPACE}/ansible/inventory/jenkins/hosts', playbook: '${WORKSPACE}/ansible/configure.yml', sudoUser: null
      }
    }
   stage ('Build Complete'){
   steps{
   rocketSend attachments: [[audioUrl: '', authorIcon: '', authorName: '', color: '', imageUrl: '', messageLink: '', text: '', thumbUrl: '', title: 'lastBuild ', titleLink: 'http://127.0.0.1:8080/job/ansiblefest-sf-2017/job/master/lastBuild/', titleLinkDownload: '', videoUrl: '']], channel: 'general', message: 'Config Deploy Finised'
   }
   }

  }
}
