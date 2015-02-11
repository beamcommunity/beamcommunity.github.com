* Responsible: Erlang Solutions Ltd
* If you have any questions, send an e-mail to beam-community@googlegroups.com

### Project: Work Stealing Scheduling on the Parallella

Brief explanation:

The Parallella is a board with a dual-core ARM processor and 16 or 64 Epiphany cores, developed by Adapteva to be highly energy efficient. The Epiphany cores were designed to execute parallel programs with high performance.

Somewhat ironically, programming parallel programs on the Parallella is an arduous task due to having to program the Epiphany cores individually and at a low level of abstraction.

A concurrent model based on Cilk was developed in order to alleviate the task of writing parallel programs on the Parallella. Initially, a work stealing scheduler was implemented for run of the mill x86 multi core machines in order to ensure that the scheduler worked as expected and delivered high performance.

The aim of this project is to utilise the Epiphany cores to get more performance for the Erlang application running on the ARM cores.

Writing an Erlang VM that runs on the Epiphany cores is deemed to be too big a problem to deal with right now.

The Cilk scheduler is good at executing short-lived, non-blocking threads/processes, so the Erlang code shall be analysed to determine which parts of it fit the Cilk model and shall be translated to something that can run on the Epiphany cores.

Expected results:

* Port of a Cilk-based work stealing scheduler to the Parallella, with unit tests demonstrating that the functionality works as expected.
* Analysis tool that can identify Erlang code eligible for Cilk offloading.
* Translate eligible Erlang code to Cilk code.

Stretch goals:

* Examples of usage of the basic primitives of the scheduler in order to write parallel programs on the Parallella (stretch goal).
* Outline of how to modify the Erlang compiler and scheduler to take the offloading analysis into account (stretch goal).


Knowledge prerequisites:

The student is expected to have some familiarity with concurrent abstractions (spawn / send / receive) and an advanced understanding of the C programming language.

Mentors: Luca Favatella / Edward Tate