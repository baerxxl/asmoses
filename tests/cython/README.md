
HOWTO run these tests by hand:
------------------------------

You need to set up the PYTHON path:
export PYTHONPATH=build/moses/cython

You also need to specify the library path:
export LD_LIBRARY_PATH=build/moses/cython/opencog

Then, from the project root directory:

nosetests -vs tests/cython/moses/


If you modify the cython bindings, you may need to manually remove
some build files to get a clean rebuild.  Basically, the CMakefiles
for cython/python are buggy, and fail to rebuild when changes are made.
So, for example:

rm build/moses/cython/opencog/pyasmoses.cpp
