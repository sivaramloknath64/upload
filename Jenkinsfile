pipeline {
	agent any
	stages {
		
		
				stage('building ') {
    					steps {
                                        echo " building the project   "
						bat "\"${tool 'MSBuild'}\" src/SmartStoreNet.sln  /p:DeployOnBuild=true /p:DeployDefaultTarget=WebPublish /p:WebPublishMethod=FileSystem /p:SkipInvalidConfigurations=true /clean /t:build /p:Configuration=Release  /p:Platform=\"Any CPU\"  /p:publishUrl=c:\\y"





					}
				}
			}
}

