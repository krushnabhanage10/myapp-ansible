pipeline{
    agent{
        label "ansible-master"
    }
    stages{
        stage("Requirement Gathering - Cloning Repo"){
            steps{
                git 'https://github.com/krushnabhanage10/myapp-ansible.git'
            }
        }
        stage("Run Playbook"){
            steps{
                ansiblePlaybook become: true, installation: 'ansible', inventory: 'dev.inv', playbook: 'apache.yml'
            }
        }
    }
}
