node {
sh 'echo HelloWorld'

stage('Checkout') {
        checkout([$class: 'GitSCM', branches: [[name: '*/$branch']], 
            doGenerateSubmoduleConfigurations: false, extensions: [], submoduleCfg: [], 
            userRemoteConfigs: []])
    }
stage('MyCustom') {
       sh 'fastlane custom_lane'
   }
}