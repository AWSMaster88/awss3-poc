Installing npm 
1. run

curl -o- https://raw.githubusercontent.com/nvm-sh/nvm/v0.39.5/install.sh | bash

2. Run
. ~/.nvm/nvm.sh
3. Run: Installing Node.js also installs the Node Package Manager (npm), so you can install additional modules as needed.

nvm install --lts
4. Test that Node.js is installed and running correctly by typing the following at the command line.

node -e "console.log('Running Node.js ' + process.version)"

5. Install git

sudo yum -y install git




To generate a Software Bill of Materials (SBOM) for a Node.js project using CycloneDX, you can follow these steps:

Install CycloneDX CLI:

First, you need to install the CycloneDX CLI tool. You can install it using npm (Node Package Manager):

bash
Copy code
npm install --global @cyclonedx/cyclonedx-npm
Navigate to Your Node.js Project:

Open your terminal and navigate to the root directory of your Node.js project.

Generate CycloneDX SBOM:

Run the following command to generate a CycloneDX SBOM for your Node.js project:

bash
Copy code
npm install 
cyclonedx-npm --output-file “bom.json”
This command will analyze your project's dependencies and generate an XML-based CycloneDX SBOM in the sbom.xml file.
pipy 
Installing pip in linux
Run 
curl -O https://bootstrap.pypa.io/get-pip.py
Run to get latest pip
   python3 get-pip.py --user
GitHub project: https://github.com/CycloneDX/cyclonedx-python
Slack channel: https://cyclonedx.slack.com/archives/CVA0QJEVA
Install the CycloneDX python plugin to your python project by running:
with pip:
pip install cyclonedx-bom
        2.  Execute the following to clone the python repository
        git clone “url-python-project”
        3.  Switch to the root folder of the project
         cd  “name-of-the-python-repo”
      4. Run the below command:
for pip:
cyclonedx-py -r -F --format json -o bom.json
Maven
Installing java
Download rpm package
 sudo rpm --import https://yum.corretto.aws/corretto.key 
 sudo curl -L -o /etc/yum.repos.d/corretto.repo https://yum.corretto.aws/corretto.repo

Install openjdk
sudo yum install -y java-1.8.0-amazon-corretto-devel

Installing maven
The following are instructions for installing Apache Maven and Java 8 on an Amazon EC2 instance. To Install Apache Maven and Java 8 on your EC2 instance
Connect to your Amazon EC2 instance with an SSH client.
Install Apache Maven on your EC2 instance. First, enter the following to add a repository with a Maven package.
sudo wget https://repos.fedorapeople.org/repos/dchen/apache-maven/epel-apache-maven.repo -O /etc/yum.repos.d/epel-apache-maven.repo
Enter the following to set the version number for the packages.
sudo sed -i s/\$releasever/6/g /etc/yum.repos.d/epel-apache-maven.repo
Then you can use yum to install Maven.
sudo yum install -y apache-maven
The Gremlin libraries require Java 8. Enter the following to install Java 8 on your EC2 instance.
sudo yum install java-1.8.0-devel
Enter the following to set Java 8 as the default runtime on your EC2 instance.
sudo /usr/sbin/alternatives --config java
When prompted, enter the number for Java 8.
Enter the following to set Java 8 as the default compiler on your EC2 instance.
sudo /usr/sbin/alternatives --config javac
When prompted, enter the number for Java 8.
Configuring cyclonedx for maven project

GitHub project: https://github.com/CycloneDX/cyclonedx-maven-plugin
Slack channel: https://cyclonedx.slack.com/archives/CVCKP34A2
Add the CycloneDX Maven plugin to your pom.xml:
maven
<plugins>
    <plugin>
        <groupId>org.cyclonedx</groupId>
        <artifactId>cyclonedx-maven-plugin</artifactId>
        <version>2.7.3</version>
    </plugin>
</plugins>
Or use 
<!-- uses default configuration -->
<plugins>
    <plugin>
        <groupId>org.cyclonedx</groupId>
        <artifactId>cyclonedx-maven-plugin</artifactId>
        <executions>
            <execution>
                <phase>package</phase>
                <goals>
                    <goal>makeAggregateBom</goal>
                </goals>
            </execution>
        </executions>
    </plugin>
</plugins>
—-------
<!-- https://mvnrepository.com/artifact/org.cyclonedx/cyclonedx-maven-plugin -->
<dependency>
    <groupId>org.cyclonedx</groupId>
    <artifactId>cyclonedx-maven-plugin</artifactId>
    <version>2.7.9</version>
</dependency>






There are more configuration options (see the GitHub project for details). But the default should suffice for most cases.
Run the below command:
mvn org.cyclonedx:cyclonedx-maven-plugin:makeBom

Find the CycloneDX SBOM JSON under ./target
References
https://docs-vsm.leanix.net/docs/setting-up-the-cyclonedx-sbom-generation#npm



Script to convert bom file to excel

Ensure that pip is installed in your machine
Install python package for document using below command
pip install pandas openpyxl

Create a file called bomExcel.py and copy the below code snippet


import pandas as pd

# Read the .bom file (change the filename as needed)
input_file = 'bom.json'
df = pd.read_csv(input_file, delimiter='\t')  # You may need to adjust the delimiter

# Create a Pandas DataFrame and process your data if needed

# Write the DataFrame to an Excel file
output_file = 'output.xlsx'
df.to_excel(output_file, index=False)

print(f'File "{output_file}" has been created.')



Execute python3 bomExcel.py
