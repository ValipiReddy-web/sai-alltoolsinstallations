
Update your POM.xml file
You will be finding the following code in pom.xml.
Go to pom.xml add the below lines :

<distributionManagement>
    <repository>
        <id>central</id>
        <name>instance-1-releases</name>
        <url>http://34.125.235.138:8081/artifactory/Bioscope</url>
    </repository>
    <snapshotRepository>
        <id>central</id>
        <name>instance-1-snapshots</name>
        <url>http://34.125.235.138:8081/artifactory/Bioscope</url>
    </snapshotRepository>
</distributionManagement>




Go to conf/setting.xml file add the username and password : 

 <servers>
    <server>
      <id>central</id>
      <username>admin</username>
      <password>Saanvi1986**</password>
    </server>
    


Mvn clean install
Mvn deploy
