RMarshal
========

RMarshal is a Ruby gem to enable the reading of data in the Python marshal format.  
It also contains support for reading `.pyc` files, including disassembly of the bytecode.

Installation
------------

To install from the gem:

	gem install rmarshal

It has no outside dependencies.

Use
---

To unmarshal some data from a file:

	require 'rmarshal'
	
	fp = File.open 'somefile.marshalled'
	data = unmarshal fp

To load a `.pyc` file and dump the code object with disassembly:

	require 'rmarshal'
	
	code = pyc 'test.pyc'
	pp code, code.disassemble

Bugs
----

- `TYPE_LONG` is currently unsupported.

Todo
----

- Add support for outputting in marshal format.
- Add RDoc documentation.
- Add real unit tests.
- Test `TYPE_FLOAT` and `TYPE_COMPLEX`.
