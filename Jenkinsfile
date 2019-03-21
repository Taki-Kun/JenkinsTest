#!/usr/bin/env groovy

library(
    identifier: 'github.com/Taki-Kun/testJenkinsSharedLibraries2@master',
    changelog: false,
    retriever: modernSCM(
        [
            $class: 'GitSCMSource',
            credentialsId: 'jenkins-global-ssh-key',
            remote: 'git@github.com:Taki-Kun/testJenkinsSharedLibraries.git'
            // traits: [
            //     [
            //         $class: 'jenkins.plugins.git.traits.BranchDiscoveryTrait'
            //     ]
            // ]
        ]
    )
)

def dummy
clientsNode {
    ws ('pipelines'){
        git 'https://github.com/fabric8io/fabric8-pipeline-library.git'
    }
}

