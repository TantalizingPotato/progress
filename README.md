# Project Milestone
- Feasibility Study [3/18]
  - collect latest work of processing subgraph on GPU
  - collect latest work of techniques of subgraph query
  - analyze and find out which benchmark to use
  - analyze and find out if TCR can support all required operators
- Implement cypher on TCR [7/15]
  - design framework [4/8]
  - implement graph storage [4/23]
  - implement physical operators [5/23]
  - implement hand-optimized query plan towards LSQB or LDBC-SNB-IC or LDBC-SNB-BI [6/7] *
  - optimize implementation and hand-optimized query plan [7/7] *
  - finish implementation of cypher on TCR [7/15]
- Write SIGMOD paper and do experiments [10/7]
  - finish outline [8/7]
  - finish design experiments [8/7]
  - finish first draft [9/7]
  - finish experiments [10/1]
  - finish revision [10/7]
- SIGMOD paper submission [10/15]
- VLDB paper submission [2024/1/1] (if not accepted by SIGMOD)

> * we choose to implement LDBC-SNB-BI and are working on these now (6/25)

## Progress 7-20

### ✅ Finished 
1. built PyTorch from source code and set up the debugging environment.
2. learned the basic knowledge of TorchScript.
3. looked into the source code of PyTorch Geometric.
### 👷 In Progress
1. implementing LDBC BI queries Q16 and Q17 in our system.
2. learning Pytorch internals.
### 📈 To Do
1. to profile our running code and to see why some operators take much more time.


## Progress 7-13

### ✅ Finished 
1. implemented LDBI BI Q11, Q12, Q13, Q14, Q18.
2. finished the script that automatically runs all LDBC BI queries with pre-generated parameters in one time.
3. run LDBI BI queries on our system, TigerGraph and Neo4j with the scale factor of 10.
### 👷 In Progress
1. implementing LDBC BI queries Q16 and Q17 in our system.
2. learning Pytorch internals.
### 📈 To Do
1. to learn more about Pytorch Geometric.

## Progress 7-6

### ✅ Finished 
1. tried the scale factors of 10 and 100, but failed.
2. read the paper _Columnar Storage and List-based Processing for Graph Database Management Systems_.
3. implemented LDBC BI queries Q1 to Q10 (except for Q10, which involves shortest path computation).
### 👷 In Progress
1. implementing LDBC BI queries Q11 to Q20 in our system.
### 📈 To Do
1. to write a script that can automatically run our system on the LDBC BI queries and output the results to files in some format.
2. to learn more about Pytorch Geometric.

## Progress 6-29

### ✅ Finished 
1. run LDBC BI queries on Neo4j.
2. made our system support string filtering.
3. fixed some logical bugs about null value processing.
### 👷 In Progress
1. implementing LDBC BI queries in addition to Q1, Q5 and Q6 in our system.
### 📈 To Do
1. to try running our system on the datasets of scale-factor 10 and 100.
2. to read the VLDB 2021 paper _Columnar Storage and List-based Processing for Graph Database Management Systems_.
3. to learn more about Pytorch Geometric.

## Progress 6-21 

### ✅ Finished 
1. learned the syntax of GSQL (for TigerGraph) and Cypher (for Neo4j).
2. run LDBC SNB BI queries on TigerGraph.
### 👷 In Progress
1. implementing LDBC BI queries in addition to Q1, Q5 and Q6 in our system.
### 📈 To Do
1. to run LDBC BI queries on Neo4j.
2. to make our system support string filtering.
