pipeline
{
	agent any
	stages
	{
		stage('Build Application')
		{
			steps
			{
				bat 'mvn clean install'
			}
		}
		stage('Deploy application to cloudhub')
		{
			steps
			{
				bat 'mvn package deploy -DmuleDeploy'
			}
		}
	}
}