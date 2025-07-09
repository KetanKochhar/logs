

## Day 8

### MKLO lecture converted to DBMS lecture 
#### Data Abstraction 
**Data Abstraction** is the process of hiding the internal implementation details and showing only essential features of an object or system.
[[data abstraction diagram.canvas|Diagram]] 

1. What is Instance ?
	- **instance** refers to the **actual data** stored in a database at a specific moment in time.
	- It **changes frequently** as data is inserted, deleted, or updated.
2. What is schema ?
	- A **schema** is the **structure or blueprint** of a database that defines how data is organized.
	- It **does not change frequently**.

#### Types of Users
1. Native / End Users 
2. Application programmers 
3. Sophisticated Users
4. Specialized users / DMA(DataBase Adminastor)

#### Roles of DBA 
- Define the **schema**
- Set up **storage structures** and **access methods**
- Implement **security** and **integrity constraints**
- Assist **application programmers** with queries
- **Monitor performance**
- Manage **backup and recovery**
#### Languages of DBMS 

1. - **DDL** → Data Definition Language
    - Used to define the **schema**
- **DML** → Data Manipulation Language
    - Used to **insert, delete, and update** data
- **DCL** → Data Control Language
    - Used to **control access and permissions** in the database


___
### EHF Lecture 
1. What is CIA Triad ?
	- **C**onfidentiality
	- **I**ntegrity
	- **A**vailability
2. write the phases of hacking 
	- 
3. write types of hackers 
	- White Hat Hackers
	- Black Hat hackers
	- Grey Hat Hackers
4. what are the Consequences of hacking 
	- Data loss or theft 
	- Financial loss
	- Legal consequences
	- Damage to reputation
	- System downtime
5. MS-DOS commands 
	- `attrib` – View or change file attributes
	- `xcopy` – Copy files and directories (advanced copy)
	- `format` – Format a disk
	- `chkdsk` – Check and fix disk errors
	- `netstat` – Display network connections
6. Linux commands 
	- `ls` – List directory contents
	- `cd` – Change directory
	- `mkdir` – Create a directory
	- `rmdir` – Remove a directory
	- `cat` – Display file contents
	- `echo` – Display messages
	- `chmod` – Change file permissions
	- `chown` – Change file ownership
	- `ifconfig` – Display network configuration
	- `rm` – Remove files or directories
	- `mv` – Move or rename files
	- `cp` – Copy files or directories
	- `pwd` – Print working directory
	- `man` – Manual/help for commands
	- `top` – Real-time system info
	- `ps` – Display running processes
	- `kill` – Terminate processes
	- `grep` – Search text using patterns
	- `df` – Show disk space usage
	- `whoami` – Show current user


___

### DBMS converted to DS 

Monali ma'am started the new chapter 3 -> Non-liner data structures 

what is herichal structure of tree ?
- A tree is a non-linear data structure where elements are arranged in a **hierarchical** manner (like a family tree).

#### **Terminologies**
- **Node**: An element of the tree
- **Child Node**: Node directly connected below a given node
- **Parent Node**: Node directly connected above a child node
- **Root Node**: The top-most node in a tree
- **Leaf Node / Terminal Node**: A node with **no children**
- **Internal Node**: A node with at least one child
- **Edge / Branch**: The link between parent and child nodes
- **Path**: Sequence of nodes from root to a specific node
- **Depth**: Distance (in levels) from root to a node
- **Height**: Maximum depth of the tree
- **Sibling**: Nodes having the same parent
- **Subtree**: A smaller tree from a node and its descendants

#### Condition for binary tree 
- A tree in which **each node** has **0, 1, or 2 children** is called a **binary tree**
#### Condition for complte binary tree
- A binary tree in which **all levels are fully filled** except possibly the **last level**, which is **filled from left to right**

#### Operations on the binary tree 
- **Create** 
- **Insert**
- **Update**
- **Delete**

#### functions on tree
- Pre order : N$\longrightarrow$L$\longrightarrow$R
- In order : L$\longrightarrow$N$\longrightarrow$R
- Post order : L$\longrightarrow$R$\longrightarrow$N

#### **Indexing in Array Representation**
- **Root Node** → index = 0
- **Left Child** → `2i + 1`
- **Right Child** → `2i + 2`
- **To find parent of node at i** → `(i - 1) / 2` (integer division)


#### Pseudo code for pre order function 

```c
PreOrder(Root) {
    if (Root != NULL) {
        printf(Root->data);
        PreOrder(Root->left);
        PreOrder(Root->right);
    }
}
```

#### Exercise Binary tree 

Write post order for this tree [[Binary tree.canvas|ref 1st tree]] 
- Ans `A,B,D,E,C,G`

Write Pre order for this tree [[Binary tree.canvas|ref 2nd tree]]
- Ans `G,H,A,B,C,I,F,M,O,P`

