# phd-datasets

Connectivity datasets used in my PhD and publicly available

Folder *grenoble* has datasets from IoT-Lab Grenoble, *lille* has datasets from IoT-Lab Lille, *soda* has datasets from UC Berkeley's Soda Hall, *strasbourg* has datasets from IoT-Lab Stransbourg, and *tutornet* has datasets from USC's Tutornet

Each file has the network connectivity measured over all 16 channels of IEEE 802.15.4 standard, considering all links between all nodes in the testbed.

In each file there are lines that can be of the types below:

* *t=\<timestamp\>*

    *\<timestamp\>* is the time that the experiment started

* *n=\<number\>*
    
    *\<number\>* is the number of nodes in the network

* *q\<id\>=\<n\>*

    *\<id\>* is the id of the node, starting at 0

    *\<n\>* is the number of packets in the queue at the beginning of each slotframe in IEEE 802.15.4. This parameter is only useful if we are simulating traffic in IEEE 802.15.4 schedules

* *a\<id\>=\<addr\>*

    *\<id\>* is the id of the node, starting at 0
    
    *\<addr\>* is the 64-bit address of the node

* *l\<id\>,\<chan\>=\<pdr_0\>,\<pdr_1\>,\<pdr_2\>,...,\<pdr_n-1\>*

    *\<id\>* is the id of the source node, starting at 0

    *\<chan\>* is the channel (0 to 15)

    *\<pdr_n\>* is the PDR to destination node n

    e.g.: *l1,2=98,0,100,82* - this line means that links with source node 1 at channel 2 are: PDR(1->0) = 98%, PDR(1>1) = 0%, PDR(1->2) = 100% and PDR(1->3) = 82%

    The PDR values are for unidirectional links.

    By default PDR(n,n) = 0 in all cases.

Please cite the paper below if you use these datasets.

```
@inproceedings{gomes2016insights,
  title={Insights into frequency diversity from measurements on an indoor low power wireless network testbed},
  author={Gomes, Pedro Henrique and Chen, Ying and Watteyne, Thomas and Krishnamachari, Bhaskar},
  booktitle={2016 IEEE Globecom Workshops (GC Wkshps)},
  pages={1--6},
  year={2016},
  organization={IEEE}
}
```
