### **Intro**

Below are the most important concepts that are needed to understand the role of "OOP" in SV or UVM which are missing in Verilog.

[1] What is Class and Object? Difference between handle and Object.

[2] How memory allocation and deallocation is performed in Class. Difference b/w C pointer and SV object handle.

[3] What is the use of constructor and how does constructor chaining is achieved.

[4] How accidental overriding of base class methods are avoided.

[5] Difference between Shallow copy and Deep copy. What are the things can be copied in Shallow Copy.

[6] What is this construct in Class. What are Static methods in Class.

[7] What is Inheritance. Difference between Multilevel and Multiple Inheritance. How does Data hiding property in Class is achieved.

[8] How does Class extension can be restricted so that no subclass can inherit a parent class.

[9] Difference b/w Static and Dynamic Casting. Application of casting in subclass and Superclass.

[10] How a Class can be made read only. What are Virtual methods in Class.

[11] Concept of Polymorphism and Abstract Class. What is an Interface Class and what it is used for.

[12] How scope resolution operator is useful in accessing the static variables in the class.

[13] Use of parameterised classes and when it is used. Default value of class constructor and its purpose.

[14] How does Class allows access to the object during automatic garbage collection and what method needs to be used during that time.

[15] Concept of memory management and weak memory references. Code reachability.

[16] What is the role of composition in class.

[17] Concept of class Aggregation.

[18] Role of pure virtual methods and how to use it.

[19] Can virtual class be extended from non virtual class.

[20] Difference between an extend and implement.

[21] Concept of upcasting and downcasting. Which one is allowed and why.** **

### Question to Cover:BASIC

[1] Concept of virtual interface and how it can connect DUT with an Verification Env. What is a Test harness.

[2] How virtual interface flow in a testbench and ultimately reach driver to interact with DUT.

[3] Basic phasing mechanism like build, connect, run, etc (ignore run time phase initially)

[4] Concept of run_test() in top module and why it is needed.

[5] Clock generation module in top module and flow of uvm config.

[6] Difference between uvm_object and uvm_component. Classification of uvm_object.

[7] TLM interconnection in UVM. Role of producer and consumer. Concept of pull port and pull import.

[8] Difference between export and imp connection. Different types - port to port, port to export, port to imp, export to export, etc.

[9] Sequencer and Driver handshaking mechanism. How start_item of sequence and get_next_item of driver are related.

[10] How a sequence can be started - Different methods like `uvm_do or start to finish item. How a sequence can be started within a sequence or from a Test - Execution difference.

[11] What is a scope in uvm_config_db and how to set in various context - like from top module, from a component or even creating a config object.

[12] Different arbitration mechanism within a sequencer. What is user arbitration.

[13] Role of Analysis port. Difference between TLM and analysis port. What is a write function.

[14] Concept of subscriber class and how to handle multiple write function.

[15] What is a Virtual Sequence class. Can a environment be created without virtual sequencer which has multiple Agents.

[16] Difference between `uvm_do, `uvm_do_on, `uvm_do_pri.

[17] How to model a transaction class and why it is necessary to implement constraint in transaction.

[18] Concept of factory registrationand factory override - different types. Why analysis port doesn't use factory mechanism.

[19] How a sequence can be started - Execution flow.

[20] How to raise and drop Objection in UVM. Why drain time is needed.

### Question to Cover:Intermediate

[1] Concept of Domain synchronization in UVM. Why it is needed. Use of sync / unsync construct. Why scheduling is needed in UVM.

[2] Run time phases of UVM. What are their advantages and when they can be used. How to implement custom phase or user defined phases in UVM.

[3] Difference between p_sequencer and m_sequencer. Reason of existance of m_sequencer in UVM.

[4] How to inject errors in a UVM testbench and verify the functionality and robustness.

[5] What is phase_ready_to_end method in objection in UVM. Is it required to raise/drop objection in UVM in every sequence and component.

[6] What are the different ways of configuring a verification environment in UVM. Different methods apart from set/get methods in config db.

[7] Difference between uvm tlm fifo and uvm tlm analysis fifo. How write functions are synchronized during comparing data transactions.

[8] What is TLM 2.0 and how it is different from TLM 1.0. Use case of TLM 2.0

[9] What is the role of Predictor in a Scoreboard. Why Agent has an analysis port within it. Role of Analysis port within a Driver.

[10] How to model interrupts in UVM or an ISR.

[11] How to implement user mode of arbitration in UVM. How transactions are processed in an arbitration queue.

[12] Concept of response handler in UVM. Role of uvm barrier and uvm barrier pool and why are they needed.

[13] How Sequential, Concurrent and Hierarchical Sequences are processed in UVM. How composition can be useful.

[14] Different ways of assigning priority in sequence execution. What is a sequence library. Multi threaded behaviour of sequence.

[15] How to bypass the priority of sequence if needed.

[16] How to create a subenv within an env. How virtual sequence can control an sub env. What is the concept of layering.

[17] How to develop reset synchronized driver. Importance of clockvar in driver code. Different blocking / nonblocking methods used in driver.


### Sougata Bhatacharjee LinkedIN

**There are multiple components and objects which build the UVM testbench hierarchy. Among them, one important block is Agent which has three components Sequencer, Driver and Monitor.Below concepts are useful in learning the structure in detail:**

✓ Sequencer <--> Driver handshaking mechanism for
a. Only for req Id.
b. Both req and RSP
c. Pipelined and Non Pipelined access
d. Wait States

✓ Use of Non blocking assignment in Driver logic code why?

✓ How to use clockvar in Driver.

✓ Configuration mechanism in Driver. Can we use UVM resource db.

✓ Factory registration and factory override.

✓ Use of function new()

✓ How to start a sequence item and randomize.

✓ How to handle multiple sequence item through Sequencer --> Use of arbitration algorithm.

✓ How to handle interrupts

✓ What is user arbitration and need of it

✓ Use of analysis port and TLM port. How to connect analysis port to subscribers.

✓ Different types of Port export connection.

✓ Use of p / m sequencer.

✓ How write function needs to be implemented.

✓ Difference b/w active and passive agent.

✓ Why Monitor uses new() instead of create method.

✓ Difference b/w TLM1.0 and TLM2.0

Range of useful topics and questions related to UVM for ASIC Verification in VLSI - Part 2

[1] What are the differences between Analysis port and TLM port. Can we use analysis port for sequencer / Driver interaction and TLM port for Monitor / Scoreboard interaction. Is it possible.

[2] Difference between UVM Object and UVM component. How many minimum no. of Tasks, Function and Classes are required to build a testbench infrastructure (approximate)

[3] Objection in UVM. How to raise and drop objection in UVM. What is drain time. Different callbacks in objection control.

[4] How multiple sequences can be connected to a single Driver and how to control stimulus on multiple drivers.

[5] Difference between start_item / finish_item and `uvm_do and which one to choose for sequence item. What is late randomization.

[6] What is set_id_info and Cloning and why they are required. What are the different ways through which sequencer and driver interact with each other.

[7] What are the different Arbitration algorithms in UVM. What is user arbitration.

[8] What is the significance of grab() and lock() methods in UVM. How interrupts can be controlled. How to implement a ISR in UVM.

[9] What is the difference between Generator and a Driver. Can they be interchanged and be implemented with the help of Mailboxes.

[10] Configuration mechanism in UVM. Difference between uvm_config_db and uvm_resource_db and what are the different methods associated with it.

[11] What is Factory registration. Difference between set type / set instance override.

[12] What are Virtual Sequencer and Virtual sequences and what are their usage.

[13] How the scoreboard needs to be modelled to handle in order and out of order data comparison.

[14] How to model a Driver for pipelined and non pipelined access.

.......................................

[1] UVM Phasing Mechanism and how it executes. What is the role of reset, configure, main and shutdown phase of run phase.

[2] Which Phases are categorised into task and function. Which Phases are divided into top down and bottom up approach.

[3] Conditions and need to introduce domain Synchronisation and Phase jumping in UVM Phasing Mechanism.

[4] Role of run_test in top module and its importance. Why UVM is called a DAC and role of uvm_root.

[5] Difference b/w physical and Virtual interface. How VIF actually works in UVM and how it flows in testbench hierarchy.

[6] Generic role of UVC's like Driver, Monitor, Scoreboard, etc.

[7] What is Configuration in UVM. Difference b/w uvm_config_db and uvm_resource_db.

[8] Sequencer to Driver handshaking mechanism flow for unidirectional, Bidirectional and Pipelined transfer.

[9] Difference between uvm_component, uvm_object and uvm_transaction. What will happen if we don't use component and object utils macro.

[10] What is Factory registration in UVM. Concept of factory override and it's different type.

[11] Difference between TLM port and analysis port. Difference between port, export and imp. What are hierarchical exports.

[12] Objection mechanism in UVM and importance raise and drop objection.

[13] Sequence item flow and how to start a test / sequence. How to create a library of sequence.

[14] Why Driver run phase uses only nonblocking assignment and not blocking.

[15] How UVM handle race conditions and detect them.


### UVM TLM QUESTIONS:

1️⃣ What is TLM?
2️⃣ How is TLM better than a mailbox-based connection?
3️⃣ What is the difference between the Push and Pull models?
4️⃣ What are port, implementation, and export, and how do they differ?
5️⃣ Explain bidirectional communication in TLM with an example.
6️⃣ How does the driver-sequencer TLM connection work?
7️⃣ Where do we use put and get methods in TLM communication?
8️⃣ How is the analysis model different from the push model in TLM?
9️⃣ What base class is used for implementing coverage class, and how does it connect to the monitor?
🔟 What base class is used for implementing a scoreboard, and how does it connect to multiple monitors?
1️⃣1️⃣ Why is `uvm_sequence_item` used for implementing transactions between driver and sequencer instead of `uvm_transaction`?
1️⃣2️⃣ How do we give response transactions from driver to sequencer?
1️⃣3️⃣ What is the difference between blocking and non-blocking communication models in TLM?
1️⃣4️⃣ Explain the UVM analysis model using an example.
1️⃣5️⃣ How many connection models are there in driver-sequencer connections?

In a recent interview, I was asked whether an Analysis Port can be used instead of a TLM Port in UVM. It's an interesting question, so let's break it down!

🚀 Key Differences:
✅ TLM Ports (uvm_tlm_*_port) → Used for direct communication (one-to-one), allowing request-response mechanisms like put(), get(), and transport().
✅ Analysis Ports (uvm_analysis_port) → Used for broadcasting transactions (one-to-many), typically in monitors, scoreboards, and coverage collectors.

🔍 Why Analysis Port CANNOT Replace TLM Port:
❌ No Response Handling: Unlike TLM ports, analysis ports support only write(), meaning they can send data but can't receive responses.
❌ One-to-Many Broadcast: Analysis ports are designed for broadcasting, while TLM ports ensure one-to-one communication, crucial for driver-sequencer interactions.
❌ Limited Use Cases: Analysis ports are ideal for functional coverage and checking but cannot drive DUT stimulus like a sequencer-driver connection.
🔥 Conclusion: Analysis Ports are powerful for broadcasting transactions but cannot replace TLM ports where direct, bidirectional communication is needed. Choose the right port based on the use case!
