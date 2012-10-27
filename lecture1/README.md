## Relational model
###Overview
* **What is Relational Model**

  A kind of data model whose ENTITIES and the RELATIONSHIP BETWEEN ENTITIES is expressed by TABLES
* **Formulation and Proposal**

  “A Relational Model of Data for Large Shared Data Banks”, E.F.Codd, 1970
* **Principle**

  The basic principle of the relational model is the Information Principle: all information is represented by data values in relations. In accordance with this Principle, a relational database is a set of relvars and the result of every query is presented as a relation.
* **Implementation**

  SQL data definition query language

* **Alternatives**

  Hierarchical Model, Network Model, Object-Oriented Model (New)
* **Three Main Components**
  * Relational Data Structure
  * Relational Operating Set
  * Relational Integrity Constraints

###Relational Data Structure
* **Basic Structure**

  Aggregation of tables
* **Relations or Tables**

  A relation is defined as a set of TURPLES (in Row) that have the same ATTRIBUTES (in Column) .The permitted value of an attribute is called DOMAIN. A tuple usually represents an object and information about that object. Objects are typically physical objects or concepts.  
* **Relation Schema**

  Relation Schema is a description of relation
  * Table Heading: Define the relation schema 
  * Table Body: Correspondent to relations

  Expression r(U, D, DOM, F) 
  * r: relation name
  * U: Aggregation of attributes
  * D: Aggregation of the Domains, to which attributes belong
  * DOM: Aggregation of the functions from attributes to domains
  * F: Aggregation of data dependence between attributes.

* **Relation Schema & Relation Instance**
  * RS:  Type
  * RI:	Value
* **Key**
  * Superkey: Aggregation A of one or more attributes, and A can uniquely note one tuple of relation r.
  * Candidate Key: Aggregation A of one or more attributes, and A can uniquely note one tuple of relation r. No proper subsets of A can be a superkey of r.
  * Primary Key: If there are two or more candidate keys of a relation, one of them can be chosen to be a primary key.
  * Null: A value means nonexistence or unknown. 

###Relational Operating Set
* **Characteristics**

Operate with SET
* **Relational Operations**
  * Query (Select, Projection, Join, Restrict, Difference, Union, Intersection, Product)
  * Modify (Insertion, Deletion, Update)

###Relational Integrity Constraints
* **Domain Integrity**

  The domain integrity states that every element from a relation should respect the type and restrictions of its corresponding attribute. A type can have a variable length, which needs to be respected. Restrictions could be the range of values that the element can have, the default value if none is provided, and if the element can be NULL.
* **Entity Integrity**

  The entity integrity constraint states that no primary key value can be null. This is because the primary key value is used to identify individual tuples in a relation. Having null value for the primary key implies that we cannot identify some tuples. This also specifies that there may not be any duplicate entries in primary key column key row.
* **Referential Integrity**

  The referential integrity constraint is specified between two relations and is used to maintain the consistency among tuples in the two relations. Informally, the referential integrity constraint states that a tuple in one relation that refers to another relation must refer to an existing tuple in that relation. It is a rule that maintains consistency among the rows of the two relations.
* **User Defined Integrity**

  The data should respect both entity integrity and referential integrity. Besides, it should also respect the constraints defined by users in a specific relational database.


### Normalization
Sometimes we can’t retrieve the information correctly and there is redundancy in our data. These are because the relation schema of our relation model is not appropriate. We can use the database normalization to solve this problem.

* **First normal form (1NF)**
  * definition

    A relation is in first normal form if the domain of each attribute contains only atomic values, and the value of each attribute contains only a single value from that domain. (A domain is atomic if elements of domain are considered to be indivisible units.)1NF is an essential property of a relation in relation database.
  * Example

    Example is that if an attribute is your class_info that contains department and class, this relation is not in 1NF. We should divide this attribute into two attributes: department and class.

* **Second normal form (2NF)*
  * definition

    A relation R is in second normal form if and only if it is in 1NF and every non-key attribute A of R is such that the set {A} is irreducibly dependent on every key of R. In other word, there is no non-key attribute that has partial function on key.
  * Example

    We consider a relation named “StudyInfo”, which has attributes of {Student_No, Student_name, DeptName, DeptHead, Course_name, Grade}. 

    The key of a relation “StudyInfo” is {Student_No, Course_name}, and Student_name and DeptName are only dependent on Student_No. This may result in that when we delete a grade of a student, we have to delete the basic information of the student at the same time.

    So we should divide this “StudyInfo” into two relations: 
StudentDept {Student_No, Student_name, DeptName, DeptHead},
and Report { Student_No, Course_name, Grade}.

* **Third normal form (3NF)**
  * definition

    A relation is in third normal form if and only if it is in 2NF and there is no transitive functional dependencies between two or more non-key attributes.
  * Example

    We still consider the example above in 2NF. There is a transitive functional dependency in StudentDept: 

    Student_No-> DeptName-> DeptHead. We may have trouble when we want to create a new Department and there is still no student in it. So we should divide StudentDept into two relations:

    Student { Student_No, Student_name, DeptName}, and Department { DeptName, DeptHead}.

* **Boyce-Codd normal form (BCNF)**

  Boyce-Codd normal form is a slightly stronger version of the 3NF developed in 1974 by Raymond F. Boyce and Edgar F. Codd. A relation schema R is in BCNF if and only if for every one of its dependencies X->Y, at least one of the following conditions hold: (a) X->Y is a trivial functional dependency (Y is in X); (b) X is a super key for schema R.


* **Forth normal form (4NF)**
  * definition
    A relation is in 4NF if and only if, for every one of its non-trivial multivalued dependencies X->->T, X is a super key.

  * other normal form
    There are some other high levels normal forms such as Fifth normal form (5NF) (1979), Domain/key normal form (DKNF) (1981), and Sixth normal form (6NF) (2002).

-------------------------------