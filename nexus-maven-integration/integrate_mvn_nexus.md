1) Update your POM.xml file

You will be finding the following code in pom.xml.

-------------------------------------------------------------------
    <distributionManagement>
        <repository>
            <id>deployment</id>
            <name>Internal Releases</name>
            <url>http://35.190.142.49:8081/repository/maven-releases/</url>
        </repository>
        <snapshotRepository>
            <id>deployment</id>
            <name>Internal Snapshot Releases</name>
            <url>http://35.190.142.49:8081/repository/maven-snapshots/</url>
        </snapshotRepository>
    </distributionManagement>

-------------------------------------------------------------------

Update this to your nexus URL .
Note : Only IP address will change.

2) Update settings.xml file in maven.

Assuming maven installed under /opt

# cd /opt/apache-maven-3.3.9/conf
# vim settings.xml 

>>> You can find a line as "</servers>". Add the following content just before that line.

    <server>
      <id>deployment</id>
      <username>admin</username>
      <password>admin123</password>
    </server>

	
Copy as it is and save and quit.


Now use the following maven cycle.

# mvn clean package deploy
