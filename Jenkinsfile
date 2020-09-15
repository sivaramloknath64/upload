pipeline {
	agent any
	stages {
		
		
		
		
		
		
		
		
				stage('Nugget Restore and bulding ') {
    					steps {
                                        echo " Restoring and building the project   "
						bat 'C:/tools/nuget.exe  restore  src/SmartStoreNet.sln'
						bat "\"${tool 'MSBuild'}\" src/SmartStoreNet.sln  /p:DeleteExistingFiles=True /p:DeployOnBuild=true /p:DeployDefaultTarget=WebPublish /p:WebPublishMethod=FileSystem /p:SkipInvalidConfigurations=true /t:build /p:Configuration=Release /p:Platform=\"Any CPU\"  /p:publishUrl=c:\\iis"





					}
				}
			}
}

