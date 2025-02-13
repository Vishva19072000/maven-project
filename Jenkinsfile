pipeline
{
agent any
stages
{
  stage ('scm checkout')
   {steps {git 'https://github.com/Vishva19072000/maven-project.git' }}

  stage ('Validate')
  {steps { withMaven(globalMavenSettingsConfig: '', jdk: 'JAVA_HOME', maven: 'MVN_HOME', mavenSettingsConfig: '', traceability: true) {
    sh "mvn validate"
}
  }}

   stage ('Compile')
  {steps { withMaven(globalMavenSettingsConfig: '', jdk: 'JAVA_HOME', maven: 'MVN_HOME', mavenSettingsConfig: '', traceability: true) {
    sh "mvn Compile"
}
  }}

  stage ('Package')
  {steps { withMaven(globalMavenSettingsConfig: '', jdk: 'JAVA_HOME', maven: 'MVN_HOME', mavenSettingsConfig: '', traceability: true) {
    sh "mvn  clean Package"
}
  }}

}
}


