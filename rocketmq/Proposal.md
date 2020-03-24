# GSoC project proposal for Apache RocketMQ.
# About me¶
 - University of Freiburg. MS Computer Science. 2018 - now 
 - Worked as a developer in industry. 3-4 years of experience in Java and 3-4 years more in Scala. Basic Python, Javascript, web-development. 
 - Contributed and continue to several opensource projects: akka (latest big PR: https://github.com/akka/akka/pull/26825), akka-http; small contributions to Apache JMeter, neosemantics, java-stix, swagger-akka-http. 
 - Oracle Certified Professional (Java 8)
 
My linkedin: https://www.linkedin.com/in/kirill-yankov-8b0747118/  
My github: https://github.com/manonthegithub
# Background¶
Project assumes implementing several roqcketmq components:
- "RocketMQ Connect Elasticsearch"(https://issues.apache.org/jira/browse/COMDEV-349)
- "RocketMQ Connect Cassandra"(https://issues.apache.org/jira/browse/COMDEV-353)
# Design / description of work¶
Two components:
 - Elasticsearch connector. Following should be implemented:
   - Configuration
   - SinkConnector
   - Tests
   - Docs
 - Cassandra connector. Following should be implemented:
   - Configuration
   - SinkConnector
   - Tests
   - Docs

# Results for the Apache community¶
- Elacticsearch connector available for use
- Cassandra sink connector availabele for use
# Deliverables¶
- Elasticsearch connector, docs, tests
- Cassandra connector, docs, tests
# Scheduling¶
Implementation of the connectors doesn't seem that difficult, but I can underestimate effort. In the worst case only one connector will be done. In the best case both. In the averge, elastic connector can be finished outside of GSoC.

Following tasks in order:  

Cassandra connector:  
- investigate more on how to implement connectors (up to 1 week)
- investigate more on Cassandra (up to 1 week)
- implementation of the SinkConnector class (1-2 weeks)
- tests (1 week)
- docs (1 week)
- spare time for fixes and unexpected works (2 weeks)

Milestone 1.

Elasticsearch connector:
- investigate more on Elastic (up to 1 week)
- implementation of the SinkConnector class (1-2 weeks)
- tests (1 week)
- docs (1 week)

Milestone 2.

# Other commitments¶
Initially the coding was expected to start on 18th of May, but as the timeline has changed, I have no overlapping activities anymore. I will be able to start working on the first few days with full dedication. At the beginning I was expecting that, when GSoC starts, I will be finishing my internship in Japan which is until the end of May.

# Community engagement¶
Subscribed to dev mailing list. Keep communication in the project Jira. Looking at some sample implementations of the connectors (https://github.com/apache/rocketmq-externals).

<!--In particular with Apache $Project, including project mailing lists, wikis, issue trackers, test systems.
This should show a rough understanding of working with open source communities. You should be engaged with the rest of the community both before coding start (e.g. to develop this proposal) and during the project.
Include any planned user testing, prototypes, code review.-->
