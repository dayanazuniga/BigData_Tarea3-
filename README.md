# BigData_Tarea3-
Código de la tarea 3 
Ingreso con el usuario vboxuser 
Contraseña bigdata
Dataset utilizado:
https://www.datos.gov.co/resource/mcec-87by.csv

login as: vboxuser
vboxuser@192.168.0.110's password:
Welcome to Ubuntu 22.04.5 LTS (GNU/Linux 5.15.0-173-generic x86_64)

 * Documentation:  https://help.ubuntu.com
 * Management:     https://landscape.canonical.com
 * Support:        https://ubuntu.com/pro

 System information as of Sun Apr  5 08:38:40 PM UTC 2026

  System load:  1.32               Processes:               118
  Usage of /:   29.9% of 31.32GB   Users logged in:         1
  Memory usage: 6%                 IPv4 address for enp0s3: 192.168.0.110
  Swap usage:   0%

 * Strictly confined Kubernetes makes edge and IoT secure. Learn how MicroK8s
   just raised the bar for easy, resilient and secure K8s cluster deployment.

   https://ubuntu.com/engage/secure-kubernetes-at-the-edge

Expanded Security Maintenance for Applications is not enabled.

13 updates can be applied immediately.
To see these additional updates run: apt list --upgradable

Enable ESM Apps to receive additional future security updates.
See https://ubuntu.com/esm or run: sudo pro status


Last login: Fri Apr  3 23:29:50 2026 from 192.168.0.103
vboxuser@BIGDATA:~$ python3 kafka_producer.py
Traceback (most recent call last):
  File "/home/vboxuser/kafka_producer.py", line 13, in <module>
    producer = KafkaProducer(bootstrap_servers=['localhost:9092'],
  File "/home/vboxuser/.local/lib/python3.10/site-packages/kafka/producer/kafka.py", line 485, in __init__
    client = self.config['kafka_client'](
  File "/home/vboxuser/.local/lib/python3.10/site-packages/kafka/client_async.py", line 262, in __init__
    self.config['api_version'] = self.check_version()
  File "/home/vboxuser/.local/lib/python3.10/site-packages/kafka/client_async.py", line 1076, in check_version
    raise Errors.NoBrokersAvailable()
kafka.errors.NoBrokersAvailable: NoBrokersAvailable
vboxuser@BIGDATA:~$ cd ~/kafka_2.12-3.9.2
vboxuser@BIGDATA:~/kafka_2.12-3.9.2$ ./bin/zookeeper-server-start.sh config/zookeeper.properties
[2026-04-05 20:40:16,519] INFO Reading configuration from: config/zookeeper.properties (org.apache.zookeeper.server.quorum.QuorumPeerConfig)
[2026-04-05 20:40:16,523] WARN config/zookeeper.properties is relative. Prepend ./ to indicate that you're sure! (org.apache.zookeeper.server.quorum.QuorumPeerConfig)
[2026-04-05 20:40:16,534] INFO clientPortAddress is 0.0.0.0:2181 (org.apache.zookeeper.server.quorum.QuorumPeerConfig)
[2026-04-05 20:40:16,535] INFO secureClientPort is not set (org.apache.zookeeper.server.quorum.QuorumPeerConfig)
[2026-04-05 20:40:16,535] INFO observerMasterPort is not set (org.apache.zookeeper.server.quorum.QuorumPeerConfig)
[2026-04-05 20:40:16,536] INFO metricsProvider.className is org.apache.zookeeper.metrics.impl.DefaultMetricsProvider (org.apache.zookeeper.server.quorum.QuorumPeerConfig)
[2026-04-05 20:40:16,540] INFO autopurge.snapRetainCount set to 3 (org.apache.zookeeper.server.DatadirCleanupManager)
[2026-04-05 20:40:16,541] INFO autopurge.purgeInterval set to 0 (org.apache.zookeeper.server.DatadirCleanupManager)
[2026-04-05 20:40:16,542] INFO Purge task is not scheduled. (org.apache.zookeeper.server.DatadirCleanupManager)
[2026-04-05 20:40:16,542] WARN Either no config or no quorum defined in config, running in standalone mode (org.apache.zookeeper.server.quorum.QuorumPeerMain)
[2026-04-05 20:40:16,545] INFO Log4j 1.2 jmx support not found; jmx disabled. (org.apache.zookeeper.jmx.ManagedUtil)
[2026-04-05 20:40:16,548] INFO Reading configuration from: config/zookeeper.properties (org.apache.zookeeper.server.quorum.QuorumPeerConfig)
[2026-04-05 20:40:16,549] WARN config/zookeeper.properties is relative. Prepend ./ to indicate that you're sure! (org.apache.zookeeper.server.quorum.QuorumPeerConfig)
[2026-04-05 20:40:16,550] INFO clientPortAddress is 0.0.0.0:2181 (org.apache.zookeeper.server.quorum.QuorumPeerConfig)
[2026-04-05 20:40:16,551] INFO secureClientPort is not set (org.apache.zookeeper.server.quorum.QuorumPeerConfig)
[2026-04-05 20:40:16,551] INFO observerMasterPort is not set (org.apache.zookeeper.server.quorum.QuorumPeerConfig)
[2026-04-05 20:40:16,552] INFO metricsProvider.className is org.apache.zookeeper.metrics.impl.DefaultMetricsProvider (org.apache.zookeeper.server.quorum.QuorumPeerConfig)
[2026-04-05 20:40:16,552] INFO Starting server (org.apache.zookeeper.server.ZooKeeperServerMain)
[2026-04-05 20:40:16,576] INFO ServerMetrics initialized with provider org.apache.zookeeper.metrics.impl.DefaultMetricsProvider@4387b79e (org.apache.zookeeper.server.ServerMetrics)
[2026-04-05 20:40:16,582] INFO ACL digest algorithm is: SHA1 (org.apache.zookeeper.server.auth.DigestAuthenticationProvider)
[2026-04-05 20:40:16,583] INFO zookeeper.DigestAuthenticationProvider.enabled = true (org.apache.zookeeper.server.auth.DigestAuthenticationProvider)
[2026-04-05 20:40:16,589] INFO zookeeper.snapshot.trust.empty : false (org.apache.zookeeper.server.persistence.FileTxnSnapLog)
[2026-04-05 20:40:16,637] INFO  (org.apache.zookeeper.server.ZooKeeperServer)
[2026-04-05 20:40:16,642] INFO   ______                  _                                           (org.apache.zookeeper.server.ZooKeeperServer)
[2026-04-05 20:40:16,642] INFO  |___  /                 | |                                          (org.apache.zookeeper.server.ZooKeeperServer)
[2026-04-05 20:40:16,643] INFO     / /    ___     ___   | | __   ___    ___   _ __     ___   _ __    (org.apache.zookeeper.server.ZooKeeperServer)
[2026-04-05 20:40:16,643] INFO    / /    / _ \   / _ \  | |/ /  / _ \  / _ \ | '_ \   / _ \ | '__| (org.apache.zookeeper.server.ZooKeeperServer)
[2026-04-05 20:40:16,644] INFO   / /__  | (_) | | (_) | |   <  |  __/ |  __/ | |_) | |  __/ | |     (org.apache.zookeeper.server.ZooKeeperServer)
[2026-04-05 20:40:16,644] INFO  /_____|  \___/   \___/  |_|\_\  \___|  \___| | .__/   \___| |_| (org.apache.zookeeper.server.ZooKeeperServer)
[2026-04-05 20:40:16,645] INFO                                               | |                      (org.apache.zookeeper.server.ZooKeeperServer)
[2026-04-05 20:40:16,645] INFO                                               |_|                      (org.apache.zookeeper.server.ZooKeeperServer)
[2026-04-05 20:40:16,646] INFO  (org.apache.zookeeper.server.ZooKeeperServer)
[2026-04-05 20:40:16,775] INFO Server environment:zookeeper.version=3.8.4-9316c2a7a97e1666d8f4593f34dd6fc36ecc436c, built on 2024-02-12 22:16 UTC (org.apache.zookeeper.server.ZooKeeperServer)
[2026-04-05 20:40:16,776] INFO Server environment:host.name=BIGDATA (org.apache.zookeeper.server.ZooKeeperServer)
[2026-04-05 20:40:16,776] INFO Server environment:java.version=11.0.30 (org.apache.zookeeper.server.ZooKeeperServer)
[2026-04-05 20:40:16,776] INFO Server environment:java.vendor=Ubuntu (org.apache.zookeeper.server.ZooKeeperServer)
[2026-04-05 20:40:16,776] INFO Server environment:java.home=/usr/lib/jvm/java-11-openjdk-amd64 (org.apache.zookeeper.server.ZooKeeperServer)
[2026-04-05 20:40:16,777] INFO Server environment:java.class.path=/home/vboxuser/kafka_2.12-3.9.2/bin/../libs/activation-1.1.1.jar:/home/vboxuser/kafka_2.12-3.9.2/bin/../libs/aopalliance-repackaged-2.6.1.jar:/home/vboxuser/kafka_2.12-3.9.2/bin/../libs/argparse4j-0.7.0.jar:/home/vboxuser/kafka_2.12-3.9.2/bin/../libs/audience-annotations-0.12.0.jar:/home/vboxuser/kafka_2.12-3.9.2/bin/../libs/caffeine-2.9.3.jar:/home/vboxuser/kafka_2.12-3.9.2/bin/../libs/commons-beanutils-1.11.0.jar:/home/vboxuser/kafka_2.12-3.9.2/bin/../libs/commons-cli-1.4.jar:/home/vboxuser/kafka_2.12-3.9.2/bin/../libs/commons-collections-3.2.2.jar:/home/vboxuser/kafka_2.12-3.9.2/bin/../libs/commons-digester-2.1.jar:/home/vboxuser/kafka_2.12-3.9.2/bin/../libs/commons-io-2.14.0.jar:/home/vboxuser/kafka_2.12-3.9.2/bin/../libs/commons-lang3-3.18.0.jar:/home/vboxuser/kafka_2.12-3.9.2/bin/../libs/commons-logging-1.3.5.jar:/home/vboxuser/kafka_2.12-3.9.2/bin/../libs/commons-validator-1.10.1.jar:/home/vboxuser/kafka_2.12-3.9.2/bin/../libs/connect-api-3.9.2.jar:/home/vboxuser/kafka_2.12-3.9.2/bin/../libs/connect-basic-auth-extension-3.9.2.jar:/home/vboxuser/kafka_2.12-3.9.2/bin/../libs/connect-json-3.9.2.jar:/home/vboxuser/kafka_2.12-3.9.2/bin/../libs/connect-mirror-3.9.2.jar:/home/vboxuser/kafka_2.12-3.9.2/bin/../libs/connect-mirror-client-3.9.2.jar:/home/vboxuser/kafka_2.12-3.9.2/bin/../libs/connect-runtime-3.9.2.jar:/home/vboxuser/kafka_2.12-3.9.2/bin/../libs/connect-transforms-3.9.2.jar:/home/vboxuser/kafka_2.12-3.9.2/bin/../libs/error_prone_annotations-2.10.0.jar:/home/vboxuser/kafka_2.12-3.9.2/bin/../libs/hk2-api-2.6.1.jar:/home/vboxuser/kafka_2.12-3.9.2/bin/../libs/hk2-locator-2.6.1.jar:/home/vboxuser/kafka_2.12-3.9.2/bin/../libs/hk2-utils-2.6.1.jar:/home/vboxuser/kafka_2.12-3.9.2/bin/../libs/jackson-annotations-2.16.2.jar:/home/vboxuser/kafka_2.12-3.9.2/bin/../libs/jackson-core-2.16.2.jar:/home/vboxuser/kafka_2.12-3.9.2/bin/../libs/jackson-databind-2.16.2.jar:/home/vboxuser/kafka_2.12-3.9.2/bin/../libs/jackson-dataformat-csv-2.16.2.jar:/home/vboxuser/kafka_2.12-3.9.2/bin/../libs/jackson-datatype-jdk8-2.16.2.jar:/home/vboxuser/kafka_2.12-3.9.2/bin/../libs/jackson-jaxrs-base-2.16.2.jar:/home/vboxuser/kafka_2.12-3.9.2/bin/../libs/jackson-jaxrs-json-provider-2.16.2.jar:/home/vboxuser/kafka_2.12-3.9.2/bin/../libs/jackson-module-afterburner-2.16.2.jar:/home/vboxuser/kafka_2.12-3.9.2/bin/../libs/jackson-module-jaxb-annotations-2.16.2.jar:/home/vboxuser/kafka_2.12-3.9.2/bin/../libs/jackson-module-scala_2.12-2.16.2.jar:/home/vboxuser/kafka_2.12-3.9.2/bin/../libs/jakarta.activation-api-1.2.2.jar:/home/vboxuser/kafka_2.12-3.9.2/bin/../libs/jakarta.annotation-api-1.3.5.jar:/home/vboxuser/kafka_2.12-3.9.2/bin/../libs/jakarta.inject-2.6.1.jar:/home/vboxuser/kafka_2.12-3.9.2/bin/../libs/jakarta.validation-api-2.0.2.jar:/home/vboxuser/kafka_2.12-3.9.2/bin/../libs/jakarta.ws.rs-api-2.1.6.jar:/home/vboxuser/kafka_2.12-3.9.2/bin/../libs/jakarta.xml.bind-api-2.3.3.jar:/home/vboxuser/kafka_2.12-3.9.2/bin/../libs/javassist-3.29.2-GA.jar:/home/vboxuser/kafka_2.12-3.9.2/bin/../libs/javax.activation-api-1.2.0.jar:/home/vboxuser/kafka_2.12-3.9.2/bin/../libs/javax.annotation-api-1.3.2.jar:/home/vboxuser/kafka_2.12-3.9.2/bin/../libs/javax.servlet-api-3.1.0.jar:/home/vboxuser/kafka_2.12-3.9.2/bin/../libs/javax.ws.rs-api-2.1.1.jar:/home/vboxuser/kafka_2.12-3.9.2/bin/../libs/jaxb-api-2.3.1.jar:/home/vboxuser/kafka_2.12-3.9.2/bin/../libs/jersey-client-2.47.jar:/home/vboxuser/kafka_2.12-3.9.2/bin/../libs/jersey-common-2.47.jar:/home/vboxuser/kafka_2.12-3.9.2/bin/../libs/jersey-container-servlet-2.47.jar:/home/vboxuser/kafka_2.12-3.9.2/bin/../libs/jersey-container-servlet-core-2.47.jar:/home/vboxuser/kafka_2.12-3.9.2/bin/../libs/jersey-hk2-2.47.jar:/home/vboxuser/kafka_2.12-3.9.2/bin/../libs/jersey-server-2.47.jar:/home/vboxuser/kafka_2.12-3.9.2/bin/../libs/jetty-client-9.4.57.v20241219.jar:/home/vboxuser/kafka_2.12-3.9.2/bin/../libs/jetty-continuation-9.4.57.v20241219.jar:/home/vboxuser/kafka_2.12-3.9.2/bin/../libs/jetty-http-9.4.57.v20241219.jar:/home/vboxuser/kafka_2.12-3.9.2/bin/../libs/jetty-io-9.4.57.v20241219.jar:/home/vboxuser/kafka_2.12-3.9.2/bin/../libs/jetty-security-9.4.57.v20241219.jar:/home/vboxuser/kafka_2.12-3.9.2/bin/../libs/jetty-server-9.4.57.v20241219.jar:/home/vboxuser/kafka_2.12-3.9.2/bin/../libs/jetty-servlet-9.4.57.v20241219.jar:/home/vboxuser/kafka_2.12-3.9.2/bin/../libs/jetty-servlets-9.4.57.v20241219.jar:/home/vboxuser/kafka_2.12-3.9.2/bin/../libs/jetty-util-9.4.57.v20241219.jar:/home/vboxuser/kafka_2.12-3.9.2/bin/../libs/jetty-util-ajax-9.4.57.v20241219.jar:/home/vboxuser/kafka_2.12-3.9.2/bin/../libs/jline-3.25.1.jar:/home/vboxuser/kafka_2.12-3.9.2/bin/../libs/jopt-simple-5.0.4.jar:/home/vboxuser/kafka_2.12-3.9.2/bin/../libs/jose4j-0.9.6.jar:/home/vboxuser/kafka_2.12-3.9.2/bin/../libs/jsr305-3.0.2.jar:/home/vboxuser/kafka_2.12-3.9.2/bin/../libs/kafka_2.12-3.9.2.jar:/home/vboxuser/kafka_2.12-3.9.2/bin/../libs/kafka-clients-3.9.2.jar:/home/vboxuser/kafka_2.12-3.9.2/bin/../libs/kafka-group-coordinator-3.9.2.jar:/home/vboxuser/kafka_2.12-3.9.2/bin/../libs/kafka-group-coordinator-api-3.9.2.jar:/home/vboxuser/kafka_2.12-3.9.2/bin/../libs/kafka-metadata-3.9.2.jar:/home/vboxuser/kafka_2.12-3.9.2/bin/../libs/kafka-raft-3.9.2.jar:/home/vboxuser/kafka_2.12-3.9.2/bin/../libs/kafka-server-3.9.2.jar:/home/vboxuser/kafka_2.12-3.9.2/bin/../libs/kafka-server-common-3.9.2.jar:/home/vboxuser/kafka_2.12-3.9.2/bin/../libs/kafka-shell-3.9.2.jar:/home/vboxuser/kafka_2.12-3.9.2/bin/../libs/kafka-storage-3.9.2.jar:/home/vboxuser/kafka_2.12-3.9.2/bin/../libs/kafka-storage-api-3.9.2.jar:/home/vboxuser/kafka_2.12-3.9.2/bin/../libs/kafka-streams-3.9.2.jar:/home/vboxuser/kafka_2.12-3.9.2/bin/../libs/kafka-streams-examples-3.9.2.jar:/home/vboxuser/kafka_2.12-3.9.2/bin/../libs/kafka-streams-scala_2.12-3.9.2.jar:/home/vboxuser/kafka_2.12-3.9.2/bin/../libs/kafka-streams-test-utils-3.9.2.jar:/home/vboxuser/kafka_2.12-3.9.2/bin/../libs/kafka-tools-3.9.2.jar:/home/vboxuser/kafka_2.12-3.9.2/bin/../libs/kafka-tools-api-3.9.2.jar:/home/vboxuser/kafka_2.12-3.9.2/bin/../libs/kafka-transaction-coordinator-3.9.2.jar:/home/vboxuser/kafka_2.12-3.9.2/bin/../libs/lz4-java-1.10.1.jar:/home/vboxuser/kafka_2.12-3.9.2/bin/../libs/maven-artifact-3.9.6.jar:/home/vboxuser/kafka_2.12-3.9.2/bin/../libs/metrics-core-2.2.0.jar:/home/vboxuser/kafka_2.12-3.9.2/bin/../libs/metrics-core-4.1.12.1.jar:/home/vboxuser/kafka_2.12-3.9.2/bin/../libs/netty-buffer-4.1.125.Final.jar:/home/vboxuser/kafka_2.12-3.9.2/bin/../libs/netty-codec-4.1.125.Final.jar:/home/vboxuser/kafka_2.12-3.9.2/bin/../libs/netty-common-4.1.125.Final.jar:/home/vboxuser/kafka_2.12-3.9.2/bin/../libs/netty-handler-4.1.125.Final.jar:/home/vboxuser/kafka_2.12-3.9.2/bin/../libs/netty-resolver-4.1.125.Final.jar:/home/vboxuser/kafka_2.12-3.9.2/bin/../libs/netty-transport-4.1.125.Final.jar:/home/vboxuser/kafka_2.12-3.9.2/bin/../libs/netty-transport-classes-epoll-4.1.125.Final.jar:/home/vboxuser/kafka_2.12-3.9.2/bin/../libs/netty-transport-native-epoll-4.1.125.Final.jar:/home/vboxuser/kafka_2.12-3.9.2/bin/../libs/netty-transport-native-unix-common-4.1.125.Final.jar:/home/vboxuser/kafka_2.12-3.9.2/bin/../libs/opentelemetry-proto-1.0.0-alpha.jar:/home/vboxuser/kafka_2.12-3.9.2/bin/../libs/osgi-resource-locator-1.0.3.jar:/home/vboxuser/kafka_2.12-3.9.2/bin/../libs/paranamer-2.8.jar:/home/vboxuser/kafka_2.12-3.9.2/bin/../libs/pcollections-4.0.1.jar:/home/vboxuser/kafka_2.12-3.9.2/bin/../libs/plexus-utils-3.5.1.jar:/home/vboxuser/kafka_2.12-3.9.2/bin/../libs/protobuf-java-3.25.5.jar:/home/vboxuser/kafka_2.12-3.9.2/bin/../libs/reflections-0.10.2.jar:/home/vboxuser/kafka_2.12-3.9.2/bin/../libs/reload4j-1.2.25.jar:/home/vboxuser/kafka_2.12-3.9.2/bin/../libs/rocksdbjni-7.9.2.jar:/home/vboxuser/kafka_2.12-3.9.2/bin/../libs/scala-collection-compat_2.12-2.10.0.jar:/home/vboxuser/kafka_2.12-3.9.2/bin/../libs/scala-java8-compat_2.12-1.0.2.jar:/home/vboxuser/kafka_2.12-3.9.2/bin/../libs/scala-library-2.12.19.jar:/home/vboxuser/kafka_2.12-3.9.2/bin/../libs/scala-logging_2.12-3.9.5.jar:/home/vboxuser/kafka_2.12-3.9.2/bin/../libs/scala-reflect-2.12.19.jar:/home/vboxuser/kafka_2.12-3.9.2/bin/../libs/slf4j-api-1.7.36.jar:/home/vboxuser/kafka_2.12-3.9.2/bin/../libs/slf4j-reload4j-1.7.36.jar:/home/vboxuser/kafka_2.12-3.9.2/bin/../libs/snappy-java-1.1.10.5.jar:/home/vboxuser/kafka_2.12-3.9.2/bin/../libs/swagger-annotations-2.2.8.jar:/home/vboxuser/kafka_2.12-3.9.2/bin/../libs/trogdor-3.9.2.jar:/home/vboxuser/kafka_2.12-3.9.2/bin/../libs/zookeeper-3.8.4.jar:/home/vboxuser/kafka_2.12-3.9.2/bin/../libs/zookeeper-jute-3.8.4.jar:/home/vboxuser/kafka_2.12-3.9.2/bin/../libs/zstd-jni-1.5.6-4.jar (org.apache.zookeeper.server.ZooKeeperServer)
[2026-04-05 20:40:16,779] INFO Server environment:java.library.path=/usr/java/packages/lib:/usr/lib/x86_64-linux-gnu/jni:/lib/x86_64-linux-gnu:/usr/lib/x86_64-linux-gnu:/usr/lib/jni:/lib:/usr/lib (org.apache.zookeeper.server.ZooKeeperServer)
[2026-04-05 20:40:16,780] INFO Server environment:java.io.tmpdir=/tmp (org.apache.zookeeper.server.ZooKeeperServer)
[2026-04-05 20:40:16,780] INFO Server environment:java.compiler=<NA> (org.apache.zookeeper.server.ZooKeeperServer)
[2026-04-05 20:40:16,780] INFO Server environment:os.name=Linux (org.apache.zookeeper.server.ZooKeeperServer)
[2026-04-05 20:40:16,780] INFO Server environment:os.arch=amd64 (org.apache.zookeeper.server.ZooKeeperServer)
[2026-04-05 20:40:16,780] INFO Server environment:os.version=5.15.0-173-generic (org.apache.zookeeper.server.ZooKeeperServer)
[2026-04-05 20:40:16,781] INFO Server environment:user.name=vboxuser (org.apache.zookeeper.server.ZooKeeperServer)
[2026-04-05 20:40:16,781] INFO Server environment:user.home=/home/vboxuser (org.apache.zookeeper.server.ZooKeeperServer)
[2026-04-05 20:40:16,781] INFO Server environment:user.dir=/home/vboxuser/kafka_2.12-3.9.2 (org.apache.zookeeper.server.ZooKeeperServer)
[2026-04-05 20:40:16,781] INFO Server environment:os.memory.free=502MB (org.apache.zookeeper.server.ZooKeeperServer)
[2026-04-05 20:40:16,781] INFO Server environment:os.memory.max=512MB (org.apache.zookeeper.server.ZooKeeperServer)
[2026-04-05 20:40:16,781] INFO Server environment:os.memory.total=512MB (org.apache.zookeeper.server.ZooKeeperServer)
[2026-04-05 20:40:16,781] INFO zookeeper.enableEagerACLCheck = false (org.apache.zookeeper.server.ZooKeeperServer)
[2026-04-05 20:40:16,781] INFO zookeeper.digest.enabled = true (org.apache.zookeeper.server.ZooKeeperServer)
[2026-04-05 20:40:16,782] INFO zookeeper.closeSessionTxn.enabled = true (org.apache.zookeeper.server.ZooKeeperServer)
[2026-04-05 20:40:16,782] INFO zookeeper.flushDelay = 0 ms (org.apache.zookeeper.server.ZooKeeperServer)
[2026-04-05 20:40:16,782] INFO zookeeper.maxWriteQueuePollTime = 0 ms (org.apache.zookeeper.server.ZooKeeperServer)
[2026-04-05 20:40:16,782] INFO zookeeper.maxBatchSize=1000 (org.apache.zookeeper.server.ZooKeeperServer)
[2026-04-05 20:40:16,782] INFO zookeeper.intBufferStartingSizeBytes = 1024 (org.apache.zookeeper.server.ZooKeeperServer)
[2026-04-05 20:40:16,787] INFO Weighed connection throttling is disabled (org.apache.zookeeper.server.BlueThrottle)
[2026-04-05 20:40:16,789] INFO minSessionTimeout set to 6000 ms (org.apache.zookeeper.server.ZooKeeperServer)
[2026-04-05 20:40:16,790] INFO maxSessionTimeout set to 60000 ms (org.apache.zookeeper.server.ZooKeeperServer)
[2026-04-05 20:40:16,792] INFO getData response cache size is initialized with value 400. (org.apache.zookeeper.server.ResponseCache)
[2026-04-05 20:40:16,794] INFO getChildren response cache size is initialized with value 400. (org.apache.zookeeper.server.ResponseCache)
[2026-04-05 20:40:16,796] INFO zookeeper.pathStats.slotCapacity = 60 (org.apache.zookeeper.server.util.RequestPathMetricsCollector)
[2026-04-05 20:40:16,797] INFO zookeeper.pathStats.slotDuration = 15 (org.apache.zookeeper.server.util.RequestPathMetricsCollector)
[2026-04-05 20:40:16,798] INFO zookeeper.pathStats.maxDepth = 6 (org.apache.zookeeper.server.util.RequestPathMetricsCollector)
[2026-04-05 20:40:16,798] INFO zookeeper.pathStats.initialDelay = 5 (org.apache.zookeeper.server.util.RequestPathMetricsCollector)
[2026-04-05 20:40:16,799] INFO zookeeper.pathStats.delay = 5 (org.apache.zookeeper.server.util.RequestPathMetricsCollector)
[2026-04-05 20:40:16,800] INFO zookeeper.pathStats.enabled = false (org.apache.zookeeper.server.util.RequestPathMetricsCollector)
[2026-04-05 20:40:16,810] INFO The max bytes for all large requests are set to 104857600 (org.apache.zookeeper.server.ZooKeeperServer)
[2026-04-05 20:40:16,811] INFO The large request threshold is set to -1 (org.apache.zookeeper.server.ZooKeeperServer)
[2026-04-05 20:40:16,813] INFO zookeeper.enforce.auth.enabled = false (org.apache.zookeeper.server.AuthenticationHelper)
[2026-04-05 20:40:16,813] INFO zookeeper.enforce.auth.schemes = [] (org.apache.zookeeper.server.AuthenticationHelper)
[2026-04-05 20:40:16,814] INFO Created server with tickTime 3000 ms minSessionTimeout 6000 ms maxSessionTimeout 60000 ms clientPortListenBacklog -1 datadir /tmp/zookeeper/version-2 snapdir /tmp/zookeeper/version-2 (org.apache.zookeeper.server.ZooKeeperServer)
[2026-04-05 20:40:16,823] INFO Using org.apache.zookeeper.server.NIOServerCnxnFactory as server connection factory (org.apache.zookeeper.server.ServerCnxnFactory)
[2026-04-05 20:40:16,825] WARN maxCnxns is not configured, using default value 0. (org.apache.zookeeper.server.ServerCnxnFactory)
[2026-04-05 20:40:16,828] INFO Configuring NIO connection handler with 10s sessionless connection timeout, 1 selector thread(s), 4 worker threads, and 64 kB direct buffers. (org.apache.zookeeper.server.NIOServerCnxnFactory)
[2026-04-05 20:40:16,837] INFO binding to port 0.0.0.0/0.0.0.0:2181 (org.apache.zookeeper.server.NIOServerCnxnFactory)
[2026-04-05 20:40:16,867] INFO Using org.apache.zookeeper.server.watch.WatchManager as watch manager (org.apache.zookeeper.server.watch.WatchManagerFactory)
[2026-04-05 20:40:16,868] INFO Using org.apache.zookeeper.server.watch.WatchManager as watch manager (org.apache.zookeeper.server.watch.WatchManagerFactory)
[2026-04-05 20:40:16,871] INFO zookeeper.snapshotSizeFactor = 0.33 (org.apache.zookeeper.server.ZKDatabase)
[2026-04-05 20:40:16,872] INFO zookeeper.commitLogCount=500 (org.apache.zookeeper.server.ZKDatabase)
[2026-04-05 20:40:16,879] INFO zookeeper.snapshot.compression.method = CHECKED (org.apache.zookeeper.server.persistence.SnapStream)
[2026-04-05 20:40:16,881] INFO Reading snapshot /tmp/zookeeper/version-2/snapshot.0 (org.apache.zookeeper.server.persistence.FileSnap)
[2026-04-05 20:40:16,885] INFO The digest value is empty in snapshot (org.apache.zookeeper.server.DataTree)
[2026-04-05 20:40:16,919] INFO ZooKeeper audit is disabled. (org.apache.zookeeper.audit.ZKAuditProvider)
[2026-04-05 20:40:16,920] INFO 36 txns loaded in 28 ms (org.apache.zookeeper.server.persistence.FileTxnSnapLog)
[2026-04-05 20:40:16,921] INFO Snapshot loaded in 48 ms, highest zxid is 0x24, digest is 71406347443 (org.apache.zookeeper.server.ZKDatabase)
[2026-04-05 20:40:16,922] INFO Snapshotting: 0x24 to /tmp/zookeeper/version-2/snapshot.24 (org.apache.zookeeper.server.persistence.FileTxnSnapLog)
[2026-04-05 20:40:16,925] INFO Snapshot taken in 3 ms (org.apache.zookeeper.server.ZooKeeperServer)
[2026-04-05 20:40:16,948] INFO zookeeper.request_throttler.shutdownTimeout = 10000 ms (org.apache.zookeeper.server.RequestThrottler)
[2026-04-05 20:40:16,949] INFO PrepRequestProcessor (sid:0) started, reconfigEnabled=false (org.apache.zookeeper.server.PrepRequestProcessor)
[2026-04-05 20:40:16,980] INFO Using checkIntervalMs=60000 maxPerMinute=10000 maxNeverUsedIntervalMs=0 (org.apache.zookeeper.server.ContainerManager)
[2026-04-05 20:41:25,500] INFO Creating new log file: log.25 (org.apache.zookeeper.server.persistence.FileTxnLog)

Evidencia del comando python3 kafka_producer.py 
Sent: {'sensor_id': 1, 'temperature': 29.69, 'humidity': 65.64, 'timestamp': 1775422742}
Sent: {'sensor_id': 6, 'temperature': 24.39, 'humidity': 42.02, 'timestamp': 1775422743}
Sent: {'sensor_id': 4, 'temperature': 25.6, 'humidity': 69.75, 'timestamp': 1775422744}
Sent: {'sensor_id': 7, 'temperature': 28.72, 'humidity': 50.23, 'timestamp': 1775422745}
Sent: {'sensor_id': 5, 'temperature': 26.02, 'humidity': 40.75, 'timestamp': 1775422746}
Sent: {'sensor_id': 5, 'temperature': 27.34, 'humidity': 31.56, 'timestamp': 1775422747}
Sent: {'sensor_id': 1, 'temperature': 21.84, 'humidity': 37.21, 'timestamp': 1775422748}
Sent: {'sensor_id': 2, 'temperature': 24.3, 'humidity': 32.41, 'timestamp': 1775422749}
Sent: {'sensor_id': 5, 'temperature': 21.94, 'humidity': 50.37, 'timestamp': 1775422750}
Sent: {'sensor_id': 3, 'temperature': 21.79, 'humidity': 52.35, 'timestamp': 1775422751}
Sent: {'sensor_id': 1, 'temperature': 27.59, 'humidity': 52.33, 'timestamp': 1775422752}
Sent: {'sensor_id': 7, 'temperature': 28.26, 'humidity': 69.44, 'timestamp': 1775422753}
Sent: {'sensor_id': 7, 'temperature': 23.33, 'humidity': 63.23, 'timestamp': 1775422754}
Sent: {'sensor_id': 1, 'temperature': 23.77, 'humidity': 54.81, 'timestamp': 1775422755}
Sent: {'sensor_id': 10, 'temperature': 28.65, 'humidity': 30.34, 'timestamp': 1775422756}
Sent: {'sensor_id': 10, 'temperature': 23.74, 'humidity': 68.32, 'timestamp': 1775422757}
Sent: {'sensor_id': 6, 'temperature': 21.34, 'humidity': 53.9, 'timestamp': 1775422758}
Sent: {'sensor_id': 1, 'temperature': 28.17, 'humidity': 38.55, 'timestamp': 1775422759}
Sent: {'sensor_id': 1, 'temperature': 20.33, 'humidity': 35.86, 'timestamp': 1775422760}
Sent: {'sensor_id': 9, 'temperature': 25.3, 'humidity': 51.39, 'timestamp': 1775422761}
Sent: {'sensor_id': 10, 'temperature': 20.71, 'humidity': 61.1, 'timestamp': 1775422762}
Sent: {'sensor_id': 10, 'temperature': 26.79, 'humidity': 54.31, 'timestamp': 1775422763}
Sent: {'sensor_id': 7, 'temperature': 29.46, 'humidity': 46.26, 'timestamp': 1775422764}
Sent: {'sensor_id': 8, 'temperature': 24.56, 'humidity': 62.08, 'timestamp': 1775422765}
Sent: {'sensor_id': 8, 'temperature': 22.95, 'humidity': 47.12, 'timestamp': 1775422766}
Sent: {'sensor_id': 8, 'temperature': 26.06, 'humidity': 61.59, 'timestamp': 1775422767}
Sent: {'sensor_id': 7, 'temperature': 24.17, 'humidity': 32.6, 'timestamp': 1775422768}
Sent: {'sensor_id': 6, 'temperature': 23.71, 'humidity': 31.45, 'timestamp': 1775422769}
Sent: {'sensor_id': 7, 'temperature': 22.81, 'humidity': 55.02, 'timestamp': 1775422770}
Sent: {'sensor_id': 10, 'temperature': 20.1, 'humidity': 52.16, 'timestamp': 1775422771}
Sent: {'sensor_id': 4, 'temperature': 27.01, 'humidity': 35.82, 'timestamp': 1775422772}
Sent: {'sensor_id': 3, 'temperature': 24.27, 'humidity': 49.57, 'timestamp': 1775422773}
Sent: {'sensor_id': 3, 'temperature': 21.7, 'humidity': 30.56, 'timestamp': 1775422774}
Sent: {'sensor_id': 1, 'temperature': 28.87, 'humidity': 53.24, 'timestamp': 1775422775}
Sent: {'sensor_id': 4, 'temperature': 29.13, 'humidity': 42.57, 'timestamp': 1775422776}
Sent: {'sensor_id': 1, 'temperature': 23.68, 'humidity': 42.18, 'timestamp': 1775422777}
Sent: {'sensor_id': 5, 'temperature': 25.26, 'humidity': 46.26, 'timestamp': 1775422778}
Sent: {'sensor_id': 6, 'temperature': 26.56, 'humidity': 51.95, 'timestamp': 1775422779}
Sent: {'sensor_id': 2, 'temperature': 27.33, 'humidity': 69.08, 'timestamp': 1775422780}
Sent: {'sensor_id': 6, 'temperature': 22.19, 'humidity': 39.53, 'timestamp': 1775422781}
Sent: {'sensor_id': 2, 'temperature': 20.53, 'humidity': 69.14, 'timestamp': 1775422782}
Sent: {'sensor_id': 4, 'temperature': 21.19, 'humidity': 40.45, 'timestamp': 1775422783}
Sent: {'sensor_id': 8, 'temperature': 28.72, 'humidity': 61.58, 'timestamp': 1775422784}
Sent: {'sensor_id': 1, 'temperature': 27.69, 'humidity': 45.33, 'timestamp': 1775422785}
Sent: {'sensor_id': 2, 'temperature': 21.99, 'humidity': 58.35, 'timestamp': 1775422786}
Sent: {'sensor_id': 3, 'temperature': 28.58, 'humidity': 48.33, 'timestamp': 1775422787}
Sent: {'sensor_id': 3, 'temperature': 27.58, 'humidity': 39.08, 'timestamp': 1775422788}
Sent: {'sensor_id': 4, 'temperature': 25.86, 'humidity': 39.12, 'timestamp': 1775422789}
Sent: {'sensor_id': 3, 'temperature': 23.05, 'humidity': 68.68, 'timestamp': 1775422790}
Sent: {'sensor_id': 5, 'temperature': 29.62, 'humidity': 41.6, 'timestamp': 1775422791}
Sent: {'sensor_id': 2, 'temperature': 22.26, 'humidity': 34.77, 'timestamp': 1775422792}
Sent: {'sensor_id': 8, 'temperature': 29.94, 'humidity': 41.33, 'timestamp': 1775422793}
Sent: {'sensor_id': 5, 'temperature': 23.99, 'humidity': 30.05, 'timestamp': 1775422794}
Sent: {'sensor_id': 6, 'temperature': 23.75, 'humidity': 69.05, 'timestamp': 1775422795}
Sent: {'sensor_id': 2, 'temperature': 20.41, 'humidity': 61.91, 'timestamp': 1775422796}
Sent: {'sensor_id': 9, 'temperature': 25.5, 'humidity': 31.6, 'timestamp': 1775422797}
Sent: {'sensor_id': 7, 'temperature': 23.07, 'humidity': 33.82, 'timestamp': 1775422798}
Sent: {'sensor_id': 6, 'temperature': 28.39, 'humidity': 44.34, 'timestamp': 1775422799}
Sent: {'sensor_id': 7, 'temperature': 22.43, 'humidity': 33.01, 'timestamp': 1775422800}
Sent: {'sensor_id': 1, 'temperature': 27.91, 'humidity': 43.13, 'timestamp': 1775422801}
Sent: {'sensor_id': 2, 'temperature': 23.79, 'humidity': 33.63, 'timestamp': 1775422802}
Sent: {'sensor_id': 9, 'temperature': 23.31, 'humidity': 50.35, 'timestamp': 1775422803}
Sent: {'sensor_id': 7, 'temperature': 20.14, 'humidity': 37.07, 'timestamp': 1775422804}
Sent: {'sensor_id': 4, 'temperature': 21.72, 'humidity': 32.6, 'timestamp': 1775422805}
Sent: {'sensor_id': 3, 'temperature': 24.75, 'humidity': 32.87, 'timestamp': 1775422806}
Sent: {'sensor_id': 8, 'temperature': 23.01, 'humidity': 59.51, 'timestamp': 1775422807}
Sent: {'sensor_id': 6, 'temperature': 25.4, 'humidity': 50.97, 'timestamp': 1775422808}
Sent: {'sensor_id': 3, 'temperature': 23.54, 'humidity': 35.47, 'timestamp': 1775422809}
Sent: {'sensor_id': 5, 'temperature': 29.02, 'humidity': 43.52, 'timestamp': 1775422810}
Sent: {'sensor_id': 6, 'temperature': 22.95, 'humidity': 30.52, 'timestamp': 1775422811}
Sent: {'sensor_id': 4, 'temperature': 21.27, 'humidity': 65.71, 'timestamp': 1775422812}
Sent: {'sensor_id': 3, 'temperature': 20.28, 'humidity': 49.12, 'timestamp': 1775422813}
Sent: {'sensor_id': 4, 'temperature': 24.48, 'humidity': 66.62, 'timestamp': 1775422814}
Sent: {'sensor_id': 9, 'temperature': 20.47, 'humidity': 39.31, 'timestamp': 1775422815}
Sent: {'sensor_id': 8, 'temperature': 22.48, 'humidity': 41.11, 'timestamp': 1775422816}
Sent: {'sensor_id': 6, 'temperature': 24.98, 'humidity': 58.6, 'timestamp': 1775422817}
Sent: {'sensor_id': 8, 'temperature': 27.36, 'humidity': 46.63, 'timestamp': 1775422818}
Sent: {'sensor_id': 4, 'temperature': 22.45, 'humidity': 64.69, 'timestamp': 1775422819}
Sent: {'sensor_id': 1, 'temperature': 26.6, 'humidity': 44.14, 'timestamp': 1775422820}
Sent: {'sensor_id': 9, 'temperature': 27.76, 'humidity': 62.7, 'timestamp': 1775422821}
Sent: {'sensor_id': 6, 'temperature': 27.34, 'humidity': 41.09, 'timestamp': 1775422822}
Sent: {'sensor_id': 6, 'temperature': 21.39, 'humidity': 40.24, 'timestamp': 1775422823}
Sent: {'sensor_id': 5, 'temperature': 28.18, 'humidity': 68.32, 'timestamp': 1775422824}
Sent: {'sensor_id': 1, 'temperature': 24.42, 'humidity': 64.66, 'timestamp': 1775422825}
Sent: {'sensor_id': 9, 'temperature': 21.98, 'humidity': 62.19, 'timestamp': 1775422826}
Sent: {'sensor_id': 2, 'temperature': 27.22, 'humidity': 45.75, 'timestamp': 1775422827}
Sent: {'sensor_id': 3, 'temperature': 23.36, 'humidity': 67.23, 'timestamp': 1775422828}
Sent: {'sensor_id': 9, 'temperature': 26.7, 'humidity': 59.37, 'timestamp': 1775422829}
Sent: {'sensor_id': 3, 'temperature': 22.7, 'humidity': 51.93, 'timestamp': 1775422830}
Sent: {'sensor_id': 9, 'temperature': 22.63, 'humidity': 38.94, 'timestamp': 1775422831}
Sent: {'sensor_id': 4, 'temperature': 26.63, 'humidity': 43.56, 'timestamp': 1775422832}
Sent: {'sensor_id': 6, 'temperature': 27.91, 'humidity': 45.74, 'timestamp': 1775422833}
Sent: {'sensor_id': 3, 'temperature': 27.36, 'humidity': 41.44, 'timestamp': 1775422834}
Sent: {'sensor_id': 6, 'temperature': 22.65, 'humidity': 40.58, 'timestamp': 1775422835}
Sent: {'sensor_id': 5, 'temperature': 25.07, 'humidity': 33.86, 'timestamp': 1775422836}
Sent: {'sensor_id': 7, 'temperature': 28.99, 'humidity': 36.54, 'timestamp': 1775422837}
Sent: {'sensor_id': 6, 'temperature': 26.12, 'humidity': 41.68, 'timestamp': 1775422838}
Sent: {'sensor_id': 3, 'temperature': 24.67, 'humidity': 54.39, 'timestamp': 1775422839}
Sent: {'sensor_id': 5, 'temperature': 26.3, 'humidity': 55.03, 'timestamp': 1775422840}
Sent: {'sensor_id': 1, 'temperature': 23.28, 'humidity': 48.7, 'timestamp': 1775422841}
Sent: {'sensor_id': 9, 'temperature': 21.65, 'humidity': 48.96, 'timestamp': 1775422842}
Sent: {'sensor_id': 7, 'temperature': 22.75, 'humidity': 57.19, 'timestamp': 1775422843}
Sent: {'sensor_id': 1, 'temperature': 21.22, 'humidity': 68.33, 'timestamp': 1775422844}
Sent: {'sensor_id': 9, 'temperature': 22.67, 'humidity': 43.59, 'timestamp': 1775422845}
Sent: {'sensor_id': 4, 'temperature': 21.47, 'humidity': 51.65, 'timestamp': 1775422846}
Sent: {'sensor_id': 8, 'temperature': 26.4, 'humidity': 44.47, 'timestamp': 1775422847}
Sent: {'sensor_id': 3, 'temperature': 24.69, 'humidity': 46.8, 'timestamp': 1775422848}
Sent: {'sensor_id': 7, 'temperature': 27.03, 'humidity': 49.13, 'timestamp': 1775422849}
Sent: {'sensor_id': 4, 'temperature': 28.26, 'humidity': 46.7, 'timestamp': 1775422850}
Sent: {'sensor_id': 1, 'temperature': 25.19, 'humidity': 35.35, 'timestamp': 1775422851}
Sent: {'sensor_id': 8, 'temperature': 21.61, 'humidity': 45.5, 'timestamp': 1775422852}
Sent: {'sensor_id': 2, 'temperature': 23.24, 'humidity': 54.67, 'timestamp': 1775422853}
Sent: {'sensor_id': 6, 'temperature': 26.76, 'humidity': 69.72, 'timestamp': 1775422854}
Sent: {'sensor_id': 6, 'temperature': 25.75, 'humidity': 60.81, 'timestamp': 1775422855}
Sent: {'sensor_id': 1, 'temperature': 26.99, 'humidity': 41.37, 'timestamp': 1775422856}
Sent: {'sensor_id': 10, 'temperature': 25.51, 'humidity': 68.55, 'timestamp': 1775422857}
Sent: {'sensor_id': 5, 'temperature': 24.93, 'humidity': 64.04, 'timestamp': 1775422858}
Sent: {'sensor_id': 1, 'temperature': 21.77, 'humidity': 64.96, 'timestamp': 1775422859}
Sent: {'sensor_id': 9, 'temperature': 22.28, 'humidity': 31.03, 'timestamp': 1775422860}
Sent: {'sensor_id': 5, 'temperature': 25.18, 'humidity': 54.94, 'timestamp': 1775422861}
Sent: {'sensor_id': 10, 'temperature': 23.5, 'humidity': 34.39, 'timestamp': 1775422862}
Sent: {'sensor_id': 1, 'temperature': 23.72, 'humidity': 62.69, 'timestamp': 1775422863}
Sent: {'sensor_id': 4, 'temperature': 20.32, 'humidity': 51.49, 'timestamp': 1775422864}
Informacion del comando spark-submit --packages org.apache.spark:spark-sql-kafka-0-10_2.12:3.5.3 
spark_streaming_consumer.py 
|{2026-04-05 20:50...|        7|26.460000038146973| 53.55500030517578|
|{2026-04-05 20:49...|        7|25.492500066757202| 49.00125026702881|
|{2026-04-05 20:44...|       10| 25.44999967302595| 58.24571337018694|
|{2026-04-05 20:44...|        4|22.956666310628254|  50.7933349609375|
|{2026-04-05 20:48...|        6| 25.18624997138977| 49.51875066757202|
|{2026-04-05 20:45...|        9|22.821249961853027| 43.34499979019165|
|{2026-04-05 20:44...|        5|20.757500171661377|50.334999084472656|
|{2026-04-05 20:44...|        2|25.065714154924667| 53.86857114519392|
|{2026-04-05 20:49...|        8|23.043333371480305|  51.6216672261556|
|{2026-04-05 20:50...|        8|26.460000038146973| 44.69999885559082|
|{2026-04-05 20:48...|        9| 26.41249990463257| 49.49499988555908|
|{2026-04-05 20:48...|        4|23.119999885559082| 40.52499961853027|
|{2026-04-05 20:46...|        9| 25.33714267185756| 50.10857173374721|
|{2026-04-05 20:50...|       10|27.440000534057617| 35.31999969482422|
|{2026-04-05 20:45...|        1|25.149999618530273| 49.92999954223633|
|{2026-04-05 20:45...|        8|26.062856946672714|51.384285245622905|
|{2026-04-05 20:47...|        8|25.262000274658202|60.933999633789064|
|{2026-04-05 20:45...|        6|23.318000030517577| 45.01199951171875|
|{2026-04-05 20:49...|        3|26.966666221618652| 57.17833391825358|
+--------------------+---------+------------------+------------------+
only showing top 20 rows

-------------------------------------------
Batch: 38
-------------------------------------------
+--------------------+---------+------------------+------------------+
|              window|sensor_id|  avg(temperature)|     avg(humidity)|
+--------------------+---------+------------------+------------------+
|{2026-04-05 20:49...|        1| 25.13999993460519|47.377143314906526|
|{2026-04-05 20:50...|        7|26.460000038146973| 53.55500030517578|
|{2026-04-05 20:49...|        7|25.492500066757202| 49.00125026702881|
|{2026-04-05 20:44...|       10| 25.44999967302595| 58.24571337018694|
|{2026-04-05 20:44...|        4|22.956666310628254|  50.7933349609375|
|{2026-04-05 20:48...|        6| 25.18624997138977| 49.51875066757202|
|{2026-04-05 20:45...|        9|22.821249961853027| 43.34499979019165|
|{2026-04-05 20:44...|        5|20.757500171661377|50.334999084472656|
|{2026-04-05 20:44...|        2|25.065714154924667| 53.86857114519392|
|{2026-04-05 20:49...|        8|23.043333371480305|  51.6216672261556|
|{2026-04-05 20:50...|        8|26.460000038146973| 44.69999885559082|
|{2026-04-05 20:48...|        9| 26.41249990463257| 49.49499988555908|
|{2026-04-05 20:48...|        4|23.119999885559082| 40.52499961853027|
|{2026-04-05 20:46...|        9| 25.33714267185756| 50.10857173374721|
|{2026-04-05 20:50...|       10|27.440000534057617| 35.31999969482422|
|{2026-04-05 20:45...|        1|25.149999618530273| 49.92999954223633|
|{2026-04-05 20:45...|        8|26.062856946672714|51.384285245622905|
|{2026-04-05 20:47...|        8|25.262000274658202|60.933999633789064|
|{2026-04-05 20:45...|        6|23.318000030517577| 45.01199951171875|
|{2026-04-05 20:49...|        3|26.966666221618652| 57.17833391825358|
+--------------------+---------+------------------+------------------+
only showing top 20 rows

-------------------------------------------
Batch: 39
-------------------------------------------
+--------------------+---------+------------------+------------------+
|              window|sensor_id|  avg(temperature)|     avg(humidity)|
+--------------------+---------+------------------+------------------+
|{2026-04-05 20:49...|        1| 25.13999993460519|47.377143314906526|
|{2026-04-05 20:50...|        7|27.485000133514404| 49.27750015258789|
|{2026-04-05 20:49...|        7|25.492500066757202| 49.00125026702881|
|{2026-04-05 20:44...|       10| 25.44999967302595| 58.24571337018694|
|{2026-04-05 20:44...|        4|22.956666310628254|  50.7933349609375|
|{2026-04-05 20:48...|        6| 25.18624997138977| 49.51875066757202|
|{2026-04-05 20:45...|        9|22.821249961853027| 43.34499979019165|
|{2026-04-05 20:44...|        5|20.757500171661377|50.334999084472656|
|{2026-04-05 20:44...|        2|25.065714154924667| 53.86857114519392|
|{2026-04-05 20:49...|        8|23.043333371480305|  51.6216672261556|
|{2026-04-05 20:50...|        8|26.460000038146973| 44.69999885559082|
|{2026-04-05 20:48...|        9| 26.41249990463257| 49.49499988555908|
|{2026-04-05 20:48...|        4|23.119999885559082| 40.52499961853027|
|{2026-04-05 20:46...|        9| 25.33714267185756| 50.10857173374721|
|{2026-04-05 20:50...|       10|25.106667200724285| 46.18333307902018|
|{2026-04-05 20:45...|        1|25.149999618530273| 49.92999954223633|
|{2026-04-05 20:45...|        8|26.062856946672714|51.384285245622905|
|{2026-04-05 20:47...|        8|25.262000274658202|60.933999633789064|
|{2026-04-05 20:45...|        6|23.318000030517577| 45.01199951171875|
|{2026-04-05 20:49...|        3|26.966666221618652| 57.17833391825358|
+--------------------+---------+------------------+------------------+
only showing top 20 rows

-------------------------------------------
Batch: 40
-------------------------------------------
+--------------------+---------+------------------+------------------+
|              window|sensor_id|  avg(temperature)|     avg(humidity)|
+--------------------+---------+------------------+------------------+
|{2026-04-05 20:49...|        1| 25.13999993460519|47.377143314906526|
|{2026-04-05 20:50...|        7|27.485000133514404| 49.27750015258789|
|{2026-04-05 20:49...|        7|25.492500066757202| 49.00125026702881|
|{2026-04-05 20:44...|       10| 25.44999967302595| 58.24571337018694|
|{2026-04-05 20:44...|        4|22.956666310628254|  50.7933349609375|
|{2026-04-05 20:48...|        6| 25.18624997138977| 49.51875066757202|
|{2026-04-05 20:45...|        9|22.821249961853027| 43.34499979019165|
|{2026-04-05 20:44...|        5|20.757500171661377|50.334999084472656|
|{2026-04-05 20:44...|        2|25.065714154924667| 53.86857114519392|
|{2026-04-05 20:49...|        8|23.043333371480305|  51.6216672261556|
|{2026-04-05 20:50...|        8|26.460000038146973| 44.69999885559082|
|{2026-04-05 20:48...|        9| 26.41249990463257| 49.49499988555908|
|{2026-04-05 20:48...|        4|23.119999885559082| 40.52499961853027|
|{2026-04-05 20:46...|        9| 25.33714267185756| 50.10857173374721|
|{2026-04-05 20:50...|       10|24.916000366210938|47.594000244140624|
|{2026-04-05 20:45...|        1|25.149999618530273| 49.92999954223633|
|{2026-04-05 20:45...|        8|26.062856946672714|51.384285245622905|
|{2026-04-05 20:47...|        8|25.262000274658202|60.933999633789064|
|{2026-04-05 20:45...|        6|23.318000030517577| 45.01199951171875|
|{2026-04-05 20:49...|        3|26.966666221618652| 57.17833391825358|
+--------------------+---------+------------------+------------------+
only showing top 20 rows

-------------------------------------------
Batch: 41
-------------------------------------------
+--------------------+---------+------------------+------------------+
|              window|sensor_id|  avg(temperature)|     avg(humidity)|
+--------------------+---------+------------------+------------------+
|{2026-04-05 20:49...|        1| 25.13999993460519|47.377143314906526|
|{2026-04-05 20:50...|        7|27.485000133514404| 49.27750015258789|
|{2026-04-05 20:49...|        7|25.492500066757202| 49.00125026702881|
|{2026-04-05 20:44...|       10| 25.44999967302595| 58.24571337018694|
|{2026-04-05 20:44...|        4|22.956666310628254|  50.7933349609375|
|{2026-04-05 20:48...|        6| 25.18624997138977| 49.51875066757202|
|{2026-04-05 20:45...|        9|22.821249961853027| 43.34499979019165|
|{2026-04-05 20:44...|        5|20.757500171661377|50.334999084472656|
|{2026-04-05 20:44...|        2|25.065714154924667| 53.86857114519392|
|{2026-04-05 20:49...|        8|23.043333371480305|  51.6216672261556|
|{2026-04-05 20:50...|        8|26.460000038146973| 44.69999885559082|
|{2026-04-05 20:48...|        9| 26.41249990463257| 49.49499988555908|
|{2026-04-05 20:48...|        4|23.119999885559082| 40.52499961853027|
|{2026-04-05 20:46...|        9| 25.33714267185756| 50.10857173374721|
|{2026-04-05 20:50...|       10|24.400000254313152| 46.32833353678385|
|{2026-04-05 20:45...|        1|25.149999618530273| 49.92999954223633|
|{2026-04-05 20:45...|        8|26.062856946672714|51.384285245622905|
|{2026-04-05 20:47...|        8|25.262000274658202|60.933999633789064|
|{2026-04-05 20:45...|        6|23.318000030517577| 45.01199951171875|
|{2026-04-05 20:49...|        3|26.966666221618652| 57.17833391825358|
+--------------------+---------+------------------+------------------+
only showing top 20 rows

-------------------------------------------
Batch: 42
-------------------------------------------
+--------------------+---------+------------------+------------------+
|              window|sensor_id|  avg(temperature)|     avg(humidity)|
+--------------------+---------+------------------+------------------+
|{2026-04-05 20:49...|        1| 25.13999993460519|47.377143314906526|
|{2026-04-05 20:50...|        7|27.485000133514404| 49.27750015258789|
|{2026-04-05 20:51...|        1| 26.59000015258789| 32.91999816894531|
|{2026-04-05 20:49...|        7|25.492500066757202| 49.00125026702881|
|{2026-04-05 20:44...|       10| 25.44999967302595| 58.24571337018694|
|{2026-04-05 20:44...|        4|22.956666310628254|  50.7933349609375|
|{2026-04-05 20:48...|        6| 25.18624997138977| 49.51875066757202|
|{2026-04-05 20:45...|        9|22.821249961853027| 43.34499979019165|
|{2026-04-05 20:51...|        7|23.170000076293945| 56.56666692097982|
|{2026-04-05 20:44...|        5|20.757500171661377|50.334999084472656|
|{2026-04-05 20:44...|        2|25.065714154924667| 53.86857114519392|
|{2026-04-05 20:49...|        8|23.043333371480305|  51.6216672261556|
|{2026-04-05 20:50...|        8|26.460000038146973| 44.69999885559082|
|{2026-04-05 20:48...|        9| 26.41249990463257| 49.49499988555908|
|{2026-04-05 20:48...|        4|23.119999885559082| 40.52499961853027|
|{2026-04-05 20:46...|        9| 25.33714267185756| 50.10857173374721|
|{2026-04-05 20:50...|       10|24.400000254313152| 46.32833353678385|
|{2026-04-05 20:45...|        1|25.149999618530273| 49.92999954223633|
|{2026-04-05 20:45...|        8|26.062856946672714|51.384285245622905|
|{2026-04-05 20:47...|        8|25.262000274658202|60.933999633789064|
+--------------------+---------+------------------+------------------+
only showing top 20 rows

-------------------------------------------
Batch: 43
-------------------------------------------
+--------------------+---------+------------------+------------------+
|              window|sensor_id|  avg(temperature)|     avg(humidity)|
+--------------------+---------+------------------+------------------+
|{2026-04-05 20:49...|        1| 25.13999993460519|47.377143314906526|
|{2026-04-05 20:50...|        7|27.485000133514404| 49.27750015258789|
|{2026-04-05 20:51...|        1| 26.59000015258789| 32.91999816894531|
|{2026-04-05 20:44...|       10| 25.44999967302595| 58.24571337018694|
|{2026-04-05 20:49...|        7|25.492500066757202| 49.00125026702881|
|{2026-04-05 20:44...|        4|22.956666310628254|  50.7933349609375|
|{2026-04-05 20:48...|        6| 25.18624997138977| 49.51875066757202|
|{2026-04-05 20:51...|        8|22.479999542236328|56.849998474121094|
|{2026-04-05 20:45...|        9|22.821249961853027| 43.34499979019165|
|{2026-04-05 20:51...|        7|23.170000076293945| 56.56666692097982|
|{2026-04-05 20:44...|        5|20.757500171661377|50.334999084472656|
|{2026-04-05 20:44...|        2|25.065714154924667| 53.86857114519392|
|{2026-04-05 20:49...|        8|23.043333371480305|  51.6216672261556|
|{2026-04-05 20:50...|        8|26.460000038146973| 44.69999885559082|
|{2026-04-05 20:48...|        9| 26.41249990463257| 49.49499988555908|
|{2026-04-05 20:48...|        4|23.119999885559082| 40.52499961853027|
|{2026-04-05 20:46...|        9| 25.33714267185756| 50.10857173374721|
|{2026-04-05 20:50...|       10|24.400000254313152| 46.32833353678385|
|{2026-04-05 20:45...|        1|25.149999618530273| 49.92999954223633|
|{2026-04-05 20:45...|        8|26.062856946672714|51.384285245622905|
+--------------------+---------+------------------+------------------+
only showing top 20 rows

-------------------------------------------
Batch: 44
-------------------------------------------
+--------------------+---------+------------------+------------------+
|              window|sensor_id|  avg(temperature)|     avg(humidity)|
+--------------------+---------+------------------+------------------+
|{2026-04-05 20:49...|        1| 25.13999993460519|47.377143314906526|
|{2026-04-05 20:50...|        7|27.485000133514404| 49.27750015258789|
|{2026-04-05 20:51...|        1|24.200000286102295| 52.16499900817871|
|{2026-04-05 20:44...|       10| 25.44999967302595| 58.24571337018694|
|{2026-04-05 20:49...|        7|25.492500066757202| 49.00125026702881|
|{2026-04-05 20:44...|        4|22.956666310628254|  50.7933349609375|
|{2026-04-05 20:48...|        6| 25.18624997138977| 49.51875066757202|
|{2026-04-05 20:51...|        8|21.639999389648438|  60.0049991607666|
|{2026-04-05 20:45...|        9|22.821249961853027| 43.34499979019165|
|{2026-04-05 20:51...|        7|23.170000076293945| 56.56666692097982|
|{2026-04-05 20:44...|        5|20.757500171661377|50.334999084472656|
|{2026-04-05 20:44...|        2|25.065714154924667| 53.86857114519392|
|{2026-04-05 20:49...|        8|23.043333371480305|  51.6216672261556|
|{2026-04-05 20:50...|        8|26.460000038146973| 44.69999885559082|
|{2026-04-05 20:48...|        9| 26.41249990463257| 49.49499988555908|
|{2026-04-05 20:48...|        4|23.119999885559082| 40.52499961853027|
|{2026-04-05 20:46...|        9| 25.33714267185756| 50.10857173374721|
|{2026-04-05 20:50...|       10|24.400000254313152| 46.32833353678385|
|{2026-04-05 20:45...|        1|25.149999618530273| 49.92999954223633|
|{2026-04-05 20:45...|        8|26.062856946672714|51.384285245622905|
+--------------------+---------+------------------+------------------+
only showing top 20 rows

-------------------------------------------
Batch: 45
-------------------------------------------
+--------------------+---------+------------------+------------------+
|              window|sensor_id|  avg(temperature)|     avg(humidity)|
+--------------------+---------+------------------+------------------+
|{2026-04-05 20:49...|        1| 25.13999993460519|47.377143314906526|
|{2026-04-05 20:50...|        7|27.485000133514404| 49.27750015258789|
|{2026-04-05 20:51...|        1|24.300000381469726| 55.63799896240234|
|{2026-04-05 20:44...|       10| 25.44999967302595| 58.24571337018694|
|{2026-04-05 20:49...|        7|25.492500066757202| 49.00125026702881|
|{2026-04-05 20:44...|        4|22.956666310628254|  50.7933349609375|
|{2026-04-05 20:48...|        6| 25.18624997138977| 49.51875066757202|
|{2026-04-05 20:51...|        8| 24.41333262125651| 57.70666631062826|
|{2026-04-05 20:45...|        9|22.821249961853027| 43.34499979019165|
|{2026-04-05 20:51...|        7|22.947500228881836| 57.80000019073486|
|{2026-04-05 20:44...|        5|20.757500171661377|50.334999084472656|
|{2026-04-05 20:44...|        2|25.065714154924667| 53.86857114519392|
|{2026-04-05 20:49...|        8|23.043333371480305|  51.6216672261556|
|{2026-04-05 20:50...|        8|26.460000038146973| 44.69999885559082|
|{2026-04-05 20:48...|        9| 26.41249990463257| 49.49499988555908|
|{2026-04-05 20:48...|        4|23.119999885559082| 40.52499961853027|
|{2026-04-05 20:46...|        9| 25.33714267185756| 50.10857173374721|
|{2026-04-05 20:50...|       10|24.400000254313152| 46.32833353678385|
|{2026-04-05 20:45...|        1|25.149999618530273| 49.92999954223633|
|{2026-04-05 20:45...|        8|26.062856946672714|51.384285245622905|
+--------------------+---------+------------------+------------------+
only showing top 20 rows

-------------------------------------------
Batch: 46
-------------------------------------------
+--------------------+---------+------------------+------------------+
|              window|sensor_id|  avg(temperature)|     avg(humidity)|
+--------------------+---------+------------------+------------------+
|{2026-04-05 20:49...|        1| 25.13999993460519|47.377143314906526|
|{2026-04-05 20:50...|        7|27.485000133514404| 49.27750015258789|
|{2026-04-05 20:51...|        1|24.300000381469726| 55.63799896240234|
|{2026-04-05 20:44...|       10| 25.44999967302595| 58.24571337018694|
|{2026-04-05 20:49...|        7|25.492500066757202| 49.00125026702881|
|{2026-04-05 20:44...|        4|22.956666310628254|  50.7933349609375|
|{2026-04-05 20:48...|        6| 25.18624997138977| 49.51875066757202|
|{2026-04-05 20:51...|        8| 24.41333262125651| 57.70666631062826|
|{2026-04-05 20:45...|        9|22.821249961853027| 43.34499979019165|
|{2026-04-05 20:51...|        7|22.728000259399415| 52.65400009155273|
|{2026-04-05 20:44...|        5|20.757500171661377|50.334999084472656|
|{2026-04-05 20:44...|        2|25.065714154924667| 53.86857114519392|
|{2026-04-05 20:49...|        8|23.043333371480305|  51.6216672261556|
|{2026-04-05 20:50...|        8|26.460000038146973| 44.69999885559082|
|{2026-04-05 20:48...|        9| 26.41249990463257| 49.49499988555908|
|{2026-04-05 20:48...|        4|23.119999885559082| 40.52499961853027|
|{2026-04-05 20:46...|        9| 25.33714267185756| 50.10857173374721|
|{2026-04-05 20:50...|       10|24.400000254313152| 46.32833353678385|
|{2026-04-05 20:45...|        1|25.149999618530273| 49.92999954223633|
|{2026-04-05 20:45...|        8|26.062856946672714|51.384285245622905|
+--------------------+---------+------------------+------------------+
only showing top 20 rows

-------------------------------------------
Batch: 47
-------------------------------------------
+--------------------+---------+------------------+------------------+
|              window|sensor_id|  avg(temperature)|     avg(humidity)|
+--------------------+---------+------------------+------------------+
|{2026-04-05 20:49...|        1| 25.13999993460519|47.377143314906526|
|{2026-04-05 20:50...|        7|27.485000133514404| 49.27750015258789|
|{2026-04-05 20:51...|        1|24.300000381469726| 55.63799896240234|
|{2026-04-05 20:44...|       10| 25.44999967302595| 58.24571337018694|
|{2026-04-05 20:49...|        7|25.492500066757202| 49.00125026702881|
|{2026-04-05 20:44...|        4|22.956666310628254|  50.7933349609375|
|{2026-04-05 20:48...|        6| 25.18624997138977| 49.51875066757202|
|{2026-04-05 20:51...|        8| 24.41333262125651| 57.70666631062826|
|{2026-04-05 20:45...|        9|22.821249961853027| 43.34499979019165|
|{2026-04-05 20:51...|        7|22.191428593226842| 54.69142859322684|
|{2026-04-05 20:44...|        5|20.757500171661377|50.334999084472656|
|{2026-04-05 20:44...|        2|25.065714154924667| 53.86857114519392|
|{2026-04-05 20:49...|        8|23.043333371480305|  51.6216672261556|
|{2026-04-05 20:50...|        8|26.460000038146973| 44.69999885559082|
|{2026-04-05 20:48...|        9| 26.41249990463257| 49.49499988555908|
|{2026-04-05 20:48...|        4|23.119999885559082| 40.52499961853027|
|{2026-04-05 20:46...|        9| 25.33714267185756| 50.10857173374721|
|{2026-04-05 20:50...|       10|24.400000254313152| 46.32833353678385|
|{2026-04-05 20:45...|        1|25.149999618530273| 49.92999954223633|
|{2026-04-05 20:45...|        8|26.062856946672714|51.384285245622905|
+--------------------+---------+------------------+------------------+
only showing top 20 rows

-------------------------------------------
Batch: 48
-------------------------------------------
+--------------------+---------+------------------+------------------+
|              window|sensor_id|  avg(temperature)|     avg(humidity)|
+--------------------+---------+------------------+------------------+
|{2026-04-05 20:49...|        1| 25.13999993460519|47.377143314906526|
|{2026-04-05 20:50...|        7|27.485000133514404| 49.27750015258789|
|{2026-04-05 20:51...|        1|  25.1233336130778| 56.85333251953125|
|{2026-04-05 20:44...|       10| 25.44999967302595| 58.24571337018694|
|{2026-04-05 20:49...|        7|25.492500066757202| 49.00125026702881|
|{2026-04-05 20:44...|        4|22.956666310628254|  50.7933349609375|
|{2026-04-05 20:48...|        6| 25.18624997138977| 49.51875066757202|
|{2026-04-05 20:51...|        8| 24.41333262125651| 57.70666631062826|
|{2026-04-05 20:45...|        9|22.821249961853027| 43.34499979019165|
|{2026-04-05 20:51...|        7|22.191428593226842| 54.69142859322684|
|{2026-04-05 20:44...|        5|20.757500171661377|50.334999084472656|
|{2026-04-05 20:44...|        2|25.065714154924667| 53.86857114519392|
|{2026-04-05 20:49...|        8|23.043333371480305|  51.6216672261556|
|{2026-04-05 20:50...|        8|26.460000038146973| 44.69999885559082|
|{2026-04-05 20:48...|        9| 26.41249990463257| 49.49499988555908|
|{2026-04-05 20:48...|        4|23.119999885559082| 40.52499961853027|
|{2026-04-05 20:52...|        6|26.329999923706055| 58.33000183105469|
|{2026-04-05 20:46...|        9| 25.33714267185756| 50.10857173374721|
|{2026-04-05 20:50...|       10|24.400000254313152| 46.32833353678385|
|{2026-04-05 20:45...|        1|25.149999618530273| 49.92999954223633|
+--------------------+---------+------------------+------------------+
only showing top 20 rows

-------------------------------------------
Batch: 49
-------------------------------------------
+--------------------+---------+------------------+------------------+
|              window|sensor_id|  avg(temperature)|     avg(humidity)|
+--------------------+---------+------------------+------------------+
|{2026-04-05 20:49...|        1| 25.13999993460519|47.377143314906526|
|{2026-04-05 20:50...|        7|27.485000133514404| 49.27750015258789|
|{2026-04-05 20:51...|        1|  25.1233336130778| 56.85333251953125|
|{2026-04-05 20:44...|       10| 25.44999967302595| 58.24571337018694|
|{2026-04-05 20:49...|        7|25.492500066757202| 49.00125026702881|
|{2026-04-05 20:44...|        4|22.956666310628254|  50.7933349609375|
|{2026-04-05 20:48...|        6| 25.18624997138977| 49.51875066757202|
|{2026-04-05 20:51...|        8| 24.41333262125651| 57.70666631062826|
|{2026-04-05 20:45...|        9|22.821249961853027| 43.34499979019165|
|{2026-04-05 20:51...|        7|22.191428593226842| 54.69142859322684|
|{2026-04-05 20:44...|        5|20.757500171661377|50.334999084472656|
|{2026-04-05 20:44...|        2|25.065714154924667| 53.86857114519392|
|{2026-04-05 20:49...|        8|23.043333371480305|  51.6216672261556|
|{2026-04-05 20:50...|        8|26.460000038146973| 44.69999885559082|
|{2026-04-05 20:52...|        2|25.803333918253582| 44.16666603088379|
|{2026-04-05 20:48...|        9| 26.41249990463257| 49.49499988555908|
|{2026-04-05 20:48...|        4|23.119999885559082| 40.52499961853027|
|{2026-04-05 20:52...|        6|26.329999923706055| 58.33000183105469|
|{2026-04-05 20:46...|        9| 25.33714267185756| 50.10857173374721|
|{2026-04-05 20:50...|       10|24.400000254313152| 46.32833353678385|
+--------------------+---------+------------------+------------------+
only showing top 20 rows

-------------------------------------------
Batch: 50
-------------------------------------------
+--------------------+---------+------------------+------------------+
|              window|sensor_id|  avg(temperature)|     avg(humidity)|
+--------------------+---------+------------------+------------------+
|{2026-04-05 20:49...|        1| 25.13999993460519|47.377143314906526|
|{2026-04-05 20:50...|        7|27.485000133514404| 49.27750015258789|
|{2026-04-05 20:51...|        1|  25.1233336130778| 56.85333251953125|
|{2026-04-05 20:44...|       10| 25.44999967302595| 58.24571337018694|
|{2026-04-05 20:49...|        7|25.492500066757202| 49.00125026702881|
|{2026-04-05 20:44...|        4|22.956666310628254|  50.7933349609375|
|{2026-04-05 20:48...|        6| 25.18624997138977| 49.51875066757202|
|{2026-04-05 20:51...|        8| 24.41333262125651| 57.70666631062826|
|{2026-04-05 20:45...|        9|22.821249961853027| 43.34499979019165|
|{2026-04-05 20:51...|        7|22.191428593226842| 54.69142859322684|
|{2026-04-05 20:44...|        5|20.757500171661377|50.334999084472656|
|{2026-04-05 20:44...|        2|25.065714154924667| 53.86857114519392|
|{2026-04-05 20:49...|        8|23.043333371480305|  51.6216672261556|
|{2026-04-05 20:50...|        8|26.460000038146973| 44.69999885559082|
|{2026-04-05 20:52...|        2|24.052000427246092| 53.21400108337402|
|{2026-04-05 20:48...|        9| 26.41249990463257| 49.49499988555908|
|{2026-04-05 20:48...|        4|23.119999885559082| 40.52499961853027|
|{2026-04-05 20:52...|        6|26.329999923706055| 58.33000183105469|
|{2026-04-05 20:46...|        9| 25.33714267185756| 50.10857173374721|
|{2026-04-05 20:50...|       10|24.400000254313152| 46.32833353678385|
+--------------------+---------+------------------+------------------+
only showing top 20 rows

-------------------------------------------
Batch: 51
-------------------------------------------
+--------------------+---------+------------------+------------------+
|              window|sensor_id|  avg(temperature)|     avg(humidity)|
+--------------------+---------+------------------+------------------+
|{2026-04-05 20:49...|        1| 25.13999993460519|47.377143314906526|
|{2026-04-05 20:50...|        7|27.485000133514404| 49.27750015258789|
|{2026-04-05 20:51...|        1|  25.1233336130778| 56.85333251953125|
|{2026-04-05 20:44...|       10| 25.44999967302595| 58.24571337018694|
|{2026-04-05 20:49...|        7|25.492500066757202| 49.00125026702881|
|{2026-04-05 20:44...|        4|22.956666310628254|  50.7933349609375|
|{2026-04-05 20:48...|        6| 25.18624997138977| 49.51875066757202|
|{2026-04-05 20:51...|        8| 24.41333262125651| 57.70666631062826|
|{2026-04-05 20:45...|        9|22.821249961853027| 43.34499979019165|
|{2026-04-05 20:51...|        7|22.191428593226842| 54.69142859322684|
|{2026-04-05 20:44...|        5|20.757500171661377|50.334999084472656|
|{2026-04-05 20:44...|        2|25.065714154924667| 53.86857114519392|
|{2026-04-05 20:49...|        8|23.043333371480305|  51.6216672261556|
|{2026-04-05 20:50...|        8|26.460000038146973| 44.69999885559082|
|{2026-04-05 20:52...|        2|24.020000457763672| 52.04833443959554|
|{2026-04-05 20:48...|        9| 26.41249990463257| 49.49499988555908|
|{2026-04-05 20:48...|        4|23.119999885559082| 40.52499961853027|
|{2026-04-05 20:52...|        6|26.329999923706055| 58.33000183105469|
|{2026-04-05 20:46...|        9| 25.33714267185756| 50.10857173374721|
|{2026-04-05 20:50...|       10|24.400000254313152| 46.32833353678385|
+--------------------+---------+------------------+------------------+
only showing top 20 rows

-------------------------------------------
Batch: 52
-------------------------------------------
+--------------------+---------+------------------+------------------+
|              window|sensor_id|  avg(temperature)|     avg(humidity)|
+--------------------+---------+------------------+------------------+
|{2026-04-05 20:49...|        1| 25.13999993460519|47.377143314906526|
|{2026-04-05 20:50...|        7|27.485000133514404| 49.27750015258789|
|{2026-04-05 20:51...|        1|  25.1233336130778| 56.85333251953125|
|{2026-04-05 20:44...|       10| 25.44999967302595| 58.24571337018694|
|{2026-04-05 20:49...|        7|25.492500066757202| 49.00125026702881|
|{2026-04-05 20:44...|        4|22.956666310628254|  50.7933349609375|
|{2026-04-05 20:48...|        6| 25.18624997138977| 49.51875066757202|
|{2026-04-05 20:51...|        8| 24.41333262125651| 57.70666631062826|
|{2026-04-05 20:45...|        9|22.821249961853027| 43.34499979019165|
|{2026-04-05 20:51...|        7|22.191428593226842| 54.69142859322684|
|{2026-04-05 20:44...|        5|20.757500171661377|50.334999084472656|
|{2026-04-05 20:44...|        2|25.065714154924667| 53.86857114519392|
|{2026-04-05 20:49...|        8|23.043333371480305|  51.6216672261556|
|{2026-04-05 20:50...|        8|26.460000038146973| 44.69999885559082|
|{2026-04-05 20:52...|        2| 23.34125018119812| 47.23875069618225|
|{2026-04-05 20:48...|        9| 26.41249990463257| 49.49499988555908|
|{2026-04-05 20:48...|        4|23.119999885559082| 40.52499961853027|
|{2026-04-05 20:52...|        6|23.576666514078777| 63.32999928792318|
|{2026-04-05 20:46...|        9| 25.33714267185756| 50.10857173374721|
|{2026-04-05 20:50...|       10|24.400000254313152| 46.32833353678385|
+--------------------+---------+------------------+------------------+
only showing top 20 rows

-------------------------------------------
Batch: 53
-------------------------------------------
+--------------------+---------+------------------+------------------+
|              window|sensor_id|  avg(temperature)|     avg(humidity)|
+--------------------+---------+------------------+------------------+
|{2026-04-05 20:49...|        1| 25.13999993460519|47.377143314906526|
|{2026-04-05 20:50...|        7|27.485000133514404| 49.27750015258789|
|{2026-04-05 20:51...|        1|  25.1233336130778| 56.85333251953125|
|{2026-04-05 20:44...|       10| 25.44999967302595| 58.24571337018694|
|{2026-04-05 20:49...|        7|25.492500066757202| 49.00125026702881|
|{2026-04-05 20:44...|        4|22.956666310628254|  50.7933349609375|
|{2026-04-05 20:48...|        6| 25.18624997138977| 49.51875066757202|
|{2026-04-05 20:51...|        8| 24.41333262125651| 57.70666631062826|
|{2026-04-05 20:45...|        9|22.821249961853027| 43.34499979019165|
|{2026-04-05 20:51...|        7|22.191428593226842| 54.69142859322684|
|{2026-04-05 20:44...|        5|20.757500171661377|50.334999084472656|
|{2026-04-05 20:44...|        2|25.065714154924667| 53.86857114519392|
|{2026-04-05 20:49...|        8|23.043333371480305|  51.6216672261556|
|{2026-04-05 20:50...|        8|26.460000038146973| 44.69999885559082|
|{2026-04-05 20:52...|        2|23.145555708143448| 46.88333405388726|
|{2026-04-05 20:48...|        9| 26.41249990463257| 49.49499988555908|
|{2026-04-05 20:48...|        4|23.119999885559082| 40.52499961853027|
|{2026-04-05 20:52...|        6|23.164999961853027| 55.36249923706055|
|{2026-04-05 20:46...|        9| 25.33714267185756| 50.10857173374721|
|{2026-04-05 20:50...|       10|24.400000254313152| 46.32833353678385|
+--------------------+---------+------------------+------------------+
only showing top 20 rows

-------------------------------------------
Batch: 54
-------------------------------------------
+--------------------+---------+------------------+------------------+
|              window|sensor_id|  avg(temperature)|     avg(humidity)|
+--------------------+---------+------------------+------------------+
|{2026-04-05 20:49...|        1| 25.13999993460519|47.377143314906526|
|{2026-04-05 20:50...|        7|27.485000133514404| 49.27750015258789|
|{2026-04-05 20:51...|        1|  25.1233336130778| 56.85333251953125|
|{2026-04-05 20:44...|       10| 25.44999967302595| 58.24571337018694|
|{2026-04-05 20:49...|        7|25.492500066757202| 49.00125026702881|
|{2026-04-05 20:44...|        4|22.956666310628254|  50.7933349609375|
|{2026-04-05 20:48...|        6| 25.18624997138977| 49.51875066757202|
|{2026-04-05 20:51...|        8| 24.41333262125651| 57.70666631062826|
|{2026-04-05 20:45...|        9|22.821249961853027| 43.34499979019165|
|{2026-04-05 20:51...|        7|22.191428593226842| 54.69142859322684|
|{2026-04-05 20:44...|        5|20.757500171661377|50.334999084472656|
|{2026-04-05 20:44...|        2|25.065714154924667| 53.86857114519392|
|{2026-04-05 20:49...|        8|23.043333371480305|  51.6216672261556|
|{2026-04-05 20:50...|        8|26.460000038146973| 44.69999885559082|
|{2026-04-05 20:52...|        2|23.145555708143448| 46.88333405388726|
|{2026-04-05 20:48...|        9| 26.41249990463257| 49.49499988555908|
|{2026-04-05 20:48...|        4|23.119999885559082| 40.52499961853027|
|{2026-04-05 20:52...|        6| 23.17599983215332|  58.1239990234375|
|{2026-04-05 20:46...|        9| 25.33714267185756| 50.10857173374721|
|{2026-04-05 20:53...|        9|20.780000686645508| 68.54000091552734|
+--------------------+---------+------------------+------------------+
only showing top 20 rows

-------------------------------------------
Batch: 55
-------------------------------------------
+--------------------+---------+------------------+------------------+
|              window|sensor_id|  avg(temperature)|     avg(humidity)|
+--------------------+---------+------------------+------------------+
|{2026-04-05 20:49...|        1| 25.13999993460519|47.377143314906526|
|{2026-04-05 20:50...|        7|27.485000133514404| 49.27750015258789|
|{2026-04-05 20:51...|        1|  25.1233336130778| 56.85333251953125|
|{2026-04-05 20:44...|       10| 25.44999967302595| 58.24571337018694|
|{2026-04-05 20:49...|        7|25.492500066757202| 49.00125026702881|
|{2026-04-05 20:44...|        4|22.956666310628254|  50.7933349609375|
|{2026-04-05 20:48...|        6| 25.18624997138977| 49.51875066757202|
|{2026-04-05 20:51...|        8| 24.41333262125651| 57.70666631062826|
|{2026-04-05 20:45...|        9|22.821249961853027| 43.34499979019165|
|{2026-04-05 20:51...|        7|22.191428593226842| 54.69142859322684|
|{2026-04-05 20:44...|        5|20.757500171661377|50.334999084472656|
|{2026-04-05 20:44...|        2|25.065714154924667| 53.86857114519392|
|{2026-04-05 20:49...|        8|23.043333371480305|  51.6216672261556|
|{2026-04-05 20:50...|        8|26.460000038146973| 44.69999885559082|
|{2026-04-05 20:52...|        2|23.145555708143448| 46.88333405388726|
|{2026-04-05 20:48...|        9| 26.41249990463257| 49.49499988555908|
|{2026-04-05 20:53...|        1|22.825000762939453| 56.84000205993652|
|{2026-04-05 20:48...|        4|23.119999885559082| 40.52499961853027|
|{2026-04-05 20:52...|        6| 23.17599983215332|  58.1239990234375|
|{2026-04-05 20:46...|        9| 25.33714267185756| 50.10857173374721|
+--------------------+---------+------------------+------------------+
only showing top 20 rows

-------------------------------------------
Batch: 56
-------------------------------------------
+--------------------+---------+------------------+------------------+
|              window|sensor_id|  avg(temperature)|     avg(humidity)|
+--------------------+---------+------------------+------------------+
|{2026-04-05 20:49...|        1| 25.13999993460519|47.377143314906526|
|{2026-04-05 20:50...|        7|27.485000133514404| 49.27750015258789|
|{2026-04-05 20:51...|        1|  25.1233336130778| 56.85333251953125|
|{2026-04-05 20:44...|       10| 25.44999967302595| 58.24571337018694|
|{2026-04-05 20:49...|        7|25.492500066757202| 49.00125026702881|
|{2026-04-05 20:44...|        4|22.956666310628254|  50.7933349609375|
|{2026-04-05 20:48...|        6| 25.18624997138977| 49.51875066757202|
|{2026-04-05 20:51...|        8| 24.41333262125651| 57.70666631062826|
|{2026-04-05 20:45...|        9|22.821249961853027| 43.34499979019165|
|{2026-04-05 20:51...|        7|22.191428593226842| 54.69142859322684|
|{2026-04-05 20:44...|        5|20.757500171661377|50.334999084472656|
|{2026-04-05 20:44...|        2|25.065714154924667| 53.86857114519392|
|{2026-04-05 20:49...|        8|23.043333371480305|  51.6216672261556|
|{2026-04-05 20:50...|        8|26.460000038146973| 44.69999885559082|
|{2026-04-05 20:52...|        2|23.145555708143448| 46.88333405388726|
|{2026-04-05 20:48...|        9| 26.41249990463257| 49.49499988555908|
|{2026-04-05 20:53...|        1|22.825000762939453| 56.84000205993652|
|{2026-04-05 20:48...|        4|23.119999885559082| 40.52499961853027|
|{2026-04-05 20:52...|        6| 23.17599983215332|  58.1239990234375|
|{2026-04-05 20:46...|        9| 25.33714267185756| 50.10857173374721|
+--------------------+---------+------------------+------------------+
only showing top 20 rows

-------------------------------------------
Batch: 57
-------------------------------------------
+--------------------+---------+------------------+------------------+
|              window|sensor_id|  avg(temperature)|     avg(humidity)|
+--------------------+---------+------------------+------------------+
|{2026-04-05 20:49...|        1| 25.13999993460519|47.377143314906526|
|{2026-04-05 20:50...|        7|27.485000133514404| 49.27750015258789|
|{2026-04-05 20:51...|        1|  25.1233336130778| 56.85333251953125|
|{2026-04-05 20:44...|       10| 25.44999967302595| 58.24571337018694|
|{2026-04-05 20:49...|        7|25.492500066757202| 49.00125026702881|
|{2026-04-05 20:44...|        4|22.956666310628254|  50.7933349609375|
|{2026-04-05 20:48...|        6| 25.18624997138977| 49.51875066757202|
|{2026-04-05 20:51...|        8| 24.41333262125651| 57.70666631062826|
|{2026-04-05 20:45...|        9|22.821249961853027| 43.34499979019165|
|{2026-04-05 20:51...|        7|22.191428593226842| 54.69142859322684|
|{2026-04-05 20:44...|        5|20.757500171661377|50.334999084472656|
|{2026-04-05 20:44...|        2|25.065714154924667| 53.86857114519392|
|{2026-04-05 20:49...|        8|23.043333371480305|  51.6216672261556|
|{2026-04-05 20:50...|        8|26.460000038146973| 44.69999885559082|
|{2026-04-05 20:52...|        2|23.145555708143448| 46.88333405388726|
|{2026-04-05 20:48...|        9| 26.41249990463257| 49.49499988555908|
|{2026-04-05 20:53...|        1|24.473333994547527| 57.21333440144857|
|{2026-04-05 20:48...|        4|23.119999885559082| 40.52499961853027|
|{2026-04-05 20:52...|        6| 23.17599983215332|  58.1239990234375|
|{2026-04-05 20:46...|        9| 25.33714267185756| 50.10857173374721|
+--------------------+---------+------------------+------------------+
only showing top 20 rows

-------------------------------------------
Batch: 58
-------------------------------------------
+--------------------+---------+------------------+------------------+
|              window|sensor_id|  avg(temperature)|     avg(humidity)|
+--------------------+---------+------------------+------------------+
|{2026-04-05 20:49...|        1| 25.13999993460519|47.377143314906526|
|{2026-04-05 20:50...|        7|27.485000133514404| 49.27750015258789|
|{2026-04-05 20:51...|        1|  25.1233336130778| 56.85333251953125|
|{2026-04-05 20:44...|       10| 25.44999967302595| 58.24571337018694|
|{2026-04-05 20:49...|        7|25.492500066757202| 49.00125026702881|
|{2026-04-05 20:44...|        4|22.956666310628254|  50.7933349609375|
|{2026-04-05 20:48...|        6| 25.18624997138977| 49.51875066757202|
|{2026-04-05 20:51...|        8| 24.41333262125651| 57.70666631062826|
|{2026-04-05 20:45...|        9|22.821249961853027| 43.34499979019165|
|{2026-04-05 20:51...|        7|22.191428593226842| 54.69142859322684|
|{2026-04-05 20:44...|        5|20.757500171661377|50.334999084472656|
|{2026-04-05 20:44...|        2|25.065714154924667| 53.86857114519392|
|{2026-04-05 20:49...|        8|23.043333371480305|  51.6216672261556|
|{2026-04-05 20:50...|        8|26.460000038146973| 44.69999885559082|
|{2026-04-05 20:52...|        2|23.145555708143448| 46.88333405388726|
|{2026-04-05 20:48...|        9| 26.41249990463257| 49.49499988555908|
|{2026-04-05 20:53...|        1|24.473333994547527| 57.21333440144857|
|{2026-04-05 20:48...|        4|23.119999885559082| 40.52499961853027|
|{2026-04-05 20:52...|        6| 23.17599983215332|  58.1239990234375|
|{2026-04-05 20:46...|        9| 25.33714267185756| 50.10857173374721|
+--------------------+---------+------------------+------------------+
only showing top 20 rows

-------------------------------------------
Batch: 59
-------------------------------------------
+--------------------+---------+------------------+------------------+
|              window|sensor_id|  avg(temperature)|     avg(humidity)|
+--------------------+---------+------------------+------------------+
|{2026-04-05 20:49...|        1| 25.13999993460519|47.377143314906526|
|{2026-04-05 20:50...|        7|27.485000133514404| 49.27750015258789|
|{2026-04-05 20:51...|        1|  25.1233336130778| 56.85333251953125|
|{2026-04-05 20:44...|       10| 25.44999967302595| 58.24571337018694|
|{2026-04-05 20:49...|        7|25.492500066757202| 49.00125026702881|
|{2026-04-05 20:44...|        4|22.956666310628254|  50.7933349609375|
|{2026-04-05 20:48...|        6| 25.18624997138977| 49.51875066757202|
|{2026-04-05 20:51...|        8| 24.41333262125651| 57.70666631062826|
|{2026-04-05 20:45...|        9|22.821249961853027| 43.34499979019165|
|{2026-04-05 20:51...|        7|22.191428593226842| 54.69142859322684|
|{2026-04-05 20:44...|        5|20.757500171661377|50.334999084472656|
|{2026-04-05 20:44...|        2|25.065714154924667| 53.86857114519392|
|{2026-04-05 20:49...|        8|23.043333371480305|  51.6216672261556|
|{2026-04-05 20:50...|        8|26.460000038146973| 44.69999885559082|
|{2026-04-05 20:52...|        2|23.145555708143448| 46.88333405388726|
|{2026-04-05 20:48...|        9| 26.41249990463257| 49.49499988555908|
|{2026-04-05 20:53...|        1|24.473333994547527| 57.21333440144857|
|{2026-04-05 20:48...|        4|23.119999885559082| 40.52499961853027|
|{2026-04-05 20:52...|        6| 23.17599983215332|  58.1239990234375|
|{2026-04-05 20:46...|        9| 25.33714267185756| 50.10857173374721|
+--------------------+---------+------------------+------------------+
only showing top 20 rows

-------------------------------------------
Batch: 60
-------------------------------------------
+--------------------+---------+------------------+------------------+
|              window|sensor_id|  avg(temperature)|     avg(humidity)|
+--------------------+---------+------------------+------------------+
|{2026-04-05 20:49...|        1| 25.13999993460519|47.377143314906526|
|{2026-04-05 20:50...|        7|27.485000133514404| 49.27750015258789|
|{2026-04-05 20:51...|        1|  25.1233336130778| 56.85333251953125|
|{2026-04-05 20:44...|       10| 25.44999967302595| 58.24571337018694|
|{2026-04-05 20:49...|        7|25.492500066757202| 49.00125026702881|
|{2026-04-05 20:44...|        4|22.956666310628254|  50.7933349609375|
|{2026-04-05 20:48...|        6| 25.18624997138977| 49.51875066757202|
|{2026-04-05 20:51...|        8| 24.41333262125651| 57.70666631062826|
|{2026-04-05 20:45...|        9|22.821249961853027| 43.34499979019165|
|{2026-04-05 20:51...|        7|22.191428593226842| 54.69142859322684|
|{2026-04-05 20:44...|        5|20.757500171661377|50.334999084472656|
|{2026-04-05 20:44...|        2|25.065714154924667| 53.86857114519392|
|{2026-04-05 20:49...|        8|23.043333371480305|  51.6216672261556|
|{2026-04-05 20:50...|        8|26.460000038146973| 44.69999885559082|
|{2026-04-05 20:52...|        2|23.145555708143448| 46.88333405388726|
|{2026-04-05 20:48...|        9| 26.41249990463257| 49.49499988555908|
|{2026-04-05 20:53...|        1|24.473333994547527| 57.21333440144857|
|{2026-04-05 20:48...|        4|23.119999885559082| 40.52499961853027|
|{2026-04-05 20:52...|        6| 23.17599983215332|  58.1239990234375|
|{2026-04-05 20:46...|        9| 25.33714267185756| 50.10857173374721|
+--------------------+---------+------------------+------------------+
only showing top 20 rows

-------------------------------------------
Batch: 61
-------------------------------------------
+--------------------+---------+------------------+------------------+
|              window|sensor_id|  avg(temperature)|     avg(humidity)|
+--------------------+---------+------------------+------------------+
|{2026-04-05 20:49...|        1| 25.13999993460519|47.377143314906526|
|{2026-04-05 20:50...|        7|27.485000133514404| 49.27750015258789|
|{2026-04-05 20:51...|        1|  25.1233336130778| 56.85333251953125|
|{2026-04-05 20:44...|       10| 25.44999967302595| 58.24571337018694|
|{2026-04-05 20:49...|        7|25.492500066757202| 49.00125026702881|
|{2026-04-05 20:44...|        4|22.956666310628254|  50.7933349609375|
|{2026-04-05 20:48...|        6| 25.18624997138977| 49.51875066757202|
|{2026-04-05 20:51...|        8| 24.41333262125651| 57.70666631062826|
|{2026-04-05 20:45...|        9|22.821249961853027| 43.34499979019165|
|{2026-04-05 20:51...|        7|22.191428593226842| 54.69142859322684|
|{2026-04-05 20:44...|        5|20.757500171661377|50.334999084472656|
|{2026-04-05 20:44...|        2|25.065714154924667| 53.86857114519392|
|{2026-04-05 20:49...|        8|23.043333371480305|  51.6216672261556|
|{2026-04-05 20:50...|        8|26.460000038146973| 44.69999885559082|
|{2026-04-05 20:52...|        2|23.145555708143448| 46.88333405388726|
|{2026-04-05 20:48...|        9| 26.41249990463257| 49.49499988555908|
|{2026-04-05 20:53...|        1| 25.11400032043457| 52.02800064086914|
|{2026-04-05 20:48...|        4|23.119999885559082| 40.52499961853027|
|{2026-04-05 20:52...|        6| 23.17599983215332|  58.1239990234375|
|{2026-04-05 20:46...|        9| 25.33714267185756| 50.10857173374721|
+--------------------+---------+------------------+------------------+
only showing top 20 rows

-------------------------------------------
Batch: 62
-------------------------------------------
+--------------------+---------+------------------+------------------+
|              window|sensor_id|  avg(temperature)|     avg(humidity)|
+--------------------+---------+------------------+------------------+
|{2026-04-05 20:49...|        1| 25.13999993460519|47.377143314906526|
|{2026-04-05 20:50...|        7|27.485000133514404| 49.27750015258789|
|{2026-04-05 20:54...|        8|  29.8700008392334| 51.72999954223633|
|{2026-04-05 20:51...|        1|  25.1233336130778| 56.85333251953125|
|{2026-04-05 20:44...|       10| 25.44999967302595| 58.24571337018694|
|{2026-04-05 20:49...|        7|25.492500066757202| 49.00125026702881|
|{2026-04-05 20:54...|        2| 24.18000030517578|  31.6200008392334|
|{2026-04-05 20:44...|        4|22.956666310628254|  50.7933349609375|
|{2026-04-05 20:48...|        6| 25.18624997138977| 49.51875066757202|
|{2026-04-05 20:51...|        8| 24.41333262125651| 57.70666631062826|
|{2026-04-05 20:45...|        9|22.821249961853027| 43.34499979019165|
|{2026-04-05 20:51...|        7|22.191428593226842| 54.69142859322684|
|{2026-04-05 20:44...|        5|20.757500171661377|50.334999084472656|
|{2026-04-05 20:44...|        2|25.065714154924667| 53.86857114519392|
|{2026-04-05 20:49...|        8|23.043333371480305|  51.6216672261556|
|{2026-04-05 20:50...|        8|26.460000038146973| 44.69999885559082|
|{2026-04-05 20:52...|        2|23.145555708143448| 46.88333405388726|
|{2026-04-05 20:48...|        9| 26.41249990463257| 49.49499988555908|
|{2026-04-05 20:53...|        1| 25.11400032043457| 52.02800064086914|
|{2026-04-05 20:48...|        4|23.119999885559082| 40.52499961853027|
+--------------------+---------+------------------+------------------+
only showing top 20 rows

-------------------------------------------
Batch: 63
-------------------------------------------
+--------------------+---------+------------------+------------------+
|              window|sensor_id|  avg(temperature)|     avg(humidity)|
+--------------------+---------+------------------+------------------+
|{2026-04-05 20:49...|        1| 25.13999993460519|47.377143314906526|
|{2026-04-05 20:50...|        7|27.485000133514404| 49.27750015258789|
|{2026-04-05 20:54...|        8|  29.8700008392334| 51.72999954223633|
|{2026-04-05 20:51...|        1|  25.1233336130778| 56.85333251953125|
|{2026-04-05 20:44...|       10| 25.44999967302595| 58.24571337018694|
|{2026-04-05 20:49...|        7|25.492500066757202| 49.00125026702881|
|{2026-04-05 20:54...|        2|26.005000114440918|  37.1850004196167|
|{2026-04-05 20:44...|        4|22.956666310628254|  50.7933349609375|
|{2026-04-05 20:48...|        6| 25.18624997138977| 49.51875066757202|
|{2026-04-05 20:51...|        8| 24.41333262125651| 57.70666631062826|
|{2026-04-05 20:45...|        9|22.821249961853027| 43.34499979019165|
|{2026-04-05 20:51...|        7|22.191428593226842| 54.69142859322684|
|{2026-04-05 20:44...|        5|20.757500171661377|50.334999084472656|
|{2026-04-05 20:44...|        2|25.065714154924667| 53.86857114519392|
|{2026-04-05 20:49...|        8|23.043333371480305|  51.6216672261556|
|{2026-04-05 20:50...|        8|26.460000038146973| 44.69999885559082|
|{2026-04-05 20:52...|        2|23.145555708143448| 46.88333405388726|
|{2026-04-05 20:48...|        9| 26.41249990463257| 49.49499988555908|
|{2026-04-05 20:53...|        1| 25.11400032043457| 52.02800064086914|
|{2026-04-05 20:48...|        4|23.119999885559082| 40.52499961853027|
+--------------------+---------+------------------+------------------+
only showing top 20 rows

-------------------------------------------
Batch: 64
-------------------------------------------
+--------------------+---------+------------------+------------------+
|              window|sensor_id|  avg(temperature)|     avg(humidity)|
+--------------------+---------+------------------+------------------+
|{2026-04-05 20:49...|        1| 25.13999993460519|47.377143314906526|
|{2026-04-05 20:50...|        7|27.485000133514404| 49.27750015258789|
|{2026-04-05 20:54...|        8|  29.8700008392334| 51.72999954223633|
|{2026-04-05 20:51...|        1|  25.1233336130778| 56.85333251953125|
|{2026-04-05 20:44...|       10| 25.44999967302595| 58.24571337018694|
|{2026-04-05 20:49...|        7|25.492500066757202| 49.00125026702881|
|{2026-04-05 20:54...|        2|24.342000198364257|50.579999923706055|
|{2026-04-05 20:44...|        4|22.956666310628254|  50.7933349609375|
|{2026-04-05 20:48...|        6| 25.18624997138977| 49.51875066757202|
|{2026-04-05 20:51...|        8| 24.41333262125651| 57.70666631062826|
|{2026-04-05 20:45...|        9|22.821249961853027| 43.34499979019165|
|{2026-04-05 20:51...|        7|22.191428593226842| 54.69142859322684|
|{2026-04-05 20:44...|        5|20.757500171661377|50.334999084472656|
|{2026-04-05 20:44...|        2|25.065714154924667| 53.86857114519392|
|{2026-04-05 20:49...|        8|23.043333371480305|  51.6216672261556|
|{2026-04-05 20:50...|        8|26.460000038146973| 44.69999885559082|
|{2026-04-05 20:52...|        2|23.145555708143448| 46.88333405388726|
|{2026-04-05 20:48...|        9| 26.41249990463257| 49.49499988555908|
|{2026-04-05 20:53...|        1| 25.11400032043457| 52.02800064086914|
|{2026-04-05 20:48...|        4|23.119999885559082| 40.52499961853027|
+--------------------+---------+------------------+------------------+
only showing top 20 rows

-------------------------------------------
Batch: 65
-------------------------------------------
+--------------------+---------+------------------+------------------+
|              window|sensor_id|  avg(temperature)|     avg(humidity)|
+--------------------+---------+------------------+------------------+
|{2026-04-05 20:49...|        1| 25.13999993460519|47.377143314906526|
|{2026-04-05 20:50...|        7|27.485000133514404| 49.27750015258789|
|{2026-04-05 20:54...|        8|27.163333892822266| 50.22333272298177|
|{2026-04-05 20:51...|        1|  25.1233336130778| 56.85333251953125|
|{2026-04-05 20:44...|       10| 25.44999967302595| 58.24571337018694|
|{2026-04-05 20:49...|        7|25.492500066757202| 49.00125026702881|
|{2026-04-05 20:54...|        2|24.342000198364257|50.579999923706055|
|{2026-04-05 20:44...|        4|22.956666310628254|  50.7933349609375|
|{2026-04-05 20:48...|        6| 25.18624997138977| 49.51875066757202|
|{2026-04-05 20:51...|        8| 24.41333262125651| 57.70666631062826|
|{2026-04-05 20:45...|        9|22.821249961853027| 43.34499979019165|
|{2026-04-05 20:51...|        7|22.191428593226842| 54.69142859322684|
|{2026-04-05 20:44...|        5|20.757500171661377|50.334999084472656|
|{2026-04-05 20:44...|        2|25.065714154924667| 53.86857114519392|
|{2026-04-05 20:49...|        8|23.043333371480305|  51.6216672261556|
|{2026-04-05 20:50...|        8|26.460000038146973| 44.69999885559082|
|{2026-04-05 20:52...|        2|23.145555708143448| 46.88333405388726|
|{2026-04-05 20:48...|        9| 26.41249990463257| 49.49499988555908|
|{2026-04-05 20:53...|        1| 25.11400032043457| 52.02800064086914|
|{2026-04-05 20:48...|        4|23.119999885559082| 40.52499961853027|
+--------------------+---------+------------------+------------------+
only showing top 20 rows

-------------------------------------------
Batch: 66
-------------------------------------------
+--------------------+---------+------------------+------------------+
|              window|sensor_id|  avg(temperature)|     avg(humidity)|
+--------------------+---------+------------------+------------------+
|{2026-04-05 20:49...|        1| 25.13999993460519|47.377143314906526|
|{2026-04-05 20:50...|        7|27.485000133514404| 49.27750015258789|
|{2026-04-05 20:54...|        8|26.167500495910645|50.964999198913574|
|{2026-04-05 20:51...|        1|  25.1233336130778| 56.85333251953125|
|{2026-04-05 20:44...|       10| 25.44999967302595| 58.24571337018694|
|{2026-04-05 20:49...|        7|25.492500066757202| 49.00125026702881|
|{2026-04-05 20:54...|        2|25.010000228881836| 53.00666650136312|
|{2026-04-05 20:44...|        4|22.956666310628254|  50.7933349609375|
|{2026-04-05 20:48...|        6| 25.18624997138977| 49.51875066757202|
|{2026-04-05 20:51...|        8| 24.41333262125651| 57.70666631062826|
|{2026-04-05 20:45...|        9|22.821249961853027| 43.34499979019165|
|{2026-04-05 20:51...|        7|22.191428593226842| 54.69142859322684|
|{2026-04-05 20:44...|        5|20.757500171661377|50.334999084472656|
|{2026-04-05 20:44...|        2|25.065714154924667| 53.86857114519392|
|{2026-04-05 20:49...|        8|23.043333371480305|  51.6216672261556|
|{2026-04-05 20:50...|        8|26.460000038146973| 44.69999885559082|
|{2026-04-05 20:52...|        2|23.145555708143448| 46.88333405388726|
|{2026-04-05 20:48...|        9| 26.41249990463257| 49.49499988555908|
|{2026-04-05 20:53...|        1| 25.11400032043457| 52.02800064086914|
|{2026-04-05 20:48...|        4|23.119999885559082| 40.52499961853027|
+--------------------+---------+------------------+------------------+
only showing top 20 rows

-------------------------------------------
Batch: 67
-------------------------------------------
+--------------------+---------+------------------+------------------+
|              window|sensor_id|  avg(temperature)|     avg(humidity)|
+--------------------+---------+------------------+------------------+
|{2026-04-05 20:49...|        1| 25.13999993460519|47.377143314906526|
|{2026-04-05 20:50...|        7|27.485000133514404| 49.27750015258789|
|{2026-04-05 20:54...|        8|25.752000427246095| 52.13399963378906|
|{2026-04-05 20:51...|        1|  25.1233336130778| 56.85333251953125|
|{2026-04-05 20:44...|       10| 25.44999967302595| 58.24571337018694|
|{2026-04-05 20:49...|        7|25.492500066757202| 49.00125026702881|
|{2026-04-05 20:54...|        2|25.121428898402623|53.489999771118164|
|{2026-04-05 20:44...|        4|22.956666310628254|  50.7933349609375|
|{2026-04-05 20:48...|        6| 25.18624997138977| 49.51875066757202|
|{2026-04-05 20:51...|        8| 24.41333262125651| 57.70666631062826|
|{2026-04-05 20:45...|        9|22.821249961853027| 43.34499979019165|
|{2026-04-05 20:51...|        7|22.191428593226842| 54.69142859322684|
|{2026-04-05 20:44...|        5|20.757500171661377|50.334999084472656|
|{2026-04-05 20:44...|        2|25.065714154924667| 53.86857114519392|
|{2026-04-05 20:49...|        8|23.043333371480305|  51.6216672261556|
|{2026-04-05 20:50...|        8|26.460000038146973| 44.69999885559082|
|{2026-04-05 20:52...|        2|23.145555708143448| 46.88333405388726|
|{2026-04-05 20:48...|        9| 26.41249990463257| 49.49499988555908|
|{2026-04-05 20:53...|        1| 25.11400032043457| 52.02800064086914|
|{2026-04-05 20:48...|        4|23.119999885559082| 40.52499961853027|
+--------------------+---------+------------------+------------------+
only showing top 20 rows

-------------------------------------------
Batch: 68
-------------------------------------------
+--------------------+---------+------------------+------------------+
|              window|sensor_id|  avg(temperature)|     avg(humidity)|
+--------------------+---------+------------------+------------------+
|{2026-04-05 20:49...|        1| 25.13999993460519|47.377143314906526|
|{2026-04-05 20:50...|        7|27.485000133514404| 49.27750015258789|
|{2026-04-05 20:54...|        8|25.752000427246095| 52.13399963378906|
|{2026-04-05 20:51...|        1|  25.1233336130778| 56.85333251953125|
|{2026-04-05 20:44...|       10| 25.44999967302595| 58.24571337018694|
|{2026-04-05 20:49...|        7|25.492500066757202| 49.00125026702881|
|{2026-04-05 20:55...|       10|24.503333409627277|59.620001475016274|
|{2026-04-05 20:54...|        2|25.121428898402623|53.489999771118164|
|{2026-04-05 20:44...|        4|22.956666310628254|  50.7933349609375|
|{2026-04-05 20:48...|        6| 25.18624997138977| 49.51875066757202|
|{2026-04-05 20:51...|        8| 24.41333262125651| 57.70666631062826|
|{2026-04-05 20:45...|        9|22.821249961853027| 43.34499979019165|
|{2026-04-05 20:51...|        7|22.191428593226842| 54.69142859322684|
|{2026-04-05 20:44...|        5|20.757500171661377|50.334999084472656|
|{2026-04-05 20:44...|        2|25.065714154924667| 53.86857114519392|
|{2026-04-05 20:49...|        8|23.043333371480305|  51.6216672261556|
|{2026-04-05 20:50...|        8|26.460000038146973| 44.69999885559082|
|{2026-04-05 20:52...|        2|23.145555708143448| 46.88333405388726|
|{2026-04-05 20:48...|        9| 26.41249990463257| 49.49499988555908|
|{2026-04-05 20:53...|        1| 25.11400032043457| 52.02800064086914|
+--------------------+---------+------------------+------------------+
only showing top 20 rows

-------------------------------------------
Batch: 69
-------------------------------------------
+--------------------+---------+------------------+------------------+
|              window|sensor_id|  avg(temperature)|     avg(humidity)|
+--------------------+---------+------------------+------------------+
|{2026-04-05 20:49...|        1| 25.13999993460519|47.377143314906526|
|{2026-04-05 20:50...|        7|27.485000133514404| 49.27750015258789|
|{2026-04-05 20:54...|        8|25.752000427246095| 52.13399963378906|
|{2026-04-05 20:51...|        1|  25.1233336130778| 56.85333251953125|
|{2026-04-05 20:44...|       10| 25.44999967302595| 58.24571337018694|
|{2026-04-05 20:49...|        7|25.492500066757202| 49.00125026702881|
|{2026-04-05 20:55...|       10|25.361666679382324|53.793334325154625|
|{2026-04-05 20:54...|        2|25.121428898402623|53.489999771118164|
|{2026-04-05 20:44...|        4|22.956666310628254|  50.7933349609375|
|{2026-04-05 20:48...|        6| 25.18624997138977| 49.51875066757202|
|{2026-04-05 20:51...|        8| 24.41333262125651| 57.70666631062826|
|{2026-04-05 20:45...|        9|22.821249961853027| 43.34499979019165|
|{2026-04-05 20:51...|        7|22.191428593226842| 54.69142859322684|
|{2026-04-05 20:44...|        5|20.757500171661377|50.334999084472656|
|{2026-04-05 20:44...|        2|25.065714154924667| 53.86857114519392|
|{2026-04-05 20:49...|        8|23.043333371480305|  51.6216672261556|
|{2026-04-05 20:50...|        8|26.460000038146973| 44.69999885559082|
|{2026-04-05 20:52...|        2|23.145555708143448| 46.88333405388726|
|{2026-04-05 20:48...|        9| 26.41249990463257| 49.49499988555908|
|{2026-04-05 20:53...|        1| 25.11400032043457| 52.02800064086914|
+--------------------+---------+------------------+------------------+
only showing top 20 rows

-------------------------------------------
Batch: 70
-------------------------------------------
+--------------------+---------+------------------+------------------+
|              window|sensor_id|  avg(temperature)|     avg(humidity)|
+--------------------+---------+------------------+------------------+
|{2026-04-05 20:49...|        1| 25.13999993460519|47.377143314906526|
|{2026-04-05 20:50...|        7|27.485000133514404| 49.27750015258789|
|{2026-04-05 20:54...|        8|25.752000427246095| 52.13399963378906|
|{2026-04-05 20:51...|        1|  25.1233336130778| 56.85333251953125|
|{2026-04-05 20:44...|       10| 25.44999967302595| 58.24571337018694|
|{2026-04-05 20:49...|        7|25.492500066757202| 49.00125026702881|
|{2026-04-05 20:55...|       10|25.178571428571427|53.135714939662385|
|{2026-04-05 20:54...|        2|25.121428898402623|53.489999771118164|
|{2026-04-05 20:44...|        4|22.956666310628254|  50.7933349609375|
|{2026-04-05 20:48...|        6| 25.18624997138977| 49.51875066757202|
|{2026-04-05 20:51...|        8| 24.41333262125651| 57.70666631062826|
|{2026-04-05 20:45...|        9|22.821249961853027| 43.34499979019165|
|{2026-04-05 20:51...|        7|22.191428593226842| 54.69142859322684|
|{2026-04-05 20:44...|        5|20.757500171661377|50.334999084472656|
|{2026-04-05 20:44...|        2|25.065714154924667| 53.86857114519392|
|{2026-04-05 20:49...|        8|23.043333371480305|  51.6216672261556|
|{2026-04-05 20:50...|        8|26.460000038146973| 44.69999885559082|
|{2026-04-05 20:52...|        2|23.145555708143448| 46.88333405388726|
|{2026-04-05 20:48...|        9| 26.41249990463257| 49.49499988555908|
|{2026-04-05 20:53...|        1| 25.11400032043457| 52.02800064086914|
+--------------------+---------+------------------+------------------+
only showing top 20 rows

-------------------------------------------
Batch: 71
-------------------------------------------
+--------------------+---------+------------------+------------------+
|              window|sensor_id|  avg(temperature)|     avg(humidity)|
+--------------------+---------+------------------+------------------+
|{2026-04-05 20:49...|        1| 25.13999993460519|47.377143314906526|
|{2026-04-05 20:50...|        7|27.485000133514404| 49.27750015258789|
|{2026-04-05 20:54...|        8|25.752000427246095| 52.13399963378906|
|{2026-04-05 20:51...|        1|  25.1233336130778| 56.85333251953125|
|{2026-04-05 20:44...|       10| 25.44999967302595| 58.24571337018694|
|{2026-04-05 20:49...|        7|25.492500066757202| 49.00125026702881|
|{2026-04-05 20:55...|       10| 25.15249991416931|54.355000495910645|
|{2026-04-05 20:54...|        2|25.121428898402623|53.489999771118164|
|{2026-04-05 20:44...|        4|22.956666310628254|  50.7933349609375|
|{2026-04-05 20:48...|        6| 25.18624997138977| 49.51875066757202|
|{2026-04-05 20:51...|        8| 24.41333262125651| 57.70666631062826|
|{2026-04-05 20:45...|        9|22.821249961853027| 43.34499979019165|
|{2026-04-05 20:51...|        7|22.191428593226842| 54.69142859322684|
|{2026-04-05 20:44...|        5|20.757500171661377|50.334999084472656|
|{2026-04-05 20:44...|        2|25.065714154924667| 53.86857114519392|
|{2026-04-05 20:49...|        8|23.043333371480305|  51.6216672261556|
|{2026-04-05 20:50...|        8|26.460000038146973| 44.69999885559082|
|{2026-04-05 20:52...|        2|23.145555708143448| 46.88333405388726|
|{2026-04-05 20:48...|        9| 26.41249990463257| 49.49499988555908|
|{2026-04-05 20:53...|        1| 25.11400032043457| 52.02800064086914|
+--------------------+---------+------------------+------------------+
only showing top 20 rows

-------------------------------------------
Batch: 72
-------------------------------------------
+--------------------+---------+------------------+------------------+
|              window|sensor_id|  avg(temperature)|     avg(humidity)|
+--------------------+---------+------------------+------------------+
|{2026-04-05 20:49...|        1| 25.13999993460519|47.377143314906526|
|{2026-04-05 20:50...|        7|27.485000133514404| 49.27750015258789|
|{2026-04-05 20:54...|        8|25.752000427246095| 52.13399963378906|
|{2026-04-05 20:51...|        1|  25.1233336130778| 56.85333251953125|
|{2026-04-05 20:44...|       10| 25.44999967302595| 58.24571337018694|
|{2026-04-05 20:49...|        7|25.492500066757202| 49.00125026702881|
|{2026-04-05 20:55...|       10|25.642222086588543| 54.53666729397244|
|{2026-04-05 20:54...|        2|25.121428898402623|53.489999771118164|
|{2026-04-05 20:44...|        4|22.956666310628254|  50.7933349609375|
|{2026-04-05 20:48...|        6| 25.18624997138977| 49.51875066757202|
|{2026-04-05 20:51...|        8| 24.41333262125651| 57.70666631062826|
|{2026-04-05 20:45...|        9|22.821249961853027| 43.34499979019165|
|{2026-04-05 20:51...|        7|22.191428593226842| 54.69142859322684|
|{2026-04-05 20:44...|        5|20.757500171661377|50.334999084472656|
|{2026-04-05 20:44...|        2|25.065714154924667| 53.86857114519392|
|{2026-04-05 20:49...|        8|23.043333371480305|  51.6216672261556|
|{2026-04-05 20:50...|        8|26.460000038146973| 44.69999885559082|
|{2026-04-05 20:52...|        2|23.145555708143448| 46.88333405388726|
|{2026-04-05 20:48...|        9| 26.41249990463257| 49.49499988555908|
|{2026-04-05 20:53...|        1| 25.11400032043457| 52.02800064086914|
+--------------------+---------+------------------+------------------+
only showing top 20 rows

-------------------------------------------
Batch: 73
-------------------------------------------
+--------------------+---------+------------------+------------------+
|              window|sensor_id|  avg(temperature)|     avg(humidity)|
+--------------------+---------+------------------+------------------+
|{2026-04-05 20:49...|        1| 25.13999993460519|47.377143314906526|
|{2026-04-05 20:50...|        7|27.485000133514404| 49.27750015258789|
|{2026-04-05 20:54...|        8|25.752000427246095| 52.13399963378906|
|{2026-04-05 20:51...|        1|  25.1233336130778| 56.85333251953125|
|{2026-04-05 20:44...|       10| 25.44999967302595| 58.24571337018694|
|{2026-04-05 20:49...|        7|25.492500066757202| 49.00125026702881|
|{2026-04-05 20:55...|       10|25.135999870300292|55.971000289916994|
|{2026-04-05 20:54...|        2|25.121428898402623|53.489999771118164|
|{2026-04-05 20:44...|        4|22.956666310628254|  50.7933349609375|
|{2026-04-05 20:48...|        6| 25.18624997138977| 49.51875066757202|
|{2026-04-05 20:51...|        8| 24.41333262125651| 57.70666631062826|
|{2026-04-05 20:45...|        9|22.821249961853027| 43.34499979019165|
|{2026-04-05 20:51...|        7|22.191428593226842| 54.69142859322684|
|{2026-04-05 20:44...|        5|20.757500171661377|50.334999084472656|
|{2026-04-05 20:44...|        2|25.065714154924667| 53.86857114519392|
|{2026-04-05 20:49...|        8|23.043333371480305|  51.6216672261556|
|{2026-04-05 20:50...|        8|26.460000038146973| 44.69999885559082|
|{2026-04-05 20:52...|        2|23.145555708143448| 46.88333405388726|
|{2026-04-05 20:48...|        9| 26.41249990463257| 49.49499988555908|
|{2026-04-05 20:53...|        1| 25.11400032043457| 52.02800064086914|
+--------------------+---------+------------------+------------------+
only showing top 20 rows

-------------------------------------------
Batch: 74
-------------------------------------------
+--------------------+---------+------------------+------------------+
|              window|sensor_id|  avg(temperature)|     avg(humidity)|
+--------------------+---------+------------------+------------------+
|{2026-04-05 20:49...|        1| 25.13999993460519|47.377143314906526|
|{2026-04-05 20:50...|        7|27.485000133514404| 49.27750015258789|
|{2026-04-05 20:54...|        8|25.752000427246095| 52.13399963378906|
|{2026-04-05 20:51...|        1|  25.1233336130778| 56.85333251953125|
|{2026-04-05 20:44...|       10| 25.44999967302595| 58.24571337018694|
|{2026-04-05 20:49...|        7|25.492500066757202| 49.00125026702881|
|{2026-04-05 20:55...|       10|25.135999870300292|55.971000289916994|
|{2026-04-05 20:54...|        2|25.121428898402623|53.489999771118164|
|{2026-04-05 20:44...|        4|22.956666310628254|  50.7933349609375|
|{2026-04-05 20:48...|        6| 25.18624997138977| 49.51875066757202|
|{2026-04-05 20:56...|       10|20.440000534057617|  51.9900016784668|
|{2026-04-05 20:51...|        8| 24.41333262125651| 57.70666631062826|
|{2026-04-05 20:45...|        9|22.821249961853027| 43.34499979019165|
|{2026-04-05 20:51...|        7|22.191428593226842| 54.69142859322684|
|{2026-04-05 20:44...|        5|20.757500171661377|50.334999084472656|
|{2026-04-05 20:44...|        2|25.065714154924667| 53.86857114519392|
|{2026-04-05 20:49...|        8|23.043333371480305|  51.6216672261556|
|{2026-04-05 20:50...|        8|26.460000038146973| 44.69999885559082|
|{2026-04-05 20:52...|        2|23.145555708143448| 46.88333405388726|
|{2026-04-05 20:48...|        9| 26.41249990463257| 49.49499988555908|
+--------------------+---------+------------------+------------------+
only showing top 20 rows

-------------------------------------------
Batch: 75
-------------------------------------------
+--------------------+---------+------------------+------------------+
|              window|sensor_id|  avg(temperature)|     avg(humidity)|
+--------------------+---------+------------------+------------------+
|{2026-04-05 20:49...|        1| 25.13999993460519|47.377143314906526|
|{2026-04-05 20:50...|        7|27.485000133514404| 49.27750015258789|
|{2026-04-05 20:54...|        8|25.752000427246095| 52.13399963378906|
|{2026-04-05 20:51...|        1|  25.1233336130778| 56.85333251953125|
|{2026-04-05 20:44...|       10| 25.44999967302595| 58.24571337018694|
|{2026-04-05 20:49...|        7|25.492500066757202| 49.00125026702881|
|{2026-04-05 20:55...|       10|25.135999870300292|55.971000289916994|
|{2026-04-05 20:54...|        2|25.121428898402623|53.489999771118164|
|{2026-04-05 20:44...|        4|22.956666310628254|  50.7933349609375|
|{2026-04-05 20:48...|        6| 25.18624997138977| 49.51875066757202|
|{2026-04-05 20:56...|       10|20.440000534057617|  51.9900016784668|
|{2026-04-05 20:51...|        8| 24.41333262125651| 57.70666631062826|
|{2026-04-05 20:45...|        9|22.821249961853027| 43.34499979019165|
|{2026-04-05 20:51...|        7|22.191428593226842| 54.69142859322684|
|{2026-04-05 20:44...|        5|20.757500171661377|50.334999084472656|
|{2026-04-05 20:44...|        2|25.065714154924667| 53.86857114519392|
|{2026-04-05 20:49...|        8|23.043333371480305|  51.6216672261556|
|{2026-04-05 20:50...|        8|26.460000038146973| 44.69999885559082|
|{2026-04-05 20:52...|        2|23.145555708143448| 46.88333405388726|
|{2026-04-05 20:48...|        9| 26.41249990463257| 49.49499988555908|
+--------------------+---------+------------------+------------------+
only showing top 20 rows

-------------------------------------------
Batch: 76
-------------------------------------------
+--------------------+---------+------------------+------------------+
|              window|sensor_id|  avg(temperature)|     avg(humidity)|
+--------------------+---------+------------------+------------------+
|{2026-04-05 20:49...|        1| 25.13999993460519|47.377143314906526|
|{2026-04-05 20:50...|        7|27.485000133514404| 49.27750015258789|
|{2026-04-05 20:54...|        8|25.752000427246095| 52.13399963378906|
|{2026-04-05 20:51...|        1|  25.1233336130778| 56.85333251953125|
|{2026-04-05 20:44...|       10| 25.44999967302595| 58.24571337018694|
|{2026-04-05 20:49...|        7|25.492500066757202| 49.00125026702881|
|{2026-04-05 20:55...|       10|25.135999870300292|55.971000289916994|
|{2026-04-05 20:54...|        2|25.121428898402623|53.489999771118164|
|{2026-04-05 20:44...|        4|22.956666310628254|  50.7933349609375|
|{2026-04-05 20:48...|        6| 25.18624997138977| 49.51875066757202|
|{2026-04-05 20:56...|       10|20.440000534057617|  51.9900016784668|
|{2026-04-05 20:51...|        8| 24.41333262125651| 57.70666631062826|
|{2026-04-05 20:45...|        9|22.821249961853027| 43.34499979019165|
|{2026-04-05 20:51...|        7|22.191428593226842| 54.69142859322684|
|{2026-04-05 20:44...|        5|20.757500171661377|50.334999084472656|
|{2026-04-05 20:44...|        2|25.065714154924667| 53.86857114519392|
|{2026-04-05 20:49...|        8|23.043333371480305|  51.6216672261556|
|{2026-04-05 20:50...|        8|26.460000038146973| 44.69999885559082|
|{2026-04-05 20:52...|        2|23.145555708143448| 46.88333405388726|
|{2026-04-05 20:48...|        9| 26.41249990463257| 49.49499988555908|
+--------------------+---------+------------------+------------------+
only showing top 20 rows

-------------------------------------------
Batch: 77
-------------------------------------------
+--------------------+---------+------------------+------------------+
|              window|sensor_id|  avg(temperature)|     avg(humidity)|
+--------------------+---------+------------------+------------------+
|{2026-04-05 20:49...|        1| 25.13999993460519|47.377143314906526|
|{2026-04-05 20:50...|        7|27.485000133514404| 49.27750015258789|
|{2026-04-05 20:54...|        8|25.752000427246095| 52.13399963378906|
|{2026-04-05 20:51...|        1|  25.1233336130778| 56.85333251953125|
|{2026-04-05 20:44...|       10| 25.44999967302595| 58.24571337018694|
|{2026-04-05 20:49...|        7|25.492500066757202| 49.00125026702881|
|{2026-04-05 20:55...|       10|25.135999870300292|55.971000289916994|
|{2026-04-05 20:54...|        2|25.121428898402623|53.489999771118164|
|{2026-04-05 20:44...|        4|22.956666310628254|  50.7933349609375|
|{2026-04-05 20:48...|        6| 25.18624997138977| 49.51875066757202|
|{2026-04-05 20:56...|       10|20.440000534057617|  51.9900016784668|
|{2026-04-05 20:51...|        8| 24.41333262125651| 57.70666631062826|
|{2026-04-05 20:45...|        9|22.821249961853027| 43.34499979019165|
|{2026-04-05 20:51...|        7|22.191428593226842| 54.69142859322684|
|{2026-04-05 20:44...|        5|20.757500171661377|50.334999084472656|
|{2026-04-05 20:44...|        2|25.065714154924667| 53.86857114519392|
|{2026-04-05 20:49...|        8|23.043333371480305|  51.6216672261556|
|{2026-04-05 20:50...|        8|26.460000038146973| 44.69999885559082|
|{2026-04-05 20:52...|        2|23.145555708143448| 46.88333405388726|
|{2026-04-05 20:48...|        9| 26.41249990463257| 49.49499988555908|
+--------------------+---------+------------------+------------------+
only showing top 20 rows

-------------------------------------------
Batch: 78
-------------------------------------------
+--------------------+---------+------------------+------------------+
|              window|sensor_id|  avg(temperature)|     avg(humidity)|
+--------------------+---------+------------------+------------------+
|{2026-04-05 20:49...|        1| 25.13999993460519|47.377143314906526|
|{2026-04-05 20:50...|        7|27.485000133514404| 49.27750015258789|
|{2026-04-05 20:54...|        8|25.752000427246095| 52.13399963378906|
|{2026-04-05 20:51...|        1|  25.1233336130778| 56.85333251953125|
|{2026-04-05 20:44...|       10| 25.44999967302595| 58.24571337018694|
|{2026-04-05 20:49...|        7|25.492500066757202| 49.00125026702881|
|{2026-04-05 20:55...|       10|25.135999870300292|55.971000289916994|
|{2026-04-05 20:54...|        2|25.121428898402623|53.489999771118164|
|{2026-04-05 20:44...|        4|22.956666310628254|  50.7933349609375|
|{2026-04-05 20:48...|        6| 25.18624997138977| 49.51875066757202|
|{2026-04-05 20:56...|       10|24.795000076293945| 46.71000099182129|
|{2026-04-05 20:51...|        8| 24.41333262125651| 57.70666631062826|
|{2026-04-05 20:45...|        9|22.821249961853027| 43.34499979019165|
|{2026-04-05 20:51...|        7|22.191428593226842| 54.69142859322684|
|{2026-04-05 20:44...|        5|20.757500171661377|50.334999084472656|
|{2026-04-05 20:44...|        2|25.065714154924667| 53.86857114519392|
|{2026-04-05 20:49...|        8|23.043333371480305|  51.6216672261556|
|{2026-04-05 20:50...|        8|26.460000038146973| 44.69999885559082|
|{2026-04-05 20:52...|        2|23.145555708143448| 46.88333405388726|
|{2026-04-05 20:48...|        9| 26.41249990463257| 49.49499988555908|
+--------------------+---------+------------------+------------------+
only showing top 20 rows

-------------------------------------------
Batch: 79
-------------------------------------------
+--------------------+---------+------------------+------------------+
|              window|sensor_id|  avg(temperature)|     avg(humidity)|
+--------------------+---------+------------------+------------------+
|{2026-04-05 20:49...|        1| 25.13999993460519|47.377143314906526|
|{2026-04-05 20:50...|        7|27.485000133514404| 49.27750015258789|
|{2026-04-05 20:54...|        8|25.752000427246095| 52.13399963378906|
|{2026-04-05 20:51...|        1|  25.1233336130778| 56.85333251953125|
|{2026-04-05 20:44...|       10| 25.44999967302595| 58.24571337018694|
|{2026-04-05 20:49...|        7|25.492500066757202| 49.00125026702881|
|{2026-04-05 20:55...|       10|25.135999870300292|55.971000289916994|
|{2026-04-05 20:54...|        2|25.121428898402623|53.489999771118164|
|{2026-04-05 20:44...|        4|22.956666310628254|  50.7933349609375|
|{2026-04-05 20:48...|        6| 25.18624997138977| 49.51875066757202|
|{2026-04-05 20:56...|       10|26.073333104451496|53.173333485921226|
|{2026-04-05 20:51...|        8| 24.41333262125651| 57.70666631062826|
|{2026-04-05 20:45...|        9|22.821249961853027| 43.34499979019165|
|{2026-04-05 20:51...|        7|22.191428593226842| 54.69142859322684|
|{2026-04-05 20:44...|        5|20.757500171661377|50.334999084472656|
|{2026-04-05 20:44...|        2|25.065714154924667| 53.86857114519392|
|{2026-04-05 20:49...|        8|23.043333371480305|  51.6216672261556|
|{2026-04-05 20:50...|        8|26.460000038146973| 44.69999885559082|
|{2026-04-05 20:52...|        2|23.145555708143448| 46.88333405388726|
|{2026-04-05 20:48...|        9| 26.41249990463257| 49.49499988555908|
+--------------------+---------+------------------+------------------+
only showing top 20 rows

-------------------------------------------
Batch: 80
-------------------------------------------
+--------------------+---------+------------------+------------------+
|              window|sensor_id|  avg(temperature)|     avg(humidity)|
+--------------------+---------+------------------+------------------+
|{2026-04-05 20:57...|        8|29.049999237060547|47.470001220703125|
|{2026-04-05 20:49...|        1| 25.13999993460519|47.377143314906526|
|{2026-04-05 20:50...|        7|27.485000133514404| 49.27750015258789|
|{2026-04-05 20:54...|        8|25.752000427246095| 52.13399963378906|
|{2026-04-05 20:51...|        1|  25.1233336130778| 56.85333251953125|
|{2026-04-05 20:44...|       10| 25.44999967302595| 58.24571337018694|
|{2026-04-05 20:49...|        7|25.492500066757202| 49.00125026702881|
|{2026-04-05 20:55...|       10|25.135999870300292|55.971000289916994|
|{2026-04-05 20:57...|       10|28.059999465942383| 46.43499946594238|
|{2026-04-05 20:57...|        9|25.100000381469727|61.779998779296875|
|{2026-04-05 20:54...|        2|25.121428898402623|53.489999771118164|
|{2026-04-05 20:44...|        4|22.956666310628254|  50.7933349609375|
|{2026-04-05 20:48...|        6| 25.18624997138977| 49.51875066757202|
|{2026-04-05 20:56...|       10|26.073333104451496|53.173333485921226|
|{2026-04-05 20:51...|        8| 24.41333262125651| 57.70666631062826|
|{2026-04-05 20:45...|        9|22.821249961853027| 43.34499979019165|
|{2026-04-05 20:51...|        7|22.191428593226842| 54.69142859322684|
|{2026-04-05 20:44...|        5|20.757500171661377|50.334999084472656|
|{2026-04-05 20:44...|        2|25.065714154924667| 53.86857114519392|
|{2026-04-05 20:49...|        8|23.043333371480305|  51.6216672261556|
+--------------------+---------+------------------+------------------+
only showing top 20 rows

-------------------------------------------
Batch: 81
-------------------------------------------
+--------------------+---------+------------------+------------------+
|              window|sensor_id|  avg(temperature)|     avg(humidity)|
+--------------------+---------+------------------+------------------+
|{2026-04-05 20:57...|        8|28.893333435058594|47.460000356038414|
|{2026-04-05 20:49...|        1| 25.13999993460519|47.377143314906526|
|{2026-04-05 20:50...|        7|27.485000133514404| 49.27750015258789|
|{2026-04-05 20:54...|        8|25.752000427246095| 52.13399963378906|
|{2026-04-05 20:51...|        1|  25.1233336130778| 56.85333251953125|
|{2026-04-05 20:44...|       10| 25.44999967302595| 58.24571337018694|
|{2026-04-05 20:49...|        7|25.492500066757202| 49.00125026702881|
|{2026-04-05 20:55...|       10|25.135999870300292|55.971000289916994|
|{2026-04-05 20:57...|       10|28.323333104451496| 43.53666687011719|
|{2026-04-05 20:57...|        9|25.100000381469727|61.779998779296875|
|{2026-04-05 20:54...|        2|25.121428898402623|53.489999771118164|
|{2026-04-05 20:44...|        4|22.956666310628254|  50.7933349609375|
|{2026-04-05 20:48...|        6| 25.18624997138977| 49.51875066757202|
|{2026-04-05 20:56...|       10|26.073333104451496|53.173333485921226|
|{2026-04-05 20:51...|        8| 24.41333262125651| 57.70666631062826|
|{2026-04-05 20:45...|        9|22.821249961853027| 43.34499979019165|
|{2026-04-05 20:51...|        7|22.191428593226842| 54.69142859322684|
|{2026-04-05 20:44...|        5|20.757500171661377|50.334999084472656|
|{2026-04-05 20:44...|        2|25.065714154924667| 53.86857114519392|
|{2026-04-05 20:49...|        8|23.043333371480305|  51.6216672261556|
+--------------------+---------+------------------+------------------+
only showing top 20 rows

-------------------------------------------
Batch: 82
-------------------------------------------
+--------------------+---------+------------------+------------------+
|              window|sensor_id|  avg(temperature)|     avg(humidity)|
+--------------------+---------+------------------+------------------+
|{2026-04-05 20:57...|        8|  26.7120002746582|44.886000061035155|
|{2026-04-05 20:49...|        1| 25.13999993460519|47.377143314906526|
|{2026-04-05 20:50...|        7|27.485000133514404| 49.27750015258789|
|{2026-04-05 20:54...|        8|25.752000427246095| 52.13399963378906|
|{2026-04-05 20:51...|        1|  25.1233336130778| 56.85333251953125|
|{2026-04-05 20:44...|       10| 25.44999967302595| 58.24571337018694|
|{2026-04-05 20:49...|        7|25.492500066757202| 49.00125026702881|
|{2026-04-05 20:55...|       10|25.135999870300292|55.971000289916994|
|{2026-04-05 20:57...|       10|           26.5625| 44.18000030517578|
|{2026-04-05 20:57...|        9|26.392500400543213| 42.73249959945679|
|{2026-04-05 20:54...|        2|25.121428898402623|53.489999771118164|
|{2026-04-05 20:44...|        4|22.956666310628254|  50.7933349609375|
|{2026-04-05 20:48...|        6| 25.18624997138977| 49.51875066757202|
|{2026-04-05 20:56...|       10|26.073333104451496|53.173333485921226|
|{2026-04-05 20:51...|        8| 24.41333262125651| 57.70666631062826|
|{2026-04-05 20:45...|        9|22.821249961853027| 43.34499979019165|
|{2026-04-05 20:51...|        7|22.191428593226842| 54.69142859322684|
|{2026-04-05 20:44...|        5|20.757500171661377|50.334999084472656|
|{2026-04-05 20:44...|        2|25.065714154924667| 53.86857114519392|
|{2026-04-05 20:49...|        8|23.043333371480305|  51.6216672261556|
+--------------------+---------+------------------+------------------+
only showing top 20 rows

-------------------------------------------
Batch: 83
-------------------------------------------
+--------------------+---------+------------------+------------------+
|              window|sensor_id|  avg(temperature)|     avg(humidity)|
+--------------------+---------+------------------+------------------+
|{2026-04-05 20:57...|        8| 25.59666697184245| 44.65166664123535|
|{2026-04-05 20:49...|        1| 25.13999993460519|47.377143314906526|
|{2026-04-05 20:50...|        7|27.485000133514404| 49.27750015258789|
|{2026-04-05 20:54...|        8|25.752000427246095| 52.13399963378906|
|{2026-04-05 20:51...|        1|  25.1233336130778| 56.85333251953125|
|{2026-04-05 20:44...|       10| 25.44999967302595| 58.24571337018694|
|{2026-04-05 20:49...|        7|25.492500066757202| 49.00125026702881|
|{2026-04-05 20:55...|       10|25.135999870300292|55.971000289916994|
|{2026-04-05 20:57...|       10| 25.28400001525879| 47.77600021362305|
|{2026-04-05 20:57...|        9| 26.18500010172526| 50.66666634877523|
|{2026-04-05 20:54...|        2|25.121428898402623|53.489999771118164|
|{2026-04-05 20:44...|        4|22.956666310628254|  50.7933349609375|
|{2026-04-05 20:48...|        6| 25.18624997138977| 49.51875066757202|
|{2026-04-05 20:56...|       10|26.073333104451496|53.173333485921226|
|{2026-04-05 20:51...|        8| 24.41333262125651| 57.70666631062826|
|{2026-04-05 20:45...|        9|22.821249961853027| 43.34499979019165|
|{2026-04-05 20:51...|        7|22.191428593226842| 54.69142859322684|
|{2026-04-05 20:44...|        5|20.757500171661377|50.334999084472656|
|{2026-04-05 20:44...|        2|25.065714154924667| 53.86857114519392|
|{2026-04-05 20:49...|        8|23.043333371480305|  51.6216672261556|
+--------------------+---------+------------------+------------------+
only showing top 20 rows

-------------------------------------------
Batch: 84
-------------------------------------------
+--------------------+---------+------------------+------------------+
|              window|sensor_id|  avg(temperature)|     avg(humidity)|
+--------------------+---------+------------------+------------------+
|{2026-04-05 20:57...|        8| 25.54142870221819|45.334285736083984|
|{2026-04-05 20:49...|        1| 25.13999993460519|47.377143314906526|
|{2026-04-05 20:50...|        7|27.485000133514404| 49.27750015258789|
|{2026-04-05 20:54...|        8|25.752000427246095| 52.13399963378906|
|{2026-04-05 20:51...|        1|  25.1233336130778| 56.85333251953125|
|{2026-04-05 20:44...|       10| 25.44999967302595| 58.24571337018694|
|{2026-04-05 20:49...|        7|25.492500066757202| 49.00125026702881|
|{2026-04-05 20:55...|       10|25.135999870300292|55.971000289916994|
|{2026-04-05 20:57...|       10| 25.28400001525879| 47.77600021362305|
|{2026-04-05 20:57...|        9| 26.18500010172526| 50.66666634877523|
|{2026-04-05 20:54...|        2|25.121428898402623|53.489999771118164|
|{2026-04-05 20:44...|        4|22.956666310628254|  50.7933349609375|
|{2026-04-05 20:48...|        6| 25.18624997138977| 49.51875066757202|
|{2026-04-05 20:56...|       10|26.073333104451496|53.173333485921226|
|{2026-04-05 20:51...|        8| 24.41333262125651| 57.70666631062826|
|{2026-04-05 20:45...|        9|22.821249961853027| 43.34499979019165|
|{2026-04-05 20:51...|        7|22.191428593226842| 54.69142859322684|
|{2026-04-05 20:44...|        5|20.757500171661377|50.334999084472656|
|{2026-04-05 20:44...|        2|25.065714154924667| 53.86857114519392|
|{2026-04-05 20:49...|        8|23.043333371480305|  51.6216672261556|
+--------------------+---------+------------------+------------------+
only showing top 20 rows

-------------------------------------------
Batch: 85
-------------------------------------------
+--------------------+---------+------------------+------------------+
|              window|sensor_id|  avg(temperature)|     avg(humidity)|
+--------------------+---------+------------------+------------------+
|{2026-04-05 20:57...|        8| 25.54142870221819|45.334285736083984|
|{2026-04-05 20:49...|        1| 25.13999993460519|47.377143314906526|
|{2026-04-05 20:50...|        7|27.485000133514404| 49.27750015258789|
|{2026-04-05 20:54...|        8|25.752000427246095| 52.13399963378906|
|{2026-04-05 20:51...|        1|  25.1233336130778| 56.85333251953125|
|{2026-04-05 20:44...|       10| 25.44999967302595| 58.24571337018694|
|{2026-04-05 20:49...|        7|25.492500066757202| 49.00125026702881|
|{2026-04-05 20:55...|       10|25.135999870300292|55.971000289916994|
|{2026-04-05 20:57...|       10|23.964285714285715| 49.75857162475586|
|{2026-04-05 20:57...|        9| 26.18500010172526| 50.66666634877523|
|{2026-04-05 20:54...|        2|25.121428898402623|53.489999771118164|
|{2026-04-05 20:44...|        4|22.956666310628254|  50.7933349609375|
|{2026-04-05 20:48...|        6| 25.18624997138977| 49.51875066757202|
|{2026-04-05 20:56...|       10|26.073333104451496|53.173333485921226|
|{2026-04-05 20:51...|        8| 24.41333262125651| 57.70666631062826|
|{2026-04-05 20:45...|        9|22.821249961853027| 43.34499979019165|
|{2026-04-05 20:51...|        7|22.191428593226842| 54.69142859322684|
|{2026-04-05 20:44...|        5|20.757500171661377|50.334999084472656|
|{2026-04-05 20:44...|        2|25.065714154924667| 53.86857114519392|
|{2026-04-05 20:49...|        8|23.043333371480305|  51.6216672261556|
+--------------------+---------+------------------+------------------+
only showing top 20 rows

-------------------------------------------
Batch: 86
-------------------------------------------
+--------------------+---------+------------------+------------------+
|              window|sensor_id|  avg(temperature)|     avg(humidity)|
+--------------------+---------+------------------+------------------+
|{2026-04-05 20:57...|        8| 25.15375018119812| 46.36749982833862|
|{2026-04-05 20:49...|        1| 25.13999993460519|47.377143314906526|
|{2026-04-05 20:50...|        7|27.485000133514404| 49.27750015258789|
|{2026-04-05 20:54...|        8|25.752000427246095| 52.13399963378906|
|{2026-04-05 20:51...|        1|  25.1233336130778| 56.85333251953125|
|{2026-04-05 20:44...|       10| 25.44999967302595| 58.24571337018694|
|{2026-04-05 20:49...|        7|25.492500066757202| 49.00125026702881|
|{2026-04-05 20:55...|       10|25.135999870300292|55.971000289916994|
|{2026-04-05 20:57...|       10| 24.53749990463257| 47.80875015258789|
|{2026-04-05 20:57...|        9| 26.18500010172526| 50.66666634877523|
|{2026-04-05 20:54...|        2|25.121428898402623|53.489999771118164|
|{2026-04-05 20:44...|        4|22.956666310628254|  50.7933349609375|
|{2026-04-05 20:48...|        6| 25.18624997138977| 49.51875066757202|
|{2026-04-05 20:56...|       10|26.073333104451496|53.173333485921226|
|{2026-04-05 20:51...|        8| 24.41333262125651| 57.70666631062826|
|{2026-04-05 20:45...|        9|22.821249961853027| 43.34499979019165|
|{2026-04-05 20:51...|        7|22.191428593226842| 54.69142859322684|
|{2026-04-05 20:44...|        5|20.757500171661377|50.334999084472656|
|{2026-04-05 20:44...|        2|25.065714154924667| 53.86857114519392|
|{2026-04-05 20:49...|        8|23.043333371480305|  51.6216672261556|
+--------------------+---------+------------------+------------------+
only showing top 20 rows

-------------------------------------------
Batch: 87
-------------------------------------------
+--------------------+---------+------------------+------------------+
|              window|sensor_id|  avg(temperature)|     avg(humidity)|
+--------------------+---------+------------------+------------------+
|{2026-04-05 20:57...|        8| 25.15375018119812| 46.36749982833862|
|{2026-04-05 20:49...|        1| 25.13999993460519|47.377143314906526|
|{2026-04-05 20:50...|        7|27.485000133514404| 49.27750015258789|
|{2026-04-05 20:54...|        8|25.752000427246095| 52.13399963378906|
|{2026-04-05 20:51...|        1|  25.1233336130778| 56.85333251953125|
|{2026-04-05 20:44...|       10| 25.44999967302595| 58.24571337018694|
|{2026-04-05 20:49...|        7|25.492500066757202| 49.00125026702881|
|{2026-04-05 20:55...|       10|25.135999870300292|55.971000289916994|
|{2026-04-05 20:57...|       10| 24.53749990463257| 47.80875015258789|
|{2026-04-05 20:57...|        9| 26.18500010172526| 50.66666634877523|
|{2026-04-05 20:54...|        2|25.121428898402623|53.489999771118164|
|{2026-04-05 20:44...|        4|22.956666310628254|  50.7933349609375|
|{2026-04-05 20:48...|        6| 25.18624997138977| 49.51875066757202|
|{2026-04-05 20:56...|       10|26.073333104451496|53.173333485921226|
|{2026-04-05 20:51...|        8| 24.41333262125651| 57.70666631062826|
|{2026-04-05 20:45...|        9|22.821249961853027| 43.34499979019165|
|{2026-04-05 20:51...|        7|22.191428593226842| 54.69142859322684|
|{2026-04-05 20:44...|        5|20.757500171661377|50.334999084472656|
|{2026-04-05 20:44...|        2|25.065714154924667| 53.86857114519392|
|{2026-04-05 20:49...|        8|23.043333371480305|  51.6216672261556|
+--------------------+---------+------------------+------------------+
only showing top 20 rows

-------------------------------------------
Batch: 88
-------------------------------------------
+--------------------+---------+------------------+------------------+
|              window|sensor_id|  avg(temperature)|     avg(humidity)|
+--------------------+---------+------------------+------------------+
|{2026-04-05 20:57...|        8| 25.15375018119812| 46.36749982833862|
|{2026-04-05 20:49...|        1| 25.13999993460519|47.377143314906526|
|{2026-04-05 20:58...|        5|24.209999084472656| 46.91999816894531|
|{2026-04-05 20:50...|        7|27.485000133514404| 49.27750015258789|
|{2026-04-05 20:54...|        8|25.752000427246095| 52.13399963378906|
|{2026-04-05 20:51...|        1|  25.1233336130778| 56.85333251953125|
|{2026-04-05 20:44...|       10| 25.44999967302595| 58.24571337018694|
|{2026-04-05 20:49...|        7|25.492500066757202| 49.00125026702881|
|{2026-04-05 20:55...|       10|25.135999870300292|55.971000289916994|
|{2026-04-05 20:57...|       10| 24.53749990463257| 47.80875015258789|
|{2026-04-05 20:57...|        9| 26.18500010172526| 50.66666634877523|
|{2026-04-05 20:54...|        2|25.121428898402623|53.489999771118164|
|{2026-04-05 20:44...|        4|22.956666310628254|  50.7933349609375|
|{2026-04-05 20:48...|        6| 25.18624997138977| 49.51875066757202|
|{2026-04-05 20:56...|       10|26.073333104451496|53.173333485921226|
|{2026-04-05 20:51...|        8| 24.41333262125651| 57.70666631062826|
|{2026-04-05 20:45...|        9|22.821249961853027| 43.34499979019165|
|{2026-04-05 20:51...|        7|22.191428593226842| 54.69142859322684|
|{2026-04-05 20:44...|        5|20.757500171661377|50.334999084472656|
|{2026-04-05 20:44...|        2|25.065714154924667| 53.86857114519392|
+--------------------+---------+------------------+------------------+
only showing top 20 rows

-------------------------------------------
Batch: 89
-------------------------------------------
+--------------------+---------+------------------+------------------+
|              window|sensor_id|  avg(temperature)|     avg(humidity)|
+--------------------+---------+------------------+------------------+
|{2026-04-05 20:57...|        8| 25.15375018119812| 46.36749982833862|
|{2026-04-05 20:49...|        1| 25.13999993460519|47.377143314906526|
|{2026-04-05 20:58...|        5|23.274999618530273|48.739999771118164|
|{2026-04-05 20:50...|        7|27.485000133514404| 49.27750015258789|
|{2026-04-05 20:54...|        8|25.752000427246095| 52.13399963378906|
|{2026-04-05 20:51...|        1|  25.1233336130778| 56.85333251953125|
|{2026-04-05 20:44...|       10| 25.44999967302595| 58.24571337018694|
|{2026-04-05 20:49...|        7|25.492500066757202| 49.00125026702881|
|{2026-04-05 20:55...|       10|25.135999870300292|55.971000289916994|
|{2026-04-05 20:57...|       10| 24.53749990463257| 47.80875015258789|
|{2026-04-05 20:57...|        9| 26.18500010172526| 50.66666634877523|
|{2026-04-05 20:54...|        2|25.121428898402623|53.489999771118164|
|{2026-04-05 20:44...|        4|22.956666310628254|  50.7933349609375|
|{2026-04-05 20:48...|        6| 25.18624997138977| 49.51875066757202|
|{2026-04-05 20:56...|       10|26.073333104451496|53.173333485921226|
|{2026-04-05 20:51...|        8| 24.41333262125651| 57.70666631062826|
|{2026-04-05 20:45...|        9|22.821249961853027| 43.34499979019165|
|{2026-04-05 20:51...|        7|22.191428593226842| 54.69142859322684|
|{2026-04-05 20:44...|        5|20.757500171661377|50.334999084472656|
|{2026-04-05 20:44...|        2|25.065714154924667| 53.86857114519392|
+--------------------+---------+------------------+------------------+
only showing top 20 rows

-------------------------------------------
Batch: 90
-------------------------------------------
+--------------------+---------+------------------+------------------+
|              window|sensor_id|  avg(temperature)|     avg(humidity)|
+--------------------+---------+------------------+------------------+
|{2026-04-05 20:57...|        8| 25.15375018119812| 46.36749982833862|
|{2026-04-05 20:49...|        1| 25.13999993460519|47.377143314906526|
|{2026-04-05 20:58...|        5|23.274999618530273|48.739999771118164|
|{2026-04-05 20:50...|        7|27.485000133514404| 49.27750015258789|
|{2026-04-05 20:54...|        8|25.752000427246095| 52.13399963378906|
|{2026-04-05 20:51...|        1|  25.1233336130778| 56.85333251953125|
|{2026-04-05 20:44...|       10| 25.44999967302595| 58.24571337018694|
|{2026-04-05 20:49...|        7|25.492500066757202| 49.00125026702881|
|{2026-04-05 20:55...|       10|25.135999870300292|55.971000289916994|
|{2026-04-05 20:57...|       10| 24.53749990463257| 47.80875015258789|
|{2026-04-05 20:57...|        9| 26.18500010172526| 50.66666634877523|
|{2026-04-05 20:54...|        2|25.121428898402623|53.489999771118164|
|{2026-04-05 20:44...|        4|22.956666310628254|  50.7933349609375|
|{2026-04-05 20:48...|        6| 25.18624997138977| 49.51875066757202|
|{2026-04-05 20:56...|       10|26.073333104451496|53.173333485921226|
|{2026-04-05 20:51...|        8| 24.41333262125651| 57.70666631062826|
|{2026-04-05 20:45...|        9|22.821249961853027| 43.34499979019165|
|{2026-04-05 20:51...|        7|22.191428593226842| 54.69142859322684|
|{2026-04-05 20:44...|        5|20.757500171661377|50.334999084472656|
|{2026-04-05 20:44...|        2|25.065714154924667| 53.86857114519392|
+--------------------+---------+------------------+------------------+
only showing top 20 rows

-------------------------------------------
Batch: 91
-------------------------------------------
+--------------------+---------+------------------+------------------+
|              window|sensor_id|  avg(temperature)|     avg(humidity)|
+--------------------+---------+------------------+------------------+
|{2026-04-05 20:57...|        8| 25.15375018119812| 46.36749982833862|
|{2026-04-05 20:49...|        1| 25.13999993460519|47.377143314906526|
|{2026-04-05 20:58...|        5|23.274999618530273|48.739999771118164|
|{2026-04-05 20:50...|        7|27.485000133514404| 49.27750015258789|
|{2026-04-05 20:54...|        8|25.752000427246095| 52.13399963378906|
|{2026-04-05 20:51...|        1|  25.1233336130778| 56.85333251953125|
|{2026-04-05 20:44...|       10| 25.44999967302595| 58.24571337018694|
|{2026-04-05 20:49...|        7|25.492500066757202| 49.00125026702881|
|{2026-04-05 20:55...|       10|25.135999870300292|55.971000289916994|
|{2026-04-05 20:57...|       10| 24.53749990463257| 47.80875015258789|
|{2026-04-05 20:57...|        9| 26.18500010172526| 50.66666634877523|
|{2026-04-05 20:54...|        2|25.121428898402623|53.489999771118164|
|{2026-04-05 20:44...|        4|22.956666310628254|  50.7933349609375|
|{2026-04-05 20:48...|        6| 25.18624997138977| 49.51875066757202|
|{2026-04-05 20:56...|       10|26.073333104451496|53.173333485921226|
|{2026-04-05 20:51...|        8| 24.41333262125651| 57.70666631062826|
|{2026-04-05 20:45...|        9|22.821249961853027| 43.34499979019165|
|{2026-04-05 20:51...|        7|22.191428593226842| 54.69142859322684|
|{2026-04-05 20:44...|        5|20.757500171661377|50.334999084472656|
|{2026-04-05 20:44...|        2|25.065714154924667| 53.86857114519392|
+--------------------+---------+------------------+------------------+
only showing top 20 rows

-------------------------------------------
Batch: 92
-------------------------------------------
+--------------------+---------+------------------+------------------+
|              window|sensor_id|  avg(temperature)|     avg(humidity)|
+--------------------+---------+------------------+------------------+
|{2026-04-05 20:57...|        8| 25.15375018119812| 46.36749982833862|
|{2026-04-05 20:49...|        1| 25.13999993460519|47.377143314906526|
|{2026-04-05 20:58...|        5|23.274999618530273|48.739999771118164|
|{2026-04-05 20:50...|        7|27.485000133514404| 49.27750015258789|
|{2026-04-05 20:54...|        8|25.752000427246095| 52.13399963378906|
|{2026-04-05 20:51...|        1|  25.1233336130778| 56.85333251953125|
|{2026-04-05 20:44...|       10| 25.44999967302595| 58.24571337018694|
|{2026-04-05 20:49...|        7|25.492500066757202| 49.00125026702881|
|{2026-04-05 20:55...|       10|25.135999870300292|55.971000289916994|
|{2026-04-05 20:57...|       10| 24.53749990463257| 47.80875015258789|
|{2026-04-05 20:57...|        9| 26.18500010172526| 50.66666634877523|
|{2026-04-05 20:54...|        2|25.121428898402623|53.489999771118164|
|{2026-04-05 20:44...|        4|22.956666310628254|  50.7933349609375|
|{2026-04-05 20:48...|        6| 25.18624997138977| 49.51875066757202|
|{2026-04-05 20:56...|       10|26.073333104451496|53.173333485921226|
|{2026-04-05 20:51...|        8| 24.41333262125651| 57.70666631062826|
|{2026-04-05 20:45...|        9|22.821249961853027| 43.34499979019165|
|{2026-04-05 20:51...|        7|22.191428593226842| 54.69142859322684|
|{2026-04-05 20:44...|        5|20.757500171661377|50.334999084472656|
|{2026-04-05 20:59...|        7|28.440000534057617| 33.52000045776367|
+--------------------+---------+------------------+------------------+
only showing top 20 rows

-------------------------------------------
Batch: 93
-------------------------------------------
+--------------------+---------+------------------+------------------+
|              window|sensor_id|  avg(temperature)|     avg(humidity)|
+--------------------+---------+------------------+------------------+
|{2026-04-05 20:57...|        8| 25.15375018119812| 46.36749982833862|
|{2026-04-05 20:49...|        1| 25.13999993460519|47.377143314906526|
|{2026-04-05 20:58...|        5|23.274999618530273|48.739999771118164|
|{2026-04-05 20:50...|        7|27.485000133514404| 49.27750015258789|
|{2026-04-05 20:54...|        8|25.752000427246095| 52.13399963378906|
|{2026-04-05 20:51...|        1|  25.1233336130778| 56.85333251953125|
|{2026-04-05 20:44...|       10| 25.44999967302595| 58.24571337018694|
|{2026-04-05 20:49...|        7|25.492500066757202| 49.00125026702881|
|{2026-04-05 20:55...|       10|25.135999870300292|55.971000289916994|
|{2026-04-05 20:57...|       10| 24.53749990463257| 47.80875015258789|
|{2026-04-05 20:57...|        9| 26.18500010172526| 50.66666634877523|
|{2026-04-05 20:54...|        2|25.121428898402623|53.489999771118164|
|{2026-04-05 20:44...|        4|22.956666310628254|  50.7933349609375|
|{2026-04-05 20:48...|        6| 25.18624997138977| 49.51875066757202|
|{2026-04-05 20:56...|       10|26.073333104451496|53.173333485921226|
|{2026-04-05 20:51...|        8| 24.41333262125651| 57.70666631062826|
|{2026-04-05 20:45...|        9|22.821249961853027| 43.34499979019165|
|{2026-04-05 20:51...|        7|22.191428593226842| 54.69142859322684|
|{2026-04-05 20:44...|        5|20.757500171661377|50.334999084472656|
|{2026-04-05 20:59...|        7|           27.1875|54.105000495910645|
+--------------------+---------+------------------+------------------+
only showing top 20 rows

-------------------------------------------
Batch: 94
-------------------------------------------
+--------------------+---------+------------------+------------------+
|              window|sensor_id|  avg(temperature)|     avg(humidity)|
+--------------------+---------+------------------+------------------+
|{2026-04-05 20:57...|        8| 25.15375018119812| 46.36749982833862|
|{2026-04-05 20:49...|        1| 25.13999993460519|47.377143314906526|
|{2026-04-05 20:58...|        5|23.274999618530273|48.739999771118164|
|{2026-04-05 20:50...|        7|27.485000133514404| 49.27750015258789|
|{2026-04-05 20:54...|        8|25.752000427246095| 52.13399963378906|
|{2026-04-05 20:51...|        1|  25.1233336130778| 56.85333251953125|
|{2026-04-05 20:44...|       10| 25.44999967302595| 58.24571337018694|
|{2026-04-05 20:49...|        7|25.492500066757202| 49.00125026702881|
|{2026-04-05 20:55...|       10|25.135999870300292|55.971000289916994|
|{2026-04-05 20:57...|       10| 24.53749990463257| 47.80875015258789|
|{2026-04-05 20:57...|        9| 26.18500010172526| 50.66666634877523|
|{2026-04-05 20:54...|        2|25.121428898402623|53.489999771118164|
|{2026-04-05 20:44...|        4|22.956666310628254|  50.7933349609375|
|{2026-04-05 20:48...|        6| 25.18624997138977| 49.51875066757202|
|{2026-04-05 20:56...|       10|26.073333104451496|53.173333485921226|
|{2026-04-05 20:51...|        8| 24.41333262125651| 57.70666631062826|
|{2026-04-05 20:45...|        9|22.821249961853027| 43.34499979019165|
|{2026-04-05 20:51...|        7|22.191428593226842| 54.69142859322684|
|{2026-04-05 20:59...|        8|24.559999465942383| 62.08000183105469|
|{2026-04-05 20:44...|        5|20.757500171661377|50.334999084472656|
+--------------------+---------+------------------+------------------+
only showing top 20 rows

-------------------------------------------
Batch: 95
-------------------------------------------
+--------------------+---------+------------------+------------------+
|              window|sensor_id|  avg(temperature)|     avg(humidity)|
+--------------------+---------+------------------+------------------+
|{2026-04-05 20:57...|        8| 25.15375018119812| 46.36749982833862|
|{2026-04-05 20:49...|        1| 25.13999993460519|47.377143314906526|
|{2026-04-05 20:58...|        5|23.274999618530273|48.739999771118164|
|{2026-04-05 20:50...|        7|27.485000133514404| 49.27750015258789|
|{2026-04-05 20:54...|        8|25.752000427246095| 52.13399963378906|
|{2026-04-05 20:51...|        1|  25.1233336130778| 56.85333251953125|
|{2026-04-05 20:44...|       10| 25.44999967302595| 58.24571337018694|
|{2026-04-05 20:49...|        7|25.492500066757202| 49.00125026702881|
|{2026-04-05 20:55...|       10|25.135999870300292|55.971000289916994|
|{2026-04-05 20:57...|       10| 24.53749990463257| 47.80875015258789|
|{2026-04-05 20:57...|        9| 26.18500010172526| 50.66666634877523|
|{2026-04-05 20:54...|        2|25.121428898402623|53.489999771118164|
|{2026-04-05 20:44...|        4|22.956666310628254|  50.7933349609375|
|{2026-04-05 20:48...|        6| 25.18624997138977| 49.51875066757202|
|{2026-04-05 20:56...|       10|26.073333104451496|53.173333485921226|
|{2026-04-05 20:51...|        8| 24.41333262125651| 57.70666631062826|
|{2026-04-05 20:45...|        9|22.821249961853027| 43.34499979019165|
|{2026-04-05 20:51...|        7|22.191428593226842| 54.69142859322684|
|{2026-04-05 20:59...|        8|24.523333231608074| 56.93000030517578|
|{2026-04-05 20:44...|        5|20.757500171661377|50.334999084472656|
+--------------------+---------+------------------+------------------+
only showing top 20 rows

-------------------------------------------
Batch: 96
-------------------------------------------
+--------------------+---------+------------------+------------------+
|              window|sensor_id|  avg(temperature)|     avg(humidity)|
+--------------------+---------+------------------+------------------+
|{2026-04-05 20:57...|        8| 25.15375018119812| 46.36749982833862|
|{2026-04-05 20:49...|        1| 25.13999993460519|47.377143314906526|
|{2026-04-05 20:58...|        5|23.274999618530273|48.739999771118164|
|{2026-04-05 20:50...|        7|27.485000133514404| 49.27750015258789|
|{2026-04-05 20:54...|        8|25.752000427246095| 52.13399963378906|
|{2026-04-05 20:51...|        1|  25.1233336130778| 56.85333251953125|
|{2026-04-05 20:44...|       10| 25.44999967302595| 58.24571337018694|
|{2026-04-05 20:49...|        7|25.492500066757202| 49.00125026702881|
|{2026-04-05 20:55...|       10|25.135999870300292|55.971000289916994|
|{2026-04-05 20:57...|       10| 24.53749990463257| 47.80875015258789|
|{2026-04-05 20:57...|        9| 26.18500010172526| 50.66666634877523|
|{2026-04-05 20:54...|        2|25.121428898402623|53.489999771118164|
|{2026-04-05 20:44...|        4|22.956666310628254|  50.7933349609375|
|{2026-04-05 20:48...|        6| 25.18624997138977| 49.51875066757202|
|{2026-04-05 20:56...|       10|26.073333104451496|53.173333485921226|
|{2026-04-05 20:51...|        8| 24.41333262125651| 57.70666631062826|
|{2026-04-05 20:45...|        9|22.821249961853027| 43.34499979019165|
|{2026-04-05 20:51...|        7|22.191428593226842| 54.69142859322684|
|{2026-04-05 20:59...|        8|25.572499752044678| 58.09250068664551|
|{2026-04-05 20:44...|        5|20.757500171661377|50.334999084472656|
+--------------------+---------+------------------+------------------+
only showing top 20 rows

-------------------------------------------
Batch: 97
-------------------------------------------
+--------------------+---------+------------------+------------------+
|              window|sensor_id|  avg(temperature)|     avg(humidity)|
+--------------------+---------+------------------+------------------+
|{2026-04-05 20:57...|        8| 25.15375018119812| 46.36749982833862|
|{2026-04-05 20:49...|        1| 25.13999993460519|47.377143314906526|
|{2026-04-05 20:58...|        5|23.274999618530273|48.739999771118164|
|{2026-04-05 20:50...|        7|27.485000133514404| 49.27750015258789|
|{2026-04-05 20:54...|        8|25.752000427246095| 52.13399963378906|
|{2026-04-05 20:51...|        1|  25.1233336130778| 56.85333251953125|
|{2026-04-05 20:44...|       10| 25.44999967302595| 58.24571337018694|
|{2026-04-05 20:49...|        7|25.492500066757202| 49.00125026702881|
|{2026-04-05 20:55...|       10|25.135999870300292|55.971000289916994|
|{2026-04-05 20:57...|       10| 24.53749990463257| 47.80875015258789|
|{2026-04-05 20:57...|        9| 26.18500010172526| 50.66666634877523|
|{2026-04-05 20:54...|        2|25.121428898402623|53.489999771118164|
|{2026-04-05 20:44...|        4|22.956666310628254|  50.7933349609375|
|{2026-04-05 20:48...|        6| 25.18624997138977| 49.51875066757202|
|{2026-04-05 20:56...|       10|26.073333104451496|53.173333485921226|
|{2026-04-05 20:51...|        8| 24.41333262125651| 57.70666631062826|
|{2026-04-05 20:45...|        9|22.821249961853027| 43.34499979019165|
|{2026-04-05 20:51...|        7|22.191428593226842| 54.69142859322684|
|{2026-04-05 20:59...|        8|26.445999908447266| 54.74000091552735|
|{2026-04-05 20:44...|        5|20.757500171661377|50.334999084472656|
+--------------------+---------+------------------+------------------+
only showing top 20 rows

-------------------------------------------
Batch: 98
-------------------------------------------
+--------------------+---------+------------------+------------------+
|              window|sensor_id|  avg(temperature)|     avg(humidity)|
+--------------------+---------+------------------+------------------+
|{2026-04-05 20:57...|        8| 25.15375018119812| 46.36749982833862|
|{2026-04-05 20:49...|        1| 25.13999993460519|47.377143314906526|
|{2026-04-05 21:00...|        7| 22.43000030517578|  33.0099983215332|
|{2026-04-05 20:58...|        5|23.274999618530273|48.739999771118164|
|{2026-04-05 20:50...|        7|27.485000133514404| 49.27750015258789|
|{2026-04-05 20:54...|        8|25.752000427246095| 52.13399963378906|
|{2026-04-05 20:51...|        1|  25.1233336130778| 56.85333251953125|
|{2026-04-05 20:44...|       10| 25.44999967302595| 58.24571337018694|
|{2026-04-05 20:49...|        7|25.492500066757202| 49.00125026702881|
|{2026-04-05 20:55...|       10|25.135999870300292|55.971000289916994|
|{2026-04-05 20:57...|       10| 24.53749990463257| 47.80875015258789|
|{2026-04-05 20:57...|        9| 26.18500010172526| 50.66666634877523|
|{2026-04-05 20:54...|        2|25.121428898402623|53.489999771118164|
|{2026-04-05 20:44...|        4|22.956666310628254|  50.7933349609375|
|{2026-04-05 20:48...|        6| 25.18624997138977| 49.51875066757202|
|{2026-04-05 20:56...|       10|26.073333104451496|53.173333485921226|
|{2026-04-05 20:51...|        8| 24.41333262125651| 57.70666631062826|
|{2026-04-05 20:45...|        9|22.821249961853027| 43.34499979019165|
|{2026-04-05 20:51...|        7|22.191428593226842| 54.69142859322684|
|{2026-04-05 20:59...|        8|26.445999908447266| 54.74000091552735|
+--------------------+---------+------------------+------------------+
only showing top 20 rows

-------------------------------------------
Batch: 99
-------------------------------------------
+--------------------+---------+------------------+------------------+
|              window|sensor_id|  avg(temperature)|     avg(humidity)|
+--------------------+---------+------------------+------------------+
|{2026-04-05 21:00...|        4|22.489999771118164| 54.97666676839193|
|{2026-04-05 20:57...|        8| 25.15375018119812| 46.36749982833862|
|{2026-04-05 21:00...|        8|23.010000228881836|  59.5099983215332|
|{2026-04-05 20:49...|        1| 25.13999993460519|47.377143314906526|
|{2026-04-05 21:00...|        7| 21.28499984741211| 35.03999900817871|
|{2026-04-05 20:58...|        5|23.274999618530273|48.739999771118164|
|{2026-04-05 20:50...|        7|27.485000133514404| 49.27750015258789|
|{2026-04-05 20:54...|        8|25.752000427246095| 52.13399963378906|
|{2026-04-05 20:51...|        1|  25.1233336130778| 56.85333251953125|
|{2026-04-05 20:44...|       10| 25.44999967302595| 58.24571337018694|
|{2026-04-05 20:49...|        7|25.492500066757202| 49.00125026702881|
|{2026-04-05 20:55...|       10|25.135999870300292|55.971000289916994|
|{2026-04-05 20:57...|       10| 24.53749990463257| 47.80875015258789|
|{2026-04-05 20:57...|        9| 26.18500010172526| 50.66666634877523|
|{2026-04-05 20:54...|        2|25.121428898402623|53.489999771118164|
|{2026-04-05 20:44...|        4|22.956666310628254|  50.7933349609375|
|{2026-04-05 20:48...|        6| 25.18624997138977| 49.51875066757202|
|{2026-04-05 20:56...|       10|26.073333104451496|53.173333485921226|
|{2026-04-05 20:51...|        8| 24.41333262125651| 57.70666631062826|
|{2026-04-05 20:45...|        9|22.821249961853027| 43.34499979019165|
+--------------------+---------+------------------+------------------+
only showing top 20 rows

-------------------------------------------
Batch: 100
-------------------------------------------
+--------------------+---------+------------------+------------------+
|              window|sensor_id|  avg(temperature)|     avg(humidity)|
+--------------------+---------+------------------+------------------+
|{2026-04-05 21:00...|        4|22.480000019073486| 57.40500068664551|
|{2026-04-05 20:57...|        8| 25.15375018119812| 46.36749982833862|
|{2026-04-05 21:00...|        8| 24.28333346048991|49.083333333333336|
|{2026-04-05 20:49...|        1| 25.13999993460519|47.377143314906526|
|{2026-04-05 21:00...|        7| 21.28499984741211| 35.03999900817871|
|{2026-04-05 20:58...|        5|23.274999618530273|48.739999771118164|
|{2026-04-05 20:50...|        7|27.485000133514404| 49.27750015258789|
|{2026-04-05 20:54...|        8|25.752000427246095| 52.13399963378906|
|{2026-04-05 20:51...|        1|  25.1233336130778| 56.85333251953125|
|{2026-04-05 20:44...|       10| 25.44999967302595| 58.24571337018694|
|{2026-04-05 20:49...|        7|25.492500066757202| 49.00125026702881|
|{2026-04-05 20:55...|       10|25.135999870300292|55.971000289916994|
|{2026-04-05 20:57...|       10| 24.53749990463257| 47.80875015258789|
|{2026-04-05 20:57...|        9| 26.18500010172526| 50.66666634877523|
|{2026-04-05 20:54...|        2|25.121428898402623|53.489999771118164|
|{2026-04-05 20:44...|        4|22.956666310628254|  50.7933349609375|
|{2026-04-05 20:48...|        6| 25.18624997138977| 49.51875066757202|
|{2026-04-05 20:56...|       10|26.073333104451496|53.173333485921226|
|{2026-04-05 20:51...|        8| 24.41333262125651| 57.70666631062826|
|{2026-04-05 20:45...|        9|22.821249961853027| 43.34499979019165|
+--------------------+---------+------------------+------------------+
only showing top 20 rows

-------------------------------------------
Batch: 101
-------------------------------------------
+--------------------+---------+------------------+------------------+
|              window|sensor_id|  avg(temperature)|     avg(humidity)|
+--------------------+---------+------------------+------------------+
|{2026-04-05 21:00...|        4|23.309999847412108| 54.63600082397461|
|{2026-04-05 20:57...|        8| 25.15375018119812| 46.36749982833862|
|{2026-04-05 21:00...|        8| 24.28333346048991|49.083333333333336|
|{2026-04-05 20:49...|        1| 25.13999993460519|47.377143314906526|
|{2026-04-05 21:00...|        7| 21.28499984741211| 35.03999900817871|
|{2026-04-05 20:58...|        5|23.274999618530273|48.739999771118164|
|{2026-04-05 20:50...|        7|27.485000133514404| 49.27750015258789|
|{2026-04-05 20:54...|        8|25.752000427246095| 52.13399963378906|
|{2026-04-05 20:51...|        1|  25.1233336130778| 56.85333251953125|
|{2026-04-05 20:44...|       10| 25.44999967302595| 58.24571337018694|
|{2026-04-05 20:49...|        7|25.492500066757202| 49.00125026702881|
|{2026-04-05 20:55...|       10|25.135999870300292|55.971000289916994|
|{2026-04-05 20:57...|       10| 24.53749990463257| 47.80875015258789|
|{2026-04-05 20:57...|        9| 26.18500010172526| 50.66666634877523|
|{2026-04-05 20:54...|        2|25.121428898402623|53.489999771118164|
|{2026-04-05 20:44...|        4|22.956666310628254|  50.7933349609375|
|{2026-04-05 20:48...|        6| 25.18624997138977| 49.51875066757202|
|{2026-04-05 20:56...|       10|26.073333104451496|53.173333485921226|
|{2026-04-05 20:51...|        8| 24.41333262125651| 57.70666631062826|
|{2026-04-05 20:45...|        9|22.821249961853027| 43.34499979019165|
+--------------------+---------+------------------+------------------+
only showing top 20 rows

-------------------------------------------
Batch: 102
-------------------------------------------
+--------------------+---------+------------------+------------------+
|              window|sensor_id|  avg(temperature)|     avg(humidity)|
+--------------------+---------+------------------+------------------+
|{2026-04-05 21:00...|        4|23.309999847412108| 54.63600082397461|
|{2026-04-05 20:57...|        8| 25.15375018119812| 46.36749982833862|
|{2026-04-05 21:00...|        8| 24.28333346048991|49.083333333333336|
|{2026-04-05 20:49...|        1| 25.13999993460519|47.377143314906526|
|{2026-04-05 21:00...|        7|23.577499866485596| 40.95249938964844|
|{2026-04-05 20:58...|        5|23.274999618530273|48.739999771118164|
|{2026-04-05 20:50...|        7|27.485000133514404| 49.27750015258789|
|{2026-04-05 20:54...|        8|25.752000427246095| 52.13399963378906|
|{2026-04-05 20:51...|        1|  25.1233336130778| 56.85333251953125|
|{2026-04-05 20:44...|       10| 25.44999967302595| 58.24571337018694|
|{2026-04-05 20:49...|        7|25.492500066757202| 49.00125026702881|
|{2026-04-05 20:55...|       10|25.135999870300292|55.971000289916994|
|{2026-04-05 20:57...|       10| 24.53749990463257| 47.80875015258789|
|{2026-04-05 20:57...|        9| 26.18500010172526| 50.66666634877523|
|{2026-04-05 20:54...|        2|25.121428898402623|53.489999771118164|
|{2026-04-05 20:44...|        4|22.956666310628254|  50.7933349609375|
|{2026-04-05 20:48...|        6| 25.18624997138977| 49.51875066757202|
|{2026-04-05 20:56...|       10|26.073333104451496|53.173333485921226|
|{2026-04-05 20:51...|        8| 24.41333262125651| 57.70666631062826|
|{2026-04-05 20:45...|        9|22.821249961853027| 43.34499979019165|
+--------------------+---------+------------------+------------------+
only showing top 20 rows

-------------------------------------------
Batch: 103
-------------------------------------------
+--------------------+---------+------------------+------------------+
|              window|sensor_id|  avg(temperature)|     avg(humidity)|
+--------------------+---------+------------------+------------------+
|{2026-04-05 21:00...|        4|23.754285539899552| 53.07571520124163|
|{2026-04-05 20:57...|        8| 25.15375018119812| 46.36749982833862|
|{2026-04-05 21:00...|        8|24.172000122070312|47.444000244140625|
|{2026-04-05 20:49...|        1| 25.13999993460519|47.377143314906526|
|{2026-04-05 21:00...|        7|24.268000030517577|42.587999725341795|
|{2026-04-05 20:58...|        5|23.274999618530273|48.739999771118164|
|{2026-04-05 20:50...|        7|27.485000133514404| 49.27750015258789|
|{2026-04-05 20:54...|        8|25.752000427246095| 52.13399963378906|
|{2026-04-05 20:51...|        1|  25.1233336130778| 56.85333251953125|
|{2026-04-05 20:44...|       10| 25.44999967302595| 58.24571337018694|
|{2026-04-05 20:49...|        7|25.492500066757202| 49.00125026702881|
|{2026-04-05 20:55...|       10|25.135999870300292|55.971000289916994|
|{2026-04-05 20:57...|       10| 24.53749990463257| 47.80875015258789|
|{2026-04-05 20:57...|        9| 26.18500010172526| 50.66666634877523|
|{2026-04-05 20:54...|        2|25.121428898402623|53.489999771118164|
|{2026-04-05 20:44...|        4|22.956666310628254|  50.7933349609375|
|{2026-04-05 20:48...|        6| 25.18624997138977| 49.51875066757202|
|{2026-04-05 20:56...|       10|26.073333104451496|53.173333485921226|
|{2026-04-05 20:51...|        8| 24.41333262125651| 57.70666631062826|
|{2026-04-05 20:45...|        9|22.821249961853027| 43.34499979019165|
+--------------------+---------+------------------+------------------+
only showing top 20 rows

-------------------------------------------
Batch: 104
-------------------------------------------
+--------------------+---------+------------------+------------------+
|              window|sensor_id|  avg(temperature)|     avg(humidity)|
+--------------------+---------+------------------+------------------+
|{2026-04-05 21:00...|        4|23.754285539899552| 53.07571520124163|
|{2026-04-05 20:57...|        8| 25.15375018119812| 46.36749982833862|
|{2026-04-05 21:00...|        8|24.172000122070312|47.444000244140625|
|{2026-04-05 20:49...|        1| 25.13999993460519|47.377143314906526|
|{2026-04-05 21:00...|        7|24.268000030517577|42.587999725341795|
|{2026-04-05 20:58...|        5|23.274999618530273|48.739999771118164|
|{2026-04-05 20:50...|        7|27.485000133514404| 49.27750015258789|
|{2026-04-05 20:54...|        8|25.752000427246095| 52.13399963378906|
|{2026-04-05 20:51...|        1|  25.1233336130778| 56.85333251953125|
|{2026-04-05 20:44...|       10| 25.44999967302595| 58.24571337018694|
|{2026-04-05 20:49...|        7|25.492500066757202| 49.00125026702881|
|{2026-04-05 20:55...|       10|25.135999870300292|55.971000289916994|
|{2026-04-05 20:57...|       10| 24.53749990463257| 47.80875015258789|
|{2026-04-05 20:57...|        9| 26.18500010172526| 50.66666634877523|
|{2026-04-05 20:54...|        2|25.121428898402623|53.489999771118164|
|{2026-04-05 20:44...|        4|22.956666310628254|  50.7933349609375|
|{2026-04-05 20:48...|        6| 25.18624997138977| 49.51875066757202|
|{2026-04-05 20:56...|       10|26.073333104451496|53.173333485921226|
|{2026-04-05 20:51...|        8| 24.41333262125651| 57.70666631062826|
|{2026-04-05 20:45...|        9|22.821249961853027| 43.34499979019165|
+--------------------+---------+------------------+------------------+
only showing top 20 rows

-------------------------------------------
Batch: 105
-------------------------------------------
+--------------------+---------+------------------+------------------+
|              window|sensor_id|  avg(temperature)|     avg(humidity)|
+--------------------+---------+------------------+------------------+
|{2026-04-05 21:00...|        4|23.754285539899552| 53.07571520124163|
|{2026-04-05 20:57...|        8| 25.15375018119812| 46.36749982833862|
|{2026-04-05 21:00...|        8|24.172000122070312|47.444000244140625|
|{2026-04-05 20:49...|        1| 25.13999993460519|47.377143314906526|
|{2026-04-05 21:00...|        7|24.268000030517577|42.587999725341795|
|{2026-04-05 20:58...|        5|23.274999618530273|48.739999771118164|
|{2026-04-05 20:50...|        7|27.485000133514404| 49.27750015258789|
|{2026-04-05 20:54...|        8|25.752000427246095| 52.13399963378906|
|{2026-04-05 20:51...|        1|  25.1233336130778| 56.85333251953125|
|{2026-04-05 20:44...|       10| 25.44999967302595| 58.24571337018694|
|{2026-04-05 20:49...|        7|25.492500066757202| 49.00125026702881|
|{2026-04-05 20:55...|       10|25.135999870300292|55.971000289916994|
|{2026-04-05 20:57...|       10| 24.53749990463257| 47.80875015258789|
|{2026-04-05 20:57...|        9| 26.18500010172526| 50.66666634877523|
|{2026-04-05 20:54...|        2|25.121428898402623|53.489999771118164|
|{2026-04-05 20:44...|        4|22.956666310628254|  50.7933349609375|
|{2026-04-05 20:48...|        6| 25.18624997138977| 49.51875066757202|
|{2026-04-05 20:56...|       10|26.073333104451496|53.173333485921226|
|{2026-04-05 20:51...|        8| 24.41333262125651| 57.70666631062826|
|{2026-04-05 20:45...|        9|22.821249961853027| 43.34499979019165|
+--------------------+---------+------------------+------------------+
only showing top 20 rows

-------------------------------------------
Batch: 106
-------------------------------------------
+--------------------+---------+------------------+------------------+
|              window|sensor_id|  avg(temperature)|     avg(humidity)|
+--------------------+---------+------------------+------------------+
|{2026-04-05 21:00...|        4|23.754285539899552| 53.07571520124163|
|{2026-04-05 20:57...|        8| 25.15375018119812| 46.36749982833862|
|{2026-04-05 21:00...|        8|24.172000122070312|47.444000244140625|
|{2026-04-05 20:49...|        1| 25.13999993460519|47.377143314906526|
|{2026-04-05 21:00...|        7|24.268000030517577|42.587999725341795|
|{2026-04-05 20:58...|        5|23.274999618530273|48.739999771118164|
|{2026-04-05 20:50...|        7|27.485000133514404| 49.27750015258789|
|{2026-04-05 20:54...|        8|25.752000427246095| 52.13399963378906|
|{2026-04-05 20:51...|        1|  25.1233336130778| 56.85333251953125|
|{2026-04-05 20:44...|       10| 25.44999967302595| 58.24571337018694|
|{2026-04-05 20:49...|        7|25.492500066757202| 49.00125026702881|
|{2026-04-05 20:55...|       10|25.135999870300292|55.971000289916994|
|{2026-04-05 20:57...|       10| 24.53749990463257| 47.80875015258789|
|{2026-04-05 20:57...|        9| 26.18500010172526| 50.66666634877523|
|{2026-04-05 20:54...|        2|25.121428898402623|53.489999771118164|
|{2026-04-05 20:44...|        4|22.956666310628254|  50.7933349609375|
|{2026-04-05 20:48...|        6| 25.18624997138977| 49.51875066757202|
|{2026-04-05 20:56...|       10|26.073333104451496|53.173333485921226|
|{2026-04-05 20:51...|        8| 24.41333262125651| 57.70666631062826|
|{2026-04-05 20:45...|        9|22.821249961853027| 43.34499979019165|
+--------------------+---------+------------------+------------------+
only showing top 20 rows




