# Abstract of lecture Entity-Relationship Model
By Q&A Group 2012.10.24 \(^_^)/

##1.What should we do to the real world? [ER Model]
###Basic consept:	
Entity: A thing or object in the real world that is distinguishable from all other subjects.

Relationship: An association between instances of one or more entity types.

Attribute: A changeable property or characteristic of some component of a program that can be set to different values. 

Primary key: An attributes that can uniquely identify different entities. 

Entity Set: a set of entities of the same type that share the same properties, or attributes.

Relationship Set: a set of relationships of the same type.

Superkey: one attribute or several groups of attributes to distinct entities.

Candidate key: a minimal superkey. 

Mapping Cardinality: one to one, one to many, many to one, many to many.
####Question:
Can there be more than one relationship between two entity sets? Yes.

What decides the mapping cardinality? Relationship.

###Draw Entity-Relational Diagram
####Draw local ER diagram
Determine range of local structure
Define entity          
Define relationship         
Allocate attributes         
####Draw global ER diagram
Conflicts: name conflict, attribute conflict

##2.What if data change at different moments? [OOM]
###Main levels of object-oriented model:
Object model

State model

Functional model

##3.How can we create a better database? [Hybrid modeling]
###Reasons
Multimedia storage

Automatic detection

Code compression
###Methodology

Object relational database

Object relational mapping


##4.How can we realize our project and cooperate with the entire LWS?[Design patterns&DbC]

###Design patterns
####Base: OOD 
####Four basic ideas:
Object oriented

Re-usable

Variable with minimal effort

Extendable without change.

####SOLID principles

###Design by contract
Three contracts:
Pre-condition

post-condition

class invariant

##5.How to deal with worldwide users? [Accumulative data]
###Question2Answer functions: hotness, points, favorites, categories
###Revised data storage and query
###Data mining process
Step1 data preparation           
Step2 modeling  & data mining         
Step3 results validation 