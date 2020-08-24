# DBpedia databus integration with IPFS project

databus-maven-plugin is a tool for publishing metainformation on the datasets for making them accessible for search by global community. The goal of this project was to investigate on possible ways of integration of the plugin and [IPFS](https://ipfs.io), and to implement a working solution.

What was done? IPFS and its APIs were explored, and the architecture of the solution was designed. The plugin's codebase was refactored to allow better integration of IPFS and easier test development. The use of IPFS was added as one of possible configurable ways of storing datasets. Unit and integration testing utils were developed as well as unit and integration tests themselves. Documentation of the plugin was significantly refactored and a description of new features was added.

The integration of the plugin with IPFS allows the user to store the dataset files in IPFS, which enables possibility of distributing of the dataset globally, makes access to it more fault-tolerant, as well as to save disk space by deduplication of the parts of the datasets which remain the same from version to version.


The details on the project proposal please find [here](Proposal.md).

You can find more details on the progress of the project [here](Project_progress_report.md).

Please find a link to the PR with all the code done [here](https://github.com/dbpedia/databus-maven-plugin/pull/130).
