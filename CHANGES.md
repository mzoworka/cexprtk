#Change Log

## 0.4.0
### New Features

  * A new method is provided on the `cexprtk.Expression` class, `results()`, which returns a Python list containing floating point values (scalars), string values (strings), or lists of floating point values (vectors).
  * Added support to the symbol table for string variables (accessed through the `.string_variables` property).


##0.3.4 (2019-12-8)
### Changed

  * Updated exprtk version current on 2019-12-7.
  * Rebuilt `.cpp` files in distribution using cython 0.29.14
  * Changed to pytest rather than nosetests for testing.
  * Updated tox to run tests for cases when cython is and isn't present.

### Bug-Fixes

  * Fixed deprecation warnings being raised by the inspect module under python 3.x.


##0.3.3 (2018-07-04)
### Bug-Fixes

  * Added missing file to MANIFEST.in (`cython/cexprtk_custom_vararg_function.pxd`) this had been causing an error under python 3.7 when trying to register custom functions.
  * Fixed bug with cexprtk.check_expression() so that it works more like that in version 0.2.0. This function isn't particularly useful in this form with the introduction of custom functions and should be deprecated in version 0.4.0.

### Changed
  * Rebuilt `.cpp` files in distribution using cython 0.28.3.

##0.3.2 (2017-12-10)
### Bug-Fixes

 * Changes to setup.py so that the correct README is displayed on PyPI
 * Updated the exprtk_benchmark.py file so that it can run under python 3.

##0.3.1 (2017-11-28)
### Bug-Fixes

* Bug fixes to `setup.py` to allow building on Linux using gcc.
* Build scripts to assist making wheels on Linux, Windows and MacOSX

##0.3.0 (2017-11-27)
### New Features

* Support for Python 3
* Custom python functions can now be registered with `Symbol_Table` and used in expressions.

##0.2.1 (2017-08-03): 
### New Features

* Updated version of bundled `exprtk` to that current as of 3rd August 2017.
* Updated `cexprtk` wrapper code to be compatible with this version of `exprtk`.
* Enabled pickling of the `Expression` and `Symbol_Table` classes. Primarily this is to allow their use with the multiprocessing module.


##0.2.0
###New Features

* Allows re-use of parsed mathematical expressions through new classes:
    - `Expression`
    - `Symbol_Table`
* Expose support for unknown symbol resolver through the `unknown_symbol_resolver_callback` argument to the `Expression` constructor.
* Improved documentation:
    - API reference.
    - Examples of the new classes.
* Updated version of `exprtk` bundled in `3rdparty`

##0.1.2 (not released to pypi)
### Bug-Fixes

* Modifications to allow `cexprtk` to build on windows.

##0.1.1 (2013-12-30)
### Bug-Fixes

* Module would not build if cython installed. 
* Now build from pre-cythonized `cexprtk.cpp` whether `cython` available or not.

##0.1.0 (2013-12-30)

* Initial Release
