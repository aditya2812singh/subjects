### STEPS TO BE FOLLOWED FOR DESIGNING UVM TB

Basic and Simple Blueprint to structure a project in UVM [Important for VLSI Professionals]

UVM is a preferred verification language due to its reusability, scalability, interoperability, CRV, proper phasing, etc.

Below are the most simplest basic steps mentioned as how to develop a TB infrastructure from scratch.

**Step 1: Documentation**

✓ Go through the specification thoroughly and prepare the Verification Plan, Test Plan, Assertion Plan and understand the working of the IP or protocol.

**Step 2: Coding**

✓ Code the interface by listing all the I/O port. Code the Clocking block to avoid race condition, synchronization and direction to TB. Optionally code the Modport.

---

Note: Cautiously use the input / output skew and the clockvar

There are certain rules while using the Clocking block and modport which someone needs to follow.

---

✓ Code the transaction class and use the randomization wherever applicable. Try to avoid the field macros and instead use proper methods.

**General thumb rule the input should be rand.
Moreover try to use the do_copy, do_ compare, convert2string, do_print methods instead of using field macros which has a overhead**

✓ Code the driver logic for the pin level activity at DUT. Use sequencer driver handshake properly depending on pipelined / non pipelined access.

---

Use proper coding guidelines while coding driver logic

---

✓ Code the Sequencer and use arbitration mechanism if needed.

✓ Code the Monitor to handle the transaction. The analysis port first needs to be connected to Agent and then to other subscribers like scoreboards, etc.

✓ Build the agent and give proper instantiation for Driver, monitor, and Sequencer. Depending on application the Agent can be chosen as either active or passive.

✓ Code the env class and give proper connection.

✓ Write some basic sequence items to check the flow along with base test class. While coding the sequence items number of methods can be used to execute the sequence.

** While using the sequence use start_item/finish_item instead of `uvm_do macro **

✓ Code the scoreboard either with the help of tlm fifo, associative array, queue depending on whether it's used in order or out of order comparator. The coding style will change depending on need.

** While designing the Scoreboard make sure the predictor and evaluator are separate**

There are almost **6 to 7 different methods** of designing a scoreboard

✓ Code the top module and use of run_test and set the config db.

---

Above are some of the very basic steps mentioned but ideally the testbench will be complex and use many more concepts which are not mentioned above. Some of them are:

✓ Virtual Sequencer and Virtual Sequences.
✓ RAL
✓ Callbacks
✓ Objection mechanism
✓ Config and resource db
✓ Coverage
✓ Assertions




//.................HOW TO STUDY UVM.....................................
UVM emerged as a preferred Verification language since last several years along with SystemVerilog, Python, Verilog, OVM as the other alternatives depending on the kind of project and execution style.

There are multiple ways as how UVM can be learnt from the scratch and few points are mentioned below:

[1] Download UVM 1.2 accellera user guide and go through it thoroughly to understand the below concepts.

a. TLM understanding, Port export connection and difference b/w TLM1 and TLM2

b. Transaction class and how to model it. Understanding of respective UVC's like Driver, Monitor, Sequencer, Scoreboard, Agent, Sequencer Driver interaction. Verification environment understanding and related coding of UVC

c. Configuration mechanism and it's requirement, Test writing.

d. Register Access Layer and it's usefulness in accessing registers.

e. UVM Testbench infrastructure understanding, communication b/w each component and object. UVM phasing mechanism.

[2] Download the UVM cookbook from verification academy and also go through the related concepts like

a. UVM TB development and run test mechanism.
b. Objection control mechanism and analysis components.
c. Sequencer and Sequences.
d. Modelling style of UVC.
e. Sequence writing.
f. Different types of scoreboard implementation.
g. RAL

[3] The next step is to put all the learning into practice. Take any simple IP like a memory controller or a FIFO and try to build a Verification environment. You can use edaplayground to test the code and one can also take the help of opencores webpage for any other project.

***
How to code a verification env in UVM from scratch will be covered in next post

****

[4] Once the basics and fundamentals are clear, the next step is to learn further. For that download "The UVM class reference manual" and can have a look at following topics:

a. UVM barriers.
b. UVM domain, phase jumping, run time phases, user defined phases.
c. Classes related to synchronization, triggering, etc.
d. UVM resource db.
e. Other classes that can be used to build TB framework.
f. UVM callbacks

[5] As a next step to enhance the learning someone needs to go through research papers, papers published in conferences, discussing with colleagues and mentors, etc.
