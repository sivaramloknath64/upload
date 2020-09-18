pipeline {
	agent any
	stages {
		
		
				stage('building ') {
    					steps {
                                        echo " building the project   "
						
						bat "\"${tool 'MSBuild'}\" src/SmartstoreNet.sln /p:PublishUrl="'bin\Release\PublishOutput'" /p:DeployOnBuild=true /p:Configuration=Release /p:WebPublishMethod=FileSystem /p:DeployTarget=WebPublish /p:AutoParameterizationWebConfigConnectionStrings=false /p:SolutionDir="'c:\\cnc'"





					}
				}
			}
}









