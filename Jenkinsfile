pipeline {
	agent any
	stages {
		
		stage('cleaning the path'){
		
			steps{
			
			sh "/p:DeleteExistingFiles=True /p:publishUrl=c:\\yes"
			}
		
			
		}
		
		
		stage('Nugget restore packages') {
		
			steps{
			
				echo "Restoring  the packages "
				bat 'C:/tools/nuget.exe  restore  src/SmartStoreNet.sln'
			}
			
			}
				stage('building ') {
    					steps {
                                        echo " building the project   "
						bat 'C:/tools/nuget.exe  restore  src/SmartStoreNet.sln'
						bat "\"${tool 'MSBuild'}\" src/SmartStoreNet.sln  /p:DeployOnBuild=true /p:DeployDefaultTarget=WebPublish /p:WebPublishMethod=FileSystem /p:SkipInvalidConfigurations=true /t:build /p:Configuration=Release /p:Platform=\"Any CPU\"  /p:publishUrl=c:\\yes"





					}
				}
			}
}

