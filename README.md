This is tolua++-1.1

Lua Version: 5.4


* What is tolua++?

  tolua++ is an extension of toLua, a tool to integrate C/C++ code with
  Lua. tolua++ includes new features oriented to c++, such as class
  templates.

  tolua is a tool that greatly simplifies the integration of C/C++ code 
  with Lua. Based on a "cleaned" header file, tolua automatically generates 
  the binding code to access C/C++ features from Lua. Using Lua-5.0 API and
  metamethod facilities, the current version automatically maps C/C++ 
  constants, external variables, functions, namespace, classes, and methods 
  to Lua. It also provides facilities to create Lua modules.

* Availability

  tolua++ is freely available for both academic and commercial purposes.
  See COPYRIGHT for details.

* Installation

```

mkdir build && cmake .. && make && make install

```


* Contacting the author
  tolua has been designed and implemented by Waldemar Celes and later was maintained by Ariel Manzur.
  Currently this tolua++ repository is maintained by dakwak.

  Send your comments, bug reports and anything else to 
  tolua@dakwak.com
