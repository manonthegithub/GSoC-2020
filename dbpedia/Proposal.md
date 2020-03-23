# Combine DBpedia/Databus with IPFS - Kirill Yankov


# Contact information

Name: Kirill Yankov  
Email Address: myworkpostbox [at] gmail.com  
My linkedin: https://www.linkedin.com/in/kirill-yankov-8b0747118/  
My github: https://github.com/manonthegithub  
  
# Project
"Combine DBpedia/Databus with IPFS" (https://forum.dbpedia.org/t/combine-dbpedia-databus-with-underlay/434)

Project Description:
Integration of Databus with IPFS.

If you would be willing and able to work on another of our suggested project ideas instead, which ones?  
Maybe, but did not look into it.

Please describe why you are interested in this specific project:  
The project has major challenges of making a good design, it is always interesting. Get experience working with a distributed file storage (IPFS) is also very interesting. Scala is a big plus too.  

## Please describe a tentative project architecture or an approach to it:
Two main components:
 - databus-maven-plugin - for publishing the data by customers
 - databus-client - loads published data, SPARQL endpoint  

This needs more investigation on IPFS, but in general the proejct looks like implementation of publishing to and reading from IPFS via current databus components (databus-client, databus-maven-plugin). 

Main problems for uploading:
 - new mechanism of uploading most likely to be implemented
 - versioning of the artifacts should be implemented
 
 Main problems for downloading:
 - in case downloading mechanism needs to changed (for example if IPFS client library needs to be used), potentially new gateway service needs to be implemented

 
Please detail an expected project plan and timeline with milestones:  
Tasks in order:  

- look in more details in the project code (both plugin and client), get better understanding how it works (1-2 weeks)
- investigate on IPFS (1-2 weeks)
- make initial design of integration with IPFS (2-3 days) (both uploading and downloading)
- make an initial prototype of the solution (1-2 weeks)
At that point re-estimation of implementation task size may be done.

Milestone 1.
- refine the solution requirements/architecture on the basis of collected from a prototype issues, drawbacks, comments (2 days - 1 week)
- implementation of the refined solution, with unit tests (1-4 weeks, difficult to assess, here is the main risk of underestimation)

Milestone 2.
- testing on some real data + integration (1-2 weeks)
- documentation (1 week)
- spare time for bugfixes and unexpected obstacles (2 weeks)
- performance testing (1 week - 4 weeks)[optional] (In case we are doing gateway, performance can become an issue, it may be not enough time for improving, but possibly I can do it outside of the scope of the project. Peformance testing assumes modeling real word scenarios and emulation of them with performance testing tools. The main criteria is whether or not the solution can handle expected load (requests/files/bytes per second). I have experience in that, but it may be very time consuming.)

Final Milestone.

In the best case fully functional integration is implemented. In the worst case, there will be at least a working prototype.
<!--Please include in your plan how will you evaluate the performance of your contribution (in terms of time, or accuracy, or both), as well as which data sets you will use for that evaluation.-->
# Technical skills

Worked as a developer in industry. 3-4 years of experience in Java and 3-4 years more in Scala. Worked as a performance testing engineer. Basic Python, web-development (js, webpack, react).  
Oracle Certified Professional (Java 8).  
See example of code in "Open source" section.

# Open Source

My PRs: https://github.com/pulls?q=is%3Apr+author%3Amanonthegithub+archived%3Afalse+

Contributed and continue to several opensource projects: akka (latest big PR: https://github.com/akka/akka/pull/26825 - persistence testkit implementation), akka-http; small contributions to Apache JMeter, neosemantics (exporting rdf - to neo4j), java-stix, swagger-akka-http.  
Why opensource? Firstly, opensource  helps you to grow as a professional, you can learn best practices and get inspiration for your projects from opensource. Secondly, sometimes I contribute to projects I use in my work, when its needed. Thirdly, its fun.

# Background & education

University of Freiburg. MS Computer Science. 2018 - now

# Research

Didn't do much of research. Had small project on investigating Neo4j performance on full Wikidata database imported in it (no publication). Cannot name any interesting paper.  
I would be interested in co-authoring a paper, if any.

# Summer plans

I will be in Russia and Germany. First two weeks of the project will not be very active, because I will be finishing my internship in NII (Japan). After the intenship - full dedication (30-40 hours per week).

# GSoC Experience

Did not participate in GSoC before.  
Have you applied or do you plan to apply for any other 2017 Summer of Code projects? Thinking about it.  
Why GSoC? Great opportunity to learn more, get new aquaintances with great programmers, potentially find a job, contribute to opensource and to earn some money.  
Why DBpedia? Two reasons: 
 - Interesting challenges (design of a working solution, integration with a distributed datastore)
 - I worked a little with rdf/ttl before, and it may be useful here
 - I love Scala, and its only project which is in Scala
 
# And finally...

Why me?
 - I think I can do a good job.
 - I love Scala.
