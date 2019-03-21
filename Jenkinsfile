#!/usr/bin/env groovy

node {
    withCredentials([sshUserPrivateKey(credentialsId: '846a4a04-da8e-4909-a5ff-eef9004b1eef', keyFileVariable: 'SSH_KEY_FOR_ABC', passphraseVariable: '', usernameVariable: '')]) {
        echo "My ssh private key is '${SSH_KEY_FOR_ABC}'"
    }
}

// @Library('github.com/Taki-Kun/testJenkinsSharedLibraries@master') _
library(
    identifier: 'git@github.com:Taki-Kun/testJenkinsSharedLibraries.git@master',
    changelog: false,
    retriever: modernSCM(
        [
            $class: 'GitSCMSource',
            credentialsId: '846a4a04-da8e-4909-a5ff-eef9004b1eef',
            remote: 'git@github.com:Taki-Kun/testJenkinsSharedLibraries.git'
        ]
    )
)

def dummy
clientsNode {
    ws ('pipelines'){
        git 'https://github.com/fabric8io/fabric8-pipeline-library.git'
    }
}

