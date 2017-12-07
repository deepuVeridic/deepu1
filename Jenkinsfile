properties([[$class: 'GithubProjectProperty', displayName: '', projectUrlStr: 'https://github.com/deepuVeridic/deepu1.git'], pipelineTriggers([githubPush()])])
pipeline {
	agent any
	parameters {
		string(name: 'Branch', defaultValue: 'default', description: 'Select which branch you want to select')
		booleanParam(name: 'Rebuild_Database', defaultValue: true, description: 'Should we rebuild the database')
		booleanParam(name: 'Deploy', defaultValue: true, description: 'Should we deploy this application')
		choice(name: 'Environment', choices: 'Integration\nAcive\nInactive' , description: 'use for postgress.sh and code deployment')
	}
	stages {
		stage('Example') {
			steps {
				echo "Hello ${params.Branch}"
				echo "Hello ${params.Rebuild_Database}"
				echo "Hello ${params.Deploy}"
				echo "Hello ${params.Environent}"
			}
		}
	}
}
