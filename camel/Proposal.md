# GSoC project proposal for Apache Camel.
# About me¶
 - University of Freiburg. MS Computer Science. 2018 - now 
 - Worked as a developer in industry. 3-4 years of experience in Java and 3-4 years more in Scala. Basic Python, Javascript, web-development. 
 - Contributed and continue to several opensource projects: akka (latest big PR: https://github.com/akka/akka/pull/26825), akka-http; small contributions to Apache JMeter, neosemantics, java-stix, swagger-akka-http. 
 - Oracle Certified Professional (Java 8)

My linkedin: https://www.linkedin.com/in/kirill-yankov-8b0747118/

My github: https://github.com/manonthegithub

# Background¶
Project assumes implementing several camel components:
- "Create a component for Kafka-Stream"(https://issues.apache.org/jira/browse/CAMEL-10652)
- "Create a camel component for etcd v3"(https://issues.apache.org/jira/browse/CAMEL-10173)
# Design / description of work¶
Highlevel design.

Kafka-stream component:
- Component implementation
- Endpoint implementation
- Consumer implementation
- Producer implementaion
- Configuration

Etcd v3 component:
- Component implementation
- Endpoint implementation
- Consumer implementation
- Producer implementaion
- Configuration

All goes with tests, docs, OSGi implementations.

# Results for the Apache community¶
 - Kafka-stream component available for use
 - Etcd v3 component available for use
 - camel-spring-boot starters [optional]
# Deliverables¶
 - Kafka-stream component (Component, Endpoint, Consumer and Producer), tests, documentation (including examples), OSGi support
 - Etcd v3 component (Component, Endpoint, Consumer and Producer), tests, documentation (including examples), OSGi support
 - camel-spring-boot starters [optional]
# Scheduling¶
Highlevel list of tasks in order.

Fistly work on Kafka.
Kafka-stream component:
- investigate on Kafka-streams more and define actual scope of the component, as well limitations of component comparing to the use of streams api (~ 2 days to 1 week)
- investigate more on the details of component, endpoint, consumer and producer implementations (~ 2-3 days)
- implementation of Producer + tests (~ 1-2 weeks)
- implementation of Consumer + tests (~ 1-2 weeks)
- implementation of Endpoint + tests (~ 2-3 days)
- implementation of Component + tests (~ 2-3 days)

Here probably a checkpoint with the decision on the priority of OSGi compared to Etcd v3 component.

- investigation on OSGi (few days) [optional]
- OSGi support implementation + tests (1-2 weeks - have no idea right now how it works, so it is very rough, may be underestimation as well as overestimation) [optional]
- documentation (~ 1 week)
- some spare days (~ 1-2 weeks) for bugfixing, some unexpected issues

Milestone 1.

In case enough time left.
Etcd v3 component:
- get acquainted with etcd and investigate on the scope and the limitations of the component (~ 1 week)
- investigate on what can be reused from etcd component (https://github.com/apache/camel/tree/master/components/camel-etcd) (~ 1-3 days)
- implementation of Producer + tests (~ 1-2 weeks)
- implementation of Consumer + tests (~ 1-2 weeks)
- implementation of Endpoint and Component + tests (~ 2-3 days)
- OSGi support + tests (~ 1 week) [optional]
- documentation (~ 1 week)

Milestone 2.

Here if time left (not sure on the priority, where to put this feature):
 - camel-spring-boot starters (https://github.com/apache/camel-spring-boot) for both components (~ 1-2 weeks)[optional]

In the worst case only one component will be done, in the best both will be done. In the average scenario, a part of the etcd component will be done, which can be finished outside of the GSoC project.

# Other commitments¶
In the beginning of the GSoC (first 2 weeks) I will be finishing an internship in NII (Japan) and will be less active, full dedication afterwards.
# Community engagement¶
Subscribed to dev mailing list. Keep communication in the project Jira. Forked github repo, looking at some sample implementations of the components.

<!--In particular with Apache $Project, including project mailing lists, wikis, issue trackers, test systems.
This should show a rough understanding of working with open source communities. You should be engaged with the rest of the community both before coding start (e.g. to develop this proposal) and during the project.
Include any planned user testing, prototypes, code review.-->
