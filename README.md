# Dyncast (Dynamic Anycast) Virtual Side meeting in IETF 110

## Time: Wed (March 10) , 120min
   - UTC 10:00 - 12:00
   - CET (UTC+1) 11:00 - 13:00 - France/Germany/Prague
   - CST (UTC+8) 18:00 - 20:00 – Beijing/Singapore
   - EST (UTC-5) 05:00-07:00
   - PST (UTC-8) 02:00-04:00

Information also available on side meeting wiki: https://trac.ietf.org/trac/ietf/meeting/wiki/110sidemeetings

## Webex
- Webex Meeting number (access code): 181 922 3870
- Password: KNp7kdNSm62
- Password if joining from a phone: 56775367
- Webex: https://htf-paris.my.webex.com/htf-paris.my/j.php?MTID=m719b852a7d548c66eab00360562f645a

## Codimd for minute takers and attendance marking
https://codimd.ietf.org/notes-ietf-110-dyncast-side-meeting

## Link to slides
https://github.com/dyncast/ietf110/blob/main/dyncast-ietf110-side-meeting-full-deck.pdf

## Drafts:
- https://tools.ietf.org/html/draft-liu-dyncast-ps-usecases-01
- https://tools.ietf.org/html/draft-liu-dyncast-reqs-00
- https://tools.ietf.org/html/draft-li-dyncast-architecture-00
- https://www.ietf.org/archive/id/draft-bormann-dyncast-affinity-00.html


## Purpose of the virtual side meeting:
- Give an update on the use cases, problem space, requirements and architecture since last meeting
- Technical discussions on instance affinity and metrics
- Collect feedback on the direction and interest to move the work in IETF routing area 

## Agenda
1.	Admin [8: 8/120] 
2.	Problem statement, use cases and requirements (updates): Peng Liu (China Mobile) [15: 23/120] 
   - https://tools.ietf.org/html/draft-liu-dyncast-ps-usecases-01
   - https://tools.ietf.org/html/draft-liu-dyncast-reqs-00
3.	Dyncast architecture (updates): Luigi Iannone [10 : 33/120]
   - https://tools.ietf.org/html/draft-li-dyncast-architecture-00
4.	Questions and Recap of the feedback received[20: 53/120]
5.	Specific technical topics – Moderator: Dirk Trossen (37: 90/120)
   - Service affinity  (27’)
      - Basic approach, aspects to consider – Dirk Trossen (7’)
      - Time period based affinity – Carsten Bormann(7’)
         - https://www.ietf.org/archive/id/draft-bormann-dyncast-affinity-00.html
     - Discussions, e.g. pros and cons, direction to go, allow multiple solutions for different use case? (13’)
   - Metrics discussion (10’)
6.	Wrap up and next steps (chairs) [20 : 110/120]


## Introduction
Service providers are exploring the edge computing to achieve better response time and control over data by moving the computing services towards the edge of the network. 
There could be a huge number of edge sites, and at the same time each edge site has a limited and very dynamic computing capacity and load characteristics. 

Then the problem comes as how to optimally route service demands based on computing and network metrics to the best edge. 

Most current practices uses random or round robin way or use geographically closest one to decide the edge to handle the service demand. It considers the static characteristics like aliveness and geographical distance of edges. Dynamic status like computing load and network path status are not taken into account. In addition, the practices usually determine the best edge in respect to the computing and networking aspects separately rather than jointly.  

Dyncast (dynamic ancyast) tries to route the computing service demands based on computing and network metrics jointly at the network layer to improve the efficiency and latency. Three features are to be supported:
* Anycast based service semantic addressing 
* Instance affinity
* Computing Aware Routing

Dyncast tries to focus on:
* Specification of dyncast framework and functional components 
* Reuse existing IETF protocols when possible. Define protocol extensions when needed or introduce a new protocol when necessary including features like:
  - Represent service specific metrics like computing metrics in defined service/service instance context 
  - Distribute the metrics using routing protocol, potential inpact to the protocol like when metrics updates should be sent
  - Use  metrics in route determination
  - Definition of requirements for any new data plane extensions and procedures to ensure the instance affinity

Comments and suggestions are welcome. 
