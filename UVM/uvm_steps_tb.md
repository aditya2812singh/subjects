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
