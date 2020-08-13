# Initiation, community bonding period
We had two meetings with Sebastian and Aman. I've got better understanding of how databus works, and what should be done. 
We have also discussed organisational issues. I've been granted rights to the databus-maven-plugin repo, 
and given access to development server. Plan for this week is also to publish sample graph with the plugin.
# Week 1 (June 1 - June 7)
This week is not very productive as expected. I have finished work in Japan and had a flight on 2nd of June back to Germany. On 3rd I was setting everything up, this is going to continue for a few days more, but I will also work on the project (just not fulltime). Started reading the code of the databus-maven-plugin. Successfully built it. Read docs on how to develop maven plugins. Got better understanding of how it works. In general, looks very simple. Trying to publish my first dataset with the plugin. 
# Week 2 (June 8 - June 14)
- got better acquainted with the code of databus maven plugin and its configuration
- created a sample test project (https://github.com/manonthegithub/publishdata) to try uploading in the databus (using databus maven plugin), and uploaded test dataset
- read ipfs documentation
- investigated ipfs api and ways of integration
- installed ipfs node on my local pc, and on test server
- tested ipfs (saving small files works well, global CIDs work)
- tried http-api
- looked at the existing scala-client, looks like its not supported any more
- wrote sample implementation of uploading of small files

# Week 3 (June 15 - June 21)
- got better understanding of how ipfs works (watched a few tutorials, asked questions on their forum and in github, read more docs)
- implemented a few more scala-client methods
- started implementation of directories uploading
- developed a few ideas of how to track user downloads (make dbpeadia's ipfs gateway, possibly encrypt the data on the user upload)
- got better understanding on how to deal with versioning (use ipld, smart chunkers)
- made an architecture draft

![architecture draft](Architecture%20draft.svg)

# Week 4 (June 22 - June 28)
- got in touch with ipfs community, who gave some useful tips
- http-api imposes unnecessary overhead, so I switched to cli 
- implemented foundation for a cli client for databus-maven-plugin
- investigated more on the deduplication and chunking in ipfs, used datasets to find out how well is deduplication going to work with them. The result is that, it may work in case we use raw `.ttl` files, but it is not really efficient with compressed data. Compression looks much more efficient than the use of raw `.ttl` with deduplication, it may be not the case only if there are not many changes in the data, and new versions are published frequently. 

# Week 5 (June 29 - July 5)

Was working on integration of ipfs with databus-maven-plugin:
- reading code of the plugin and getting to know the structure in detail
- code refactorings for smoother integration of ipfs
- exploring approaches to testing of maven plugins (unit-tests, integration tests)
- made a sample unit test and sample integration test
- made a draft integration of IpfsCliClient with the plugin code (changes in dataid ttl are left to do, better testing is left)
- added dynamic generation of plugin version which can be used in code

# Week 6 (July 6 - July 12)

- encountered issues with testing the plugin, the solution needs to be discussed with Sebastian. Existing unittest utils do not allow to inject default values for standard maven properties, and to do real testing we need either require docker or ipfs installed on the build machine. How to deal with it is to be decided. 
- made some slight improvements in the IpfsPluginOps
- spent time trying to figure out why databus plugin is not working on the provided server. Connection to my webid address was not working on the server. The issue magically disappeared today.
- some parts of the plugin can be removed or replaced by invocation of the existing plugins, to be discussed with Sebastian
- cleaned up dependencies in the pom file, possibly more cleaning is needed. removing unneded deps allowed to run tests using maven-testing-harness without workarounds.
- did more investigation on file deduplication, and got promising results. previous conclusions that deduplication doesnt work for archives looks to be wrong, need to do more experiments to make final conclusion
- have deduced and calculated the formula for the optimal block size to achieve minimal size on deduplication (not putting all the details here): sqrt (hash_size * changes_every_n_bytes), where hash_size is the the length of the hash of a block in bytes (256 for sha256), changes_every_n_bytes is an average distance in bytes between changes in a file. 

# Week 7 (July 13 - July 19)

This week was mostly coding and diving deeper into maven plugin testing. I am really disappointed by the tools maven provides for tests.

- finally figured out the way of doing proper unit-testing for our plugin. The main problem was that maven plugin testing tools are very limited and do not inject maven properties.
- had to do lots of refactorings for testing to work
- wrote util functions and classes to ease the testing and initialisation of the tests
- finally started to write unittests

# Week 8 (July 20 - July 26)

It is taking a while to write the tests. I think I'll manage to finish it by the end of the week, at least some basic ones.

- the use of dummy implementations doesnt allow to simply check how the object was used, so I decided to switch on mocks
- configured mockito and explored its api
- rewrote a part of the tests for using mocks instead of dummy implementations
- as the plugin does a post request to the endpoint on deploy, configured mock web-server for unitests, appears to be very convenient thing for testing
- finished some basic unittests
- started with the integration tests
- configured test-containers (framework for running docker containers in integration tests) for running ipfs

# Week 9 (July 27 - August 2)

- wrote documentation
- did more investigation on the ways to increase deduplication of compresssed files with ipfs.
- did some slight code imporvements for configuring the ipfs in the plugin 
- more tests

# Week 10 (August 3 - August 9)

This week I have met the team of DbPedia in Leipzig.

- it took some time to fix the integration tests, I had to discover of how to configure the buid and the plugins properly, so that interation tests are preconfigured and run at the right moment
- trip to Leipzig
- meeting the team, discussions on what may be done next

# Week 11 (August 10 - August 16)

This week is a start of a final phase of the project.

- created a PR for the final submission
- created a draft documentation file for a final submission
- started writing and organising documentation
- investigated more on how to configure the ipfs client to connect to a remote node (got a hint from the community on how to do it)
- implemented configuration of the ipfs cli client to connect to a remote node (in the plugin), fixed the tests connected with it
- removed packageDirectory configuration property (for now it defaults to target)

# Week 12 (August 17 - August 23)

#todo


