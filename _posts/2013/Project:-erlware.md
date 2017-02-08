* Website: http://www.erlware.org/
* Responsible: Jordan Wilberding, Eric Merritt
* If you have any questions, send an e-mail to beam-community@googlegroups.com

### Idea #1: Modern Erlang Package Manager

Brief explanation: A proper package manager solution for Erlang.
* Please see the following for full details: http://hyperthunk.wordpress.com/2012/05/28/does-erlangotp-need-a-new-package-management-solution/

Expected results: 
* we need/want a dependency manager, not a package manager
* complete functionality available from the command line (pipeable/scriptable)
* there is also a complete Erlang API for everything (with no assumptions about the runtime environment) so that tools integration is easy
* packages need to be identified by name, version and publisher (e.g., basho/rebar-1.0 is not the same as hyperthunk/rebar-1.0)
* multiple versions of packages (plus maybe multiple originators) may exist within a local machine so….
 * the plain OTP lib_dir thing isn’t going to work (just having basho/rebar-1.0 and hyperthunk/rebar-1.0 installed isn’t viable), and
 * reltool isn’t going to like this or provide a decent way of handling it
* so we need some kind of custom local repository
 * that understands publisher as an additional concept
 * with a means of getting the right code path set up for any given task
* storing package meta-data indexes in git is smart and easy
 * one git repository per publisher/organisation is best, supporting index meta-data for any package they’re publishing
 * users simply white-list publishers/organisations and get access to all their packages thereafter
 * creating your own index (of packages) is easy and secure (via your github repository access control settings)
* we prefer pushing built, binary artefacts rather than having the index(es) point to source code only repositories
* the binary (+ mandatory stuff like includes and/or optional things like source code) artefacts should probably be bundled as .ez files
* published binary (.ez) artefacts can and should just live inside the index, but pulling the index should not mean pulling the whole remote repo
 * you never actually clone the whole repository unless you’re the publisher who owns and is working on and publishing to  it
 * the master branch is generally empty and contains only a README for the benefit of github browsing
 * the index itself lives in a special ‘index’ branch and nothing but index metadata ever goes in here
 * when a binary artefact is added, it is put on a new branch and tagged – all the index metadata is deleted from the branch/tag so only the artefact remains
 * when pulling the index or a specific artefact that has been located by examining a local copy of the index, you fetch only that specific subset of the repository, by using git’s fetch-pack instruction set

Knowledge prerequisites: 
* A general understanding of Erlang and OTP is required

Mentors: 
* Jordan Wilberding (jwilberding@gmail.com)
* Eric Merritt (ericbmerritt@gmail.com)