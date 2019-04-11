node {
	stage('Checkout') {
        	sh 'set -o pipefail && xcodebuild -project "JenkinsAutomationTests.xcodeproj" -scheme "Testing" -sdk "iphonesimulator12.2" -destination "platform=iOS Simulator,OS=latest,name=iPhone 7" test -only-testing:"JenkinsAutomationTestsUITests/JenkinsAutomationTestsUITests" -resultBundlePath TestResults | xcpretty'
	    }
        post {
	    always {
		sh 'xchtmlreport -r TestResults'
	    }
        }
}