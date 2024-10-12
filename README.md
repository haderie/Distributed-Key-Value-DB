All project code is written in Python.

To implement the key-value datastore, we first implemented an election system so that there would be 1 leader and the rest of the replicas would be followers. We handled broadcasting heartbeats so that the followers know that the leader is still "active". We also implemented a database hashmap in order to keep track of all kev-value messages and be able to use them to distribute the log entries to all other replicas. In order to add the key-value messages to our hashmap, we create functions in order to respond to the client's "put" and "get" messages correctly. 

One challenge we faced was implementing the log and append entries functionalities. We struggled with how to approach implementing these. To help us start, we attended office hours and received guidance from a TA. Following this, we used the config files to test our implementations until they ran properly. 

One property/feature of our program we believe is good is that we separated the various program specifications provided by the assignment description into various functions. This made it much easier to debug the code since pinpointing where any issues we encountered was made much easier through this. If a test from a config file was not passing, we would review the corresponding function which carried out this task.   

To test our code, we used print statements–which have since been deleted for submission purposes. Such print statements implemented were used to review messages being sent and received. Primarily, however, we ran the tests within the config files to ensure our program's correctness. When the simulation was completed for a given test with no errors detected, we knew that the corresponding portion of our code was correct.
