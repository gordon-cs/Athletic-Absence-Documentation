Some topics probably need their own documents:
Install and setup: How to get your system installed and working on a new machine (real or virtual).  (It would be wise to document this early, while you remember clearly what you did.  Even better, test your documentation by setting up a second system, and use it for testing.)
Testing: How to test all parts of your system.  This is how they’ll know if the install worked, and if changes broke something.  (Don’t wait until this is due to write the tests.  You should write them as you go, so they can help you keep your code working.  The deadline is just for documenting how to use them.)

And some topics should be covered at the top level in the Design Document, which should have links to whatever more detailed documentation is needed to cover the topic:
Server API: Clearly document each call, it’s arguments, and its response.
Database Schema: Be sure structure and purpose are clear.
Code and class guide: Overview and roadmap of the class and directory structure.  

Clearly, some documentation belongs completely in the code: 
File/Class comments: every file or class needs a good top-level comment.

Finally, this is all built on clear and correct code.  So the code itself is the ground that is described and mapped by the rest of the documentation.
