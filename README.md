### Hi there 👋

**venus-revisioner/venus-revisioner** is a ✨ _special_ ✨ repository because its `README.md` (this file) appears on your GitHub profile.

Here are some ideas to get you started:

- 🔭 I’m currently working on ... nothing interesting, AI, art, philosophy, mathematics...
- 🌱 I’m currently learning ... nothing. Except GitHub which I feel like a toddler again!
- 👯 I’m looking to collaborate on ... well, extrating meaningful large-scale forms from time series with fft in order to make
                                a plausible model for cross-modality for future reference for AI research. And ofc would you build singularity with me?
- 🤔 I’m looking for help with ... everything. Can you wash my clothes?
- 💬 Ask me about ... if I'd like to talk with you in haikus for the whole day?
- 📫 How to reach me: ... I'm hard to reach even with a phone number!
- 😄 Pronouns: ... me? 
- ⚡ Fun fact: ... I stoned a brand new Mercedes-Benz when I was 7-8 yo. I was just fascinated of the parabolic trajectores the stones made especially when bouncing off the neighboring cars. I didn't realize its not ok to do so.
 HELP ME!






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
