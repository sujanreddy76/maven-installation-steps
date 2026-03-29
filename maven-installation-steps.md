# Maven Installation Guide

## 1) Install OpenJDK 17

Navigate to the `/opt` directory and download OpenJDK 17:

```bash
cd /opt
wget https://download.java.net/java/GA/jdk17.0.2/dfd4a8d0985749f896bed50d7138ee7f/8/GPL/openjdk-17.0.2_linux-x64_bin.tar.gz
````

Extract the downloaded archive:

```bash
tar xvf openjdk-17.0.2_linux-x64_bin.tar.gz
```

Move the extracted JDK to a permanent location:

```bash
sudo mv jdk-17.0.2/ /opt/jdk-17
```

---

## 2) Install Maven 3.8.9

Download Maven:

```bash
cd /opt
wget https://dlcdn.apache.org/maven/maven-3/3.8.9/binaries/apache-maven-3.8.9-bin.tar.gz
```

Extract the Maven archive:

```bash
tar -xzvf apache-maven-3.8.9-bin.tar.gz
```

---

## 3) Set Up Environment Variables

To make Java and Maven available system-wide:

Open the profile file:

```bash
sudo vi /etc/profile
```

Add the following lines at the bottom:

```bash
export JAVA_HOME=/opt/jdk-17
export PATH=$PATH:$JAVA_HOME/bin

export M2_HOME=/opt/apache-maven-3.8.9
export PATH=$PATH:$M2_HOME/bin
```

Apply the changes:

```bash
source /etc/profile
```

---

## ✅ Verify Installation

```bash
java -version
mvn -version
```

