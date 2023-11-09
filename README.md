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

## Progress 11-9

### ✅ Finished 
1. finished implementing all currently supported LDBC BI queries.
### 👷 In Progress
1. writing the paper.
2. learning PyTorch internals.
3. doing ablation study
### 📈 To Do
1. to do scalability test.
2. to do other experiments like query time breakdown and Performance Per Dollar test.

## Progress 11-2

### ✅ Finished 
1. finished and improved the implementation of `TreeTable`, a class bringing in the graph-ralated optimization.
2. conducted comparison experiments on implemented LDBC BI benchmark queries.
3. conducted comparison experiments on LSQB benchmark queries.
### 👷 In Progress
1. writing the paper.
2. implementing remaining LDBC BI queries in our system.
3. learning PyTorch internals.
### 📈 To Do
1. to do ablation study.
2. to do scalability test.
3. to do other experiments like query time breakdown and Performance Per Dollar test.

   
## Progress 10-5

### ✅ Finished 
1. finished the draft of the main part of paper.
2. implemented the `expand_tree` method of `TreeTable`.
### 👷 In Progress
1. writing the paper.
2. implementing the graph-related optimisation method into our system.
3. implementing other LDBC BI queries using new techniques.
4. implementing remaining LDBC BI queries in our system.
5. learning PyTorch internals.
### 📈 To Do
1. to implement `expand_tree` and `TreeTable` and test the performance of implemented graph-related optimisation.
2. to learn about more join methods, like zip join and radix join.
3. to think about the way we systematically test the performance of PyTorch Tensor operators on CPU and GPU.
4. to think about the possibility of making CPU and GPU cooperate better.


## Progress 9-21

### ✅ Finished 
1. designed the preliminary structure of the paper and started writing the paper.
2. re-implemented LDBC BI Q9, Q11 and Q12 using `EdgeTable` and `PathTable`, in addition to Q1-Q8.
### 👷 In Progress
1. writing the paper.
2. implementing the graph-related optimisation method into our system.
3. implementing other LDBC BI queries using new techniques.
4. implementing remaining LDBC BI queries in our system.
5. learning PyTorch internals.
### 📈 To Do
1. to implement `expand_tree` and `TreeTable` and test the performance of implemented graph-related optimisation.
2. to learn about more join methods, like zip join and radix join.
3. to think about the way we systematically test the performance of PyTorch Tensor operators on CPU and GPU.
4. to think about the possibility of making CPU and GPU cooperate better.


## Progress 9-14

### ✅ Finished 
1. improved and further completed the implementation of `PathTable` and `EdgeTable`.
2. re-implemented LDBC BI Q1 to Q8 using `EdgeTable` and `PathTable`, and compared the performance with previous implementation.
### 👷 In Progress
1. implementing the graph-related optimisation method into our system.
2. implementing other LDBC BI queries using new techniques.
3. implementing remaining LDBC BI queries in our system.
4. learning PyTorch internals.
### 📈 To Do
1. to implement `expand_tree` and `TreeTable` and test the performance of implemented graph-related optimisation.
2. to learn about more join methods, like zip join and radix join.
3. to think about the way we systematically test the performance of PyTorch Tensor operators on CPU and GPU.
4. to think about the possibility of making CPU and GPU cooperate better.

## Progress 9-7

### ✅ Finished 
1. implemented `get_neighbors` in `EdgeTable`.
2. implemented `select`, `project`, `aggregate`, `distinct` and `sort` in `PathTable`.
3. re-implemented LDBC BI Q3 and Q4 using `EdgeTable` and `PathTable`, and compared the performance with previous implementation.
### 👷 In Progress
1. implementing the graph-related optimisation method into our system.
2. implementing other LDBC BI queries in addition to Q3 and Q4 using new techniques.
3. implementing remaining LDBC BI queries in our system.
4. learning PyTorch internals.
### 📈 To Do
1. to implement `expand_tree` and `TreeTable` and test the performance of implemented graph-related optimisation.
2. to learn about more join methods, like zip join and radix join.
3. to think about the way we systematically test the performance of PyTorch Tensor operators on CPU and GPU.
4. to think about the possibility of making CPU and GPU cooperate better.

## Progress 8-31

### ✅ Finished 
1. implemented node renumbering and EdgeTable preprocessing.
2. implemented `expand_path` in `PathTable` and `closure` in `EdgeTable`.
### 👷 In Progress
1. implementing the graph-related optimisation method into our system.
2. implementing remaining LDBC BI queries in our system.
3. learning PyTorch internals.
### 📈 To Do
1. to implement `expand_tree` and test the performance of implemented graph-related optimisation.
2. to learn about more join methods, like zip join and radix join.
3. to think about the way we systematically test the performance of PyTorch Tensor operators on CPU and GPU.
4. to think about the possibility of making CPU and GPU cooperate better.

## Progress 8-17

### ✅ Finished 
1. profiled our running code and found that `torch.bincount` takes too much time on GPU in Q3 and Q4, while  `torch.unique ` and  `torch.sort` are relatively slow on CPU.
2. designed a graph-related optimisation method for our system, in which we compress the edge table and intermediate join results.
### 👷 In Progress
1. implementing the graph-related optimisation method into our system.
2. implementing remaining LDBC BI queries in our system.
3. learning PyTorch internals.
### 📈 To Do
1. to learn about more join methods, like zip join and radix join.
2. to think about the way we systematically test the performance of PyTorch Tensor operators on CPU and GPU.
3. to think about the possibility of making CPU and GPU cooperate better.


## Progress 8-3

### ✅ Finished 
1. tested the effects of optimizations implemented last week on different queries and different scale factors.
### 👷 In Progress
1. profiling our running code to see which operators take more time and trying to analyze the reason.
2. implementing remaining LDBC BI queries in our system.
3. learning PyTorch internals.
### 📈 To Do
1. to think about the possibility of making CPU and GPU cooperate better.
2. to add graph-specific optimisations into our system.

## Progress 7-27

### ✅ Finished 
1. implemented some basic optimisations like merging _filter_ and _project_, merging _join_ and _project_.
### 👷 In Progress
1. profiling our running code to see which operators take more time and trying to analyze the reason.
2. implementing remaining LDBC BI queries in our system.
3. learning PyTorch internals.
### 📈 To Do
1. to think about the possibility of making CPU and GPU cooperate better.
2. to add graph-specific optimisations into our system.

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
2. learning PyTorch internals.
### 📈 To Do
1. to learn more about PyTorch Geometric.

## Progress 7-6

### ✅ Finished 
1. tried the scale factors of 10 and 100, but failed.
2. read the paper _Columnar Storage and List-based Processing for Graph Database Management Systems_.
3. implemented LDBC BI queries Q1 to Q10 (except for Q10, which involves shortest path computation).
### 👷 In Progress
1. implementing LDBC BI queries Q11 to Q20 in our system.
### 📈 To Do
1. to write a script that can automatically run our system on the LDBC BI queries and output the results to files in some format.
2. to learn more about PyTorch Geometric.

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
3. to learn more about PyTorch Geometric.

## Progress 6-21 

### ✅ Finished 
1. learned the syntax of GSQL (for TigerGraph) and Cypher (for Neo4j).
2. run LDBC SNB BI queries on TigerGraph.
### 👷 In Progress
1. implementing LDBC BI queries in addition to Q1, Q5 and Q6 in our system.
### 📈 To Do
1. to run LDBC BI queries on Neo4j.
2. to make our system support string filtering.
