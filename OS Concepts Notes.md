# Chapter 1  Overview
## Computer System  
1. __Hardware__  
(Basic computing resources)  
 * CPU(central processing unit)  
 * memory  
 * I/O devices  
2. __Operating system__  
(controls the hardware and coordinates its use among the various application programs for various users)   
Similar to the government, only provides an *__environment__* within which other programs can do useful work   
3. __Application programs__  
(defines the ways in which these resources are used to solve users' computing problems)   
4. __Users__  

## User point of view  

1. __PC__  
mostly for **ease of use** for **single user**  
with <u>some attention to performance</u> and <u>none to resource utilization</u>  
2. __Terminals connected to the mainframe or minicomputer__
maximize resource utilization (__efficiently__)  
no individual user takes more than her fair share.  
3. __Workstations connected to the networks of other workstations or servers__  
compromise between individual usability and resource utilization.  
4. __Mobile computers__  
Interacts the system with the *touch screen* by pressing or swiping fingers  
5. __Embedded computers__  
are designed primarily to run without user intervention.  


## System point of view  

1. *Resource Allocator*  
2. *Control program prevent errors and improper use of computer (IO)*  

## Brief history of OS  
1. Fundamental goal of computer systems:  
* execute user programs  
* make solving user problems easier.  
2. --> Since bare hardware alone is not particularly easy to use, application programs are developed.  
These programs require certain common operations, such as those controlling the I/O devices.  
3. -->The common functions of controlling and allocating resources are then brought together into OS  

*__Kernel__* Along with *System programs & Application programs *   
**OS** is the one program running at all times on the computer—usually called the kernel  

Nowadays, <u>mobile OS</u> include not only the kernel but also the *__middleware__*  
(a set of software frameworks that provide additional services to application developers)  

## Computer System organisation
CPU and controller devices can execute in parallel, competing the memory cycles. (Access to the memory by a single bus)

*__Bootstrap program__* is the initial program when the computer is powered up
Stored in the  
* __ROM__ (Read only memory)  
  cannot be changed, so only static programs
* __EEPROM__ (electrically erasable programmable read-only memory)  
  __firmware__
  can be changed but not frequently, so contains most static programs
  (e.g. factory-installed programs on mobiles)
To load and execute OS, bootstrap must locate the kernel and load it into the memory

__System processes (System daemons)__
Some services are provided outside of the kernel, run the entire time the kernel is running.
(And wait for the event occur)

Occurrence of an event is usually signaled by an *__interrupt__*  
* Hardware  
  Sending a signal to the CPU, by means of the bus  
* Software  
  Execute the __System Call__ (__Monitor Call__)  

--> CPU transfers what it is doing to a fixed location where contains the starting address where the interrupt service routine located  



## Storage Structure
Now many using semiconductor tech  

Since CPU can only load instructions from the memory,  
--> many computers use the __Main memory__ (__RAM__ random access memory)
which is rewritable and is implemented by __DRAM__ (dynamic random-access memory)

All forms of memory provide an array of bytes. Each byte has its own address.
Interactions are achieved by a sequence of *load* & *store*

*Load*  : Move a byte or a word  RAM -> internal register of CPU
*Store* : Vice Verse

Remark: CPU automatically loads instructions from main memory

Execution cycle: (example in _von Neumann architecture_)
1. Fetches instructions from memory
2. Stores in the instruction register
3. Being decoded and recursively execute the instructions possibly on the operands
4. Result maybe stored back in memory

__Secondary Storage__
such as __magnetic disk__
Stores the programs and data permanently.
!!! Disk management is crucial  

![Storage-device hierarchy](/Macintosh HD/Users/daviesxue/Downloads/Storage-device hierarchy)
trade-off  
Expensive but fast
-->  
Cheap but slow
