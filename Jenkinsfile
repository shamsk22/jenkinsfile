pipeline {
  agent any
  parameters {
    choice(name: 'Namespace_Choice',
      choices: 'Merch-pl-planning-ci\nMerch-pl-planning-stage-3\nMerch-pl-planning-stress-3\nMerch-pl-planning-preprod',
      description: 'Select the required Namespace')
	booleanParam(name: 'kap-admin-service',
      	defaultValue: false,
      	description: 'Select sevice to build')
	booleanParam(name: 'kap-assortment-service',
      	defaultValue: false,
      	description: 'Select service to build')
       string(name: 'All-MAP-Services',
      defaultValue: 'kap-admin-service,kap-assortment-service',
      description: 'Dafault serviced')
  }
  stages {
    stage('Example') {
      steps {
        echo 'Hello World!'
        echo "Trying: ${params.Namespace_Choice}"
        echo "Build admin: ${params.kap_admin_service}"
	echo "Build Assortment: ${params.kap_assortment_service}"
	echo "The DJ says: ${params.All_MAP_Services}"
      }
    }
  }
}
