#!/usr/bin/env groovy

library(
    identifier: 'github.com/Taki-Kun/testJenkinsSharedLibraries2@master',
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

