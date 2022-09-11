### Hi there 👋

<!--
**venus-revisioner/venus-revisioner** is a ✨ _special_ ✨ repository because its `README.md` (this file) appears on your GitHub profile.

Here are some ideas to get you started:

- 🔭 I’m currently working on ...
- 🌱 I’m currently learning ...
- 👯 I’m looking to collaborate on ...
- 🤔 I’m looking for help with ...
- 💬 Ask me about ...
- 📫 How to reach me: ...
- 😄 Pronouns: ...
- ⚡ Fun fact: ...
-->


# overhead-0.6.0

My _overhead_ tools of mixed-bag-distribution, self-organized, self-build.
Used in many many projects as helper packages, functions and Classes.

### __installing (notes to myself):__

----------------------------------
# TL;DR #
#### make this into a script?
>PREREQ:
> 
>##### pip install twine, pipreqs

pipreqs --mode gt

        (-- mode gt means >= current package)

pip install .

pip install --upgrade .

python setup.py check

python setup.py sdist
#####
- _choose wheel or also tar.ball_
>####  pip install wheel
>#### python setup.py bdist_wheel --universal
- _both go under dist/ directory_

python setup.py bdist_wheel --universal

twine upload --repository-url https://test.pypi.org/legacy/ dist/*

username & password? __token__ under &HOME/.pypirc

# test:
pip install --index-url https://test.pypi.org/simple/ pyexample --user

## troubleshooting:
>  download tarball without install:
> 
>  pip download pyexample

>  or just the package without dependencies:
> 
>  pip download --no-deps myexample

###
### https://betterscientificsoftware.github.io/python-for-hpc/tutorials/python-pypi-packaging/
###

pipreqs --mode gt ( >=current package )

  pip install .

  pip install --upgrade .

## Source distribution: ##
This file is your source distribution containing a compressed archive of the package.
If it does not automatically contain what you want, then you might consider using a MANIFEST file.

python setup.py check

python setup.py sdist

(creates a dist/ diredtory with .tar.gz file.)

# Creating a wheel distribution: #
(pip install wheel)

python setup.py bdist_wheel --universal (python2 & python3 compatible)

(python setup.py bdist_wheel) (optionally)

  -> under dist/ directory


##  PyPI Test ##

pip install twine

only tar:
twine upload --repository-url https://test.pypi.org/legacy/ dist/my-0.1.0.tar.gz

both:
twine upload --repository-url https://test.pypi.org/legacy/ dist/*

username & password? __token__ under &HOME/.pypirc

now you can test-download your package!

pip install --index-url https://test.pypi.org/simple/ pyexample --user


### IF READY TO PUBLISH ###

upload:  twine upload dist/*

install: pip install mypackage --user

download tarball without install:

pip download pyexample

or just the package without dependencies:

pip download --no-deps myexample
