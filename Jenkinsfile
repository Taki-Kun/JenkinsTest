#!/usr/bin/env groovy

import org.jenkinsci.plugins.workflow.libs.Library


@Library('github.com/Taki-Kun/testJenkinsSharedLibraries@master') _
/*
library(
    identifier: 'github.com/Taki-Kun/testJenkinsSharedLibraries@master',
    // changelog: false,
    retriever: modernSCM(
        [
            $class: 'GitSCMSource',
            credentialsId: 'ssh-git-credentials-id',
            remote: 'git@github.com:Taki-Kun/testJenkinsSharedLibraries.git'
        ]
    )
)
*/

pipeline {
    agent 'mac-mini3'

    stages {
        stage('test') {
            steps {
                echo "${PATH}"
                sh "pwd"
            }
        }
    }
}

/*
def dummy
// binaryNode(label: 'mac-book-pro-1') {
binaryNode(argone: 'one') {
    ws ("workspace/${env.JOB_NAME}/pipelines".replace('%2F', '_')) {
        git 'https://github.com/fabric8io/fabric8-pipeline-library.git'
        // checkoutGeneralSCM(browser: 'github', url: 'https://github.com/Taki-Kun/testJenkinsSharedLibraries.git', name: 'master')
    }
}
*/
