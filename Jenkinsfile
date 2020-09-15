pipeline {
	agent any
	stages {
		stage('nugget restore'){
			steps{
				 echo "nugget restoring packages"
		         	bat 'C:/tools/nuget.exe  restore  src/SmartStoreNet.sln'
				
					}
				}
				stage('Build') {
    					steps {
                                        echo " building the project  "
						bat "\"${tool 'MSBuild'}\" src/SmartStoreNet.sln / /t:clean /t:build /p:Configuration=Release /p:Platform=\"Any CPU\" "




					}
				}
			}
}

