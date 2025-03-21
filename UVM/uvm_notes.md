### Question to Cover:BASIC

[1] Concept of virtual interface and how it can connect DUT with an Verification Env. What is a Test harness.

[2] How virtual interface flow in a testbench and ultimately reach driver to interact with DUT.

[3] Basic phasing mechanism like build, connect, run, etc (ignore run time phase initially)

[4] Concept of run_test() in top module and why it is needed.

[5] Clock generation module in top module and flow of uvm config.

[6] Difference between uvm_object and uvm_component. Classification of uvm_object.

[7] TLM interconnection in UVM. Role of producer and consumer. Concept of pull port and pull import.** **

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
