 To view as a website, see: http://zhangyushao.site/awesome-database-testing/.
 
# Awesome-Database-Testing
This is a curitated list of resources on *database testing*.

**What covered: papers**, blogs, notes, tools and etc. for whoever wants to test a database mangement system (DBMS). 

**What is not**: using SQLs, learning database basic knowledge, implementing a database system.

**Note**: this is NOT an exhaustive list of materials, you may want to find more accroding to references of each item.


## High-level Views
Here we put materials with general discussions.

### Research Papers
**NOTE:** We only include peer-reviewed and published papers here, the same also applies to other entries. You may want to find the authors' *free-version* of the papers on their personal page.

*  *Understanding the query optimization*  [Query Optimization in Database Systems](https://dl.acm.org/doi/10.1145/356924.356928) [1984]
*  *Understanding the query optimization - a more recent view*  [An Overview of Query Optimization](https://www2.cs.duke.edu/courses/fall19/compsci516/Papers/chaudhuri98.pdf) [1998]
*  *What are the problems from the indutrial view*  [Testing SQL Server's Query Optimizer : Challenges , Techniques and Experiences](http://citeseerx.ist.psu.edu/viewdoc/summary?doi=10.1.1.143.3767)

*  *Optimizer Evaluation*  [How good are query optimizers, really?](https://www.vldb.org/pvldb/vol9/p204-leis.pdf)

### Others
*  *What are the problems from the academic view*  [Is Query Optimization a “Solved” Problem?](https://wp.sigmod.org/?p=1075)



## Input Generation

### Research Papers
*  *Query generation with template substitution*  [Generating Thousand Benchmark Queries in Seconds](http://linkinghub.elsevier.com/retrieve/pii/B9780120884698500917)
*  *Language for customized data generator*  [Flexible Database Generators](https://www.csd.uoc.gr/~hy460/pdf/Flexible%20Database%20Generators.pdf)
*  *RAGS Microsoft SQL Server*  [Massive Stochastic Testing of SQL](https://www.microsoft.com/en-us/research/publication/massive-stochastic-testing-of-sql/)
*  *Generate data regarding the query constraints*  [QAGen: Generating Query-Aware Test Databases](http://portal.acm.org/citation.cfm?doid=1247480.1247520)
*  *How could symbolic execution help*  [Qex: Symbolic SQL Query Explorer](http://link.springer.com/10.1007/978-3-642-17511-4_24)
*  *Data generation as a search problem*  [Search-based test data generation for SQL queries](http://dl.acm.org/citation.cfm?doid=3180155.3180202)
*  *For more valid inputs!* [SQUIRREL: Testing Database Management Systems with Language Validity and Coverage Feedback](https://arxiv.org/abs/2006.02398) [CCS 2021]

### Tools
*  Randgen [MySQL version (not maintained)](https://launchpad.net/randgen) [doc](https://github.com/RQG/RQG-Documentation/wiki/), [MariaDB version](https://github.com/MariaDB/randgen), [PingCAP version](https://github.com/pingcap/go-randgen) 
*  [pquery](https://github.com/Percona-QA/pquery) - stress testing MySQL
*  [Sysbench](https://dev.mysql.com/downloads/benchmarks.html) - MySQL benchmarks
*  [SQLsmith](https://github.com/anse1/sqlsmith) - fuzzing style tool
*  [Squirrel](https://github.com/s3team/Squirrel) - tool for CCS 2021 paper
*  [mtr_to_sql.sh](https://github.com/Percona-QA/percona-qa/blob/master/mtr_to_sql.sh)@Percona-QA - a script to extract [mysql-test](https://dev.mysql.com/doc/dev/mysql-server/latest/PAGE_MYSQL_TEST_RUN.html) cases as a sql file, with engine replacement and shuffles according to your need



## Engine Correctness
Here we mainly refer to the case where the engine returns wrong query result.

### Research Papers

#### What You Really Want to Know About
*  *RAGS with system-differential testing*  [Massive Stochastic Testing of SQL](https://www.microsoft.com/en-us/research/publication/massive-stochastic-testing-of-sql/)
*  *Data generation with contraints sovling*  [Query-Aware Test Generation Using a Relational Constraint Solver](http://ieeexplore.ieee.org/document/4639327/)
*  *Differential testing for the optimizing rules*  [A framework for testing query transformation rules](http://portal.acm.org/citation.cfm?doid=1559845.1559874)
*  *Criteria on integrtity testing*  [The Effectiveness of Test Coverage Criteria for Relational Database Schema Integrity Constraints](http://dl.acm.org/citation.cfm?doid=2852270.2818639)


#### What You Want to Know About
*  *Parallelism on the old machines*  [Quickly generating billion-record synthetic databases](http://portal.acm.org/citation.cfm?doid=191843.191886)
*  *Verified database system*  [Toward a Verified Relational Database Management System](http://portal.acm.org/citation.cfm?doid=1706299.1706329)
*  *Reply the transactions*  [Debugging transactions and tracking their provenance with reenactment]()

#### What's New
*  [Search-based test data generation for SQL queries](http://dl.acm.org/citation.cfm?doid=3180155.3180202) [2018]
*  [Automated verification of query equivalence using satisfiability modulo theories](http://dl.acm.org/citation.cfm?doid=3342263.3360343) [2019]
*  [Detecting Optimization Bugs in Database Engines via Non-Optimizing Reference Engine Construction](https://www.manuelrigger.at/preprints/NoREC.pdf
) [2020]
*  [Testing query execution engines with mutations](https://dl.acm.org/doi/10.1145/3395032.3395322) [2020]

### Tools
*  [SQLancer](https://github.com/sqlancer/sqlancer)@ETH_ZURICH
*  [go-sqlancer](https://github.com/chaos-mesh/go-sqlancer)@PingCAP
*  [pquery](https://github.com/Percona-QA/pquery)@Percona-QA - a tool providing the ability to combine correctness and crash recovery testing on both single-node and clustered instances



## Performance
Here we focus on detecting and debugging performance issues.

### Research Papers

#### What You Really Want to Know About
*  *Very first system*  [Efficient testing of high performance transaction processing systems](http://www.vldb.org/conf/1997/P595.PDF)
*  *Is the exact estimation possible*  [Exact Cardinality Query Optimization for Optimizer Testing](http://citeseerx.ist.psu.edu/viewdoc/summary?doi=10.1.1.151.6265)
*  *How to identify issues on plan generation*  [On the stability of plan costs and the costs of plan stability](http://dl.acm.org/doi/10.14778/1920841.1920983)
*  *What's wrong with the models*  [Testing cardinality estimation models in SQL server](http://dl.acm.org/citation.cfm?doid=2304510.2304526)

#### What You Want to Know About
*  *Generate and compare the plans*  [Testing the accuracy of query optimizers](http://dl.acm.org/citation.cfm?doid=2304510.2304525)

#### What's New
*  [APOLLO: Automatic Detection and Diagnosis of Performance Regressions in Database Systems](https://dl.acm.org/doi/10.14778/3357377.3357382) [2020]

### Tools
*  [TPC Benchmarking](http://www.tpc.org/)
*  [APOLLO](https://github.com/sslab-gatech/apollo)@gatech


## Industry Practice
We list idea and tools which are adopted in the industry.

### Tools
* [Chaos Mesh](https://github.com/chaos-mesh/chaos-mesh) from PingCAP
  *  Article: [Building an Automated Testing Framework Based on Chaos Mesh® and Argo](https://pingcap.com/blog/building-automated-testing-framework-based-on-chaos-mesh-and-argo)
  *  Talk: [Testing TiDB Using Chaos Mesh® with TiPocket](https://www.youtube.com/watch?v=60uCsnwNdU0)


## Contributors
*  [zhangysh1995](https://github.com/zhangysh1995)
*  [mkx22](https://github.com/mkx22)

# Contributions are Super Welcome!
What you can contribute:
*  papers (only peer-reviewed papers will be accepted to this repo)
*  talks/slides/articles
*  tools

Please also add yourself to *Contributors* in the PR.


