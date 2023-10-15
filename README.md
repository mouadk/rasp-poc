# rasp-agent

This repository contains a proof-of-concept (PoC) for a RASP (Runtime Application Self-Protection) agent. Java Virtual Machine (JVM) RASP agents are designed to be executed alongside a JVM to guard sensitive sinks.

First, navigate to the rasp-agent directory:

```
cd rasp-agent
```

Then compile and package the agent using Maven:

```
mvn clean package
```

I've included a PoC for Spring Cloud SpEL injection to validate the capabilities of the RASP agent.
To test:

Run your application with the VM option pointing to the agent JAR:

```
$pwd/rasp-agent/target/rasp-agent-1.0-SNAPSHOT.jar
```
Execute the exploit.sh script to initiate the exploit.

If successful, you should receive a failure message resembling:

```
com.applicationsec.RASPSecurityException: Commands :[open, -a, Calculator] has been blocked by RASP
```
