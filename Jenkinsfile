node('DOTNETCORE') {
	stage('SCM') {
			check([$class: 'GitSCM', branches: [[name: '*/master']], doGenerateSubmoduleConfigurations: false,
			extensions: [], submoduleCfg: [], userRemoteConfigs: [[url: 'https://github.com/axelluccin/Jenkins-docker-Test']]])
	}
	stage('Build'){
		sh 'dotnet build ConsoleApp1'
	}
	stage('Test'){
		echo 'Execute unit tests'
	}
	stage('Package'){
		echo 'Zip it up'
	}
	stage('Deploy'){
		echo 'Push to deployment'
	}
}
