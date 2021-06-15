pipeline
{
	agent any
	stages
	{
		stage('Build Application')
		{
			steps
			{
				bat 'mvn clean install -DskipTests=true'
			}
		}
		stage('Munit Testing Application')
		{
			steps
			{
				bat 'mvn test'
			}
		}
		stage('Deploy application to cloudhub')
		{
			steps
			{
				bat 'mvn package deploy -DmuleDeploy -DskipTests=true'
			}
		}
	}
}