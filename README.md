# Arweave Decentralized Web Nodes

 Decentralized Backend functionality for DWA's using mesh network methodology.

 ## What is an ADWN?

 An Arweave Decentralized Web Node is a service worker that is installed by a Decentralized Web App when a client is accessing the app. Inside the service worker  
 is a program that connects to other running ADWN's for that app by referencing a smartweave Warp contract for the index of indexer nodes who pass on a list of client nodes.

 ### What program does a ADWN node run?

 The ADWN at its core runs a mesh network program that connects to all the other nodes for the specific DWA. When a DWA is created, they deploy the indexer contract for their app, which is formatted to maintain a list of indexer nodes. The indexer contract can of course be used for other indexing purposes, such as asset and user indexing for the DWA. Above the core functionality, the ADWN can run Node.js programs, for example a messaging app, grub app, etc.

 ### What is a Client Node?

 A client node is a singular instance of an ADWN. It can be either a master or slave node and that is determined on merit of its speed and reliability. Client nodes are also assigned to be Cluster Indexers as needed.

 ### What is a Indexer Node?

 A indexer node is a node run specifically for the purpose of maintaining a list of familial clusters. Anyone can register as an indexer by going to the ADWN settings of the app and applying to become a indexer, or, by interacting with the smart contract directly. The contract's creators can restrict who can become an indexer thru creating roles in the indexer contract.

## What is a Cluster?

 A cluster is a group of nodes created for the means of load balancing the mesh network. Its important for mesh networks to have a hierarchy of nodes, otherwise the routing of messages can become slow. Each cluster has master node which talk directly to other master nodes in the apps network. Master nodes are client nodes that are assigned factoring speed and reliability. A master node may be reassigned to another IP if that IP shows to be faster or more reliable. This ensures scalablity of the mesh network.

 ### What is a Familial Cluster?

 A familial cluster is a cluster of parent clusters master nodes. The master node of a familial cluster maintains a list of parent clusters who in turn maintain a list of child clusters who in turn maintain a list of client nodes. Whenever the work of maintaining the list of clusters reaches the limits of its reasonable capability, the network balances by creating a new cluster layer. Since the work of maintaining a simple list of connection addresses is quite low, this should not need to scale to many layers deep.

 
 
