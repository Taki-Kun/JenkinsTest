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
    agent {
        node {
            label 'master'
            customWorkspace "workspace/${JOB_NAME.replace('%2F', '/')}"
        }
    }

    environment {
        LANG = "C.UTF-8"
        LC_ALL = "en_US.UTF-8"
        LANGUAGE = "en_US.UTF-8"
        // HOME = "/Users/mac"
    }

    stages {
        stage('test') {
            steps {
                sh "env"
                sh "ls ${JENKINS_HOME}/"
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
