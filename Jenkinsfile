#!/usr/bin/env groovy

@Library('github.com/Taki-Kun/testJenkinsSharedLibraries@master') _
/*
library(
    identifier: 'github.com/Taki-Kun/testJenkinsSharedLibraries@master',
    changelog: false,
    retriever: modernSCM(
        [
            $class: 'GitSCMSource',
            credentialsId: '846a4a04-da8e-4909-a5ff-eef9004b1eef',
            remote: 'git@github.com:Taki-Kun/testJenkinsSharedLibraries.git'
        ]
    )
)
*/

def dummy
iOSNode(label: 'mac-mini5') {
    ws ('pipelines'){
        git 'https://github.com/fabric8io/fabric8-pipeline-library.git'
    }
}

