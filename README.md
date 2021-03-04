#Dyncast (Dynamic Anycast) Virtual Side meeting in IETF 109

## Time: Wed (March 10) , 90min
   - UTC 10:00 - 11:30
   - CET (UTC+1) 11:00 - 12:30 - France/Germany/Prague
   - CST (UTC+8) 18:00 - 19:30 – Beijing/Singapore
   - EST (UTC-5) 05:00-06:30
   - PST (UTC-8) 02:00-03:30

Information also available on side meeting wiki: https://trac.ietf.org/trac/ietf/meeting/wiki/110sidemeetings

## Webex
- Webex Meeting number (access code): 
- Password:
- Password if joining from a phone: 
- Webex: https://htf-paris.my.webex.com/htf-paris.my/j.php?MTID=m719b852a7d548c66eab00360562f645a

## Etherpad for minute takers
https://etherpad.wikimedia.org/p/dyncast-ietf110

## Drafts:
- https://tools.ietf.org/html/draft-liu-dyncast-ps-usecases-01
- https://tools.ietf.org/html/draft-liu-dyncast-reqs-00
- https://tools.ietf.org/html/draft-li-dyncast-architecture-00
- https://tools.ietf.org/html/draft-bormann-dyncast-affinity-00

## Purpose of the virtual side meeting:
- Give an update on the use cases, problem space, requirements and architecture since last meeting
- Technical discussions on instance affinity and metrics
- Collect feedback on the direction and interest to move the work in IETF routing area 


## Introduction
Service providers are exploring the edge computing to achieve better response time and control over data by moving the computing services towards the edge of the network. 
There could be a huge number of edge sites, and at the same time each edge site has a limited and very dynamic computing capacity and load characteristics. 

Then the problem comes as how to optimally route service demands based on computing and network metrics to the best edge. 

Most current practices uses random or round robin way or use geographically closest one to decide the edge to handle the service demand. It considers the static characteristics like aliveness and geographical distance of edges. Dynamic status like computing load and network path status are not taken into account. In addition, the practices usually determine the best edge in respect to the computing and networking aspects separately rather than jointly.  

Dyncast (dynamic ancyast) tries to route the computing service demands based on computing and network metrics jointly at the network layer to improve the efficiency and latency. Three features are to be supported:
* Anycast based service addressing methodology 
* Flow affinity
* Computing Aware Routing

Dyncast tries to focus on:
* Specification of dyncast framework and functional components 
* Reuse existing IETF protocols when possible. Define protocol extensions when needed or introduce a new protocol when necessary including features like:
  - Represent service specific metrics like computing metrics in defined service/service instance context 
  - Distribute the metrics using routing protocol, potential inpact to the protocol like when metrics updates should be sent
  - Use  metrics in route determination
  - Definition of requirements for any new data plane extensions and procedures to ensure the instance affinity

Comments and suggestions are welcome. 
