# citusdb_ri
CitusDB Reference Implementation

##### Installation Guide
[https://docs.citusdata.com/en/stable/installation/multi_node_rhel.html](https://docs.citusdata.com/en/stable/installation/multi_node_rhel.html) <br/>

##### Citus Single/Distributed Diagram
![Citus S/D Diagram](https://github.com/lel99999/citusdb_ri/blob/master/citus-01.png) <br/>

##### Upgrade Path v7.x -> v11.x
1. v7.2 + PG10 <br/>
2. v9.0 + PG10 <br/>
3. v9.0 + PG12 <br/>
4. v10.2 + PG12 <br/>
5. v10.2 + PG13/PG14 <br/>
6. v11.0 + PG13/PG14 <br/>

Notes: <br/>
- Only step 6 should use the open-source packages <br/>
- 2-5 should be enterprise packages, otherwise you’ll miss features <br/>


