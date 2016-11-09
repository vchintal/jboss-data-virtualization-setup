## JBoss Data Virtualization Setup Automation

This repo is designed to help automate/speed up setup of **JBoss Data Virtualization** and its related components in a development environment or for a workshop setting.

### Prerequisites

* [Java JDK](http://www.oracle.com/technetwork/java/javase/downloads/jdk8-downloads-2133151.html), preferably 1.8 
* **JAVA_HOME** environment variable set
* **JAVA_HOME\bin** is on the PATH
* All of the necessary binaries downloaded. Refer to [binaries] (binaries/README.md) for download locations and filename/versions.
* EAP patches downloaded. Refer to the [patches] (patches/README.md) for download locations and filename/versions.
* Familiarity with Apache Ant

### Running the setup

#### Running the setup with EAP patches downloaded

Run the following command in the root folder of the repo by ideally cd'ing (change directory) into it.

```sh
./install.sh 
```

or on Windows 

```bat
install.bat
```

#### Running the setup without EAP patches downloaded

If you are downloading the binaries from [http://developers.redhat.com/products/](http://developers.redhat.com/products/), you don't have access to EAP patches. So assuming you are okay with missing EAP patches you can still run the setup with the following command.

Run the following command in the root folder of the repo by ideally cd'ing (change directory) into it.

```sh
./install.sh -DskipPatching
```

or on Windows 

```bat
install.bat -DskipPatching
```

### Important Notes

* The password for all accounts on the JDV runtime is `redhat1!`. Refer to **build.properties**.
