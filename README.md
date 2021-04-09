# **sybond** JMeter Simulator

This repository to contain all configurations, script, and library, to be used with Apache JMeter to support various functionality of (not limited to) payment simulator.

Currently the repository contain following configurations:

|Messaging|Type|Description|
|---|:---:|:---|
|ISO8583| Sender, Receiver|Available|
|JSON|Sender, Receiver|TO-DO|

## How to
To use simulator you need working [Apache JMeter](https://jmeter.apache.org/) running in your machine.

### Installing ISO8583 Plugin
To support ISO8583 messaging format within JMeter, you need to install following module:

1. Copy the [jmeter-iso8583 jar file](https://github.com/tilln/jmeter-iso8583/releases/download/1.1/jmeter-iso8583-1.1.jar) into JMeter's `lib/ext` directory.
2. Copy the following dependencies into JMeter's `lib` directory (and optionally remove older versions of any of those jar files):
    * [org.jpos / jpos](https://search.maven.org/remotecontent?filepath=org/jpos/jpos/2.1.4/jpos-2.1.4.jar)
    * [org.bouncycastle / bcprov-jdk15on](https://search.maven.org/remotecontent?filepath=org/bouncycastle/bcprov-jdk15on/1.64/bcprov-jdk15on-1.64.jar)
    * [org.bouncycastle / bcpg-jdk15on](https://search.maven.org/remotecontent?filepath=org/bouncycastle/bcpg-jdk15on/1.64/bcpg-jdk15on-1.64.jar)
    * [org.jdom / jdom2](https://search.maven.org/remotecontent?filepath=org/jdom/jdom2/2.0.6/jdom2-2.0.6.jar)
    * [org.osgi / org.osgi.core](https://search.maven.org/remotecontent?filepath=org/osgi/org.osgi.core/6.0.0/org.osgi.core-6.0.0.jar)
    * [commons-cli / commons-cli](https://search.maven.org/remotecontent?filepath=commons-cli/commons-cli/1.4/commons-cli-1.4.jar)
    * [org.yaml / snakeyaml](https://search.maven.org/remotecontent?filepath=org/yaml/snakeyaml/1.26/snakeyaml-1.26.jar)
    * [org.hdrhistogram / HdrHistogram](https://search.maven.org/remotecontent?filepath=org/hdrhistogram/HdrHistogram/2.1.12/HdrHistogram-2.1.12.jar)
    * [org.javatuples / javatuples](https://search.maven.org/remotecontent?filepath=org/javatuples/javatuples/1.2/javatuples-1.2.jar)
3. Copy Custom JPOS module from [here](https://github.com/sybond/sybond-JMeter-Simulator/tree/master/lib) into JMeter's `lib` directory.
4. Restart JMeter

To configure ISO8583 simulator you can read [here](iso8583-Sampler).
