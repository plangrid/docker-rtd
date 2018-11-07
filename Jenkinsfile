#!/bin/groovy
node {

    stage('checkout') {
        // Clone repo and subtree
        checkout([
            $class: 'GitSCM',
            gitTool: 'native git',
            branches: scm.branches,
            env.PROJECT_NAME='docs',
            env.GIT_BRANCH = env.BRANCH_NAME,
            doGenerateSubmoduleConfigurations: false,
            extensions: [
                [$class: 'SubmoduleOption', disableSubmodules: false, parentCredentials: false, recursiveSubmodules: true, reference: '', trackingSubmodules: false]
            ],
            userRemoteConfigs: scm.userRemoteConfigs
        ])
    }

    stage('Build Docker') {
            ansiColor('xterm') {
                retry(3) {
                    sh '/opt/plangrid/build-tools/bin/build-docker'
                }
            }
        }
        stage('Push Docker') {
            ansiColor('xterm') {
                retry(3) {
                    sh '/opt/plangrid/build-tools/bin/push-docker'
                }
            }
        }
}
