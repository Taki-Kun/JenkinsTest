#!/usr/bin/env groovy

def token
node {
    withCredentials([sshUserPrivateKey(credentialsId: '846a4a04-da8e-4909-a5ff-eef9004b1eef', keyFileVariable: 'SSH_KEY_FOR_ABC', passphraseVariable: '', usernameVariable: '')]) {
        token = env.SSH_KEY_FOR_ABC
    }
}
echo "My ssh private key is '${token}'"

// @Library('github.com/Taki-Kun/testJenkinsSharedLibraries@master') _
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

def dummy
clientsNode {
    ws ('pipelines'){
        git 'https://github.com/fabric8io/fabric8-pipeline-library.git'
    }
}

