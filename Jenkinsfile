pipeline {
    agent any

    parameters {
        // booleanParam, choice, file, text, password, run, or string
        string(defaultValue: "https://rundeck.epmtest.cyberarkcloud.com/", description: 'Rundeck URL for Given Team', name: 'url')
        string(defaultValue: "", description: 'Rundeck Token for Given Team', name: 'token')
        string(defaultValue: "Policy1", description: 'Name of the New ACL Policy', name: 'policyName')
        string(defaultValue: "", description: 'Name of the Project we Wish to Alter ACL Policies for', name: 'projectName')
        string(defaultValue: "", description: 'What ACL Policy Role do you wish to Apply', name: 'policyRole')
    }

    stages {
        stage("foo") {
            steps {
                echo "rundeck_url: ${params.url}"
                echo "rundeck_token: ${params.token}"
                echo "policy_name: ${params.policyName}"
                echo "project_name: ${params.projectName}"
                echo "policy_role: ${params.policyRole}"
            }
        }
    }
}
