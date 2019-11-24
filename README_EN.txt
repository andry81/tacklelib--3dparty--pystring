* README_EN.txt
* 2019.11.24
* pystring

1. DESCRIPTION
2. LICENSE
3. REPOSITORIES
4. INSTALLATION
5. AUTHOR EMAIL

-------------------------------------------------------------------------------
1. DESCRIPTION
-------------------------------------------------------------------------------
pystring patched sources fork from: https://github.com/imageworks/pystring

Based on version: 2019.03.21 <4af4a865208b400b9cd5ae71b0e162a6baf331f9>

Partially refactored to be used with std::basic_string template class instead of
single std::string.

From authors:

  Pystring is a collection of C++ functions which match the interface and
  behavior of python's string class methods using std::string. Implemented in
  C++, it does not require or make use of a python interpreter. It provides
  convenience and familiarity for common string operations not included in the
  standard C++ library. It's also useful in environments where both C++ and
  python are used.

  Overlapping functionality (such as index and slice/substr) of std::string is
  included to match python interfaces.

  Originally developed at Sony Pictures Imageworks.
  http://opensource.imageworks.com/

The original library patched to fix these issues:

1. Use std::basic_string instead of single std::string (unable to use functions
   in unicode contexts because of what reason).

2. Compilation warnings in the Microsoft Visual Studio 2015 Update 3.

Cmake scripts uses the cmake modules from the tacklelib library:

https://svn.code.sf.net/p/tacklelib/cmake/trunk

-------------------------------------------------------------------------------
2. LICENSE
-------------------------------------------------------------------------------
Copyright (c) 2008-2010, Sony Pictures Imageworks Inc
(see included text file "LICENSE" or
https://github.com/imageworks/pystring/blob/master/LICENSE)

-------------------------------------------------------------------------------
3. REPOSITORIES
-------------------------------------------------------------------------------
Primary:
  * https://sf.net/p/tacklelib/3dparty--pystring/HEAD/tree/trunk
    https://svn.code.sf.net/p/tacklelib/3dparty--pystring/trunk
First mirror:
  * https://github.com/andry81/tacklelib--3dparty--pystring/tree/trunk
    https://github.com/andry81/tacklelib--3dparty--pystring.git
Second mirror:
  * https://bitbucket.org/andry81/tacklelib-3dparty-pystring/src/trunk
    https://bitbucket.org/andry81/tacklelib-3dparty-pystring.git

-------------------------------------------------------------------------------
4. INSTALLATION
-------------------------------------------------------------------------------
N/A

-------------------------------------------------------------------------------
5. AUTHOR EMAIL
-------------------------------------------------------------------------------
Andrey Dibrov (andry at inbox dot ru)
