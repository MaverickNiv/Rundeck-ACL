

pipeline {
    agent { label 'ecs-worker-default' }
	stages {
		stage('Add EC2 instance to inventory file') {
		    steps {   
			sh "echo '${env.address}' >> JenkinsHosts.ini"
			}
		}
		stage('Run ansible playbook') {
			environment {
                SSH_CREDS = credentials('slave-node')
            	}
		    steps { 
			sh 'ansible-playbook jenkins_install_playbook.yml -i JenkinsHosts.ini --private-key $SSH_CREDS --ssh-common-args="-o StrictHostKeyChecking=no"'
			}
		}
	 }
}
