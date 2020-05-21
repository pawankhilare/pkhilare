#!/usr/bin/env groovy
pipeline{
	agent any


	stages {
		stage('Build') {
		steps {
		echo "This is my cft build one"
		step([$class: 'AnsibleAdHocCommandBuilder']) (
		hostPattern: localhost,
		module: command,
		command: cat /etc/hosts
		)
		}
	}
}
}
