node {
	sh 'echo HelloWorld'

	stage('Checkout') {
        	checkout([$class: 'GitSCM', branches: [[name: '*/$branch']], 
	            doGenerateSubmoduleConfigurations: false, extensions: [], submoduleCfg: [], 
        	    userRemoteConfigs: [[credentialsId:'/$githubToken' , url: 'https://github.com/jordan-romeroporter-earnin/JenkinsRemote.git']]])
	    }
	stage('MyCustom') {
       		sh 'fastlane custom_lane'
	}
}