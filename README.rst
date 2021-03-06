=============
ckanext-cob_theme
=============

.. Put a description of your extension here:
   What does it do? What features does it have?
   Consider including some screenshots or embedding a video!


------------
Requirements
------------

Compatible with CKAN 2.3+

Install the ckanext-showcase extension


------------
Development Installation
------------

To install ckanext-cob_theme:

1. Activate your CKAN virtual environment, for example::

     . /usr/lib/ckan/default/bin/activate

2. Download the ckanext-cob_theme github repository::

     cd /usr/lib/ckan/default/src
     git clone https://github.com/Ontodia/ckanext-cob_theme.git

3. Install the extension into your virtual environment::

     cd ckanext-cob_theme
     python setup.py develop

4. Add ``cob_theme`` to the ``ckan.plugins`` setting in your CKAN
   config file (by default the config file is located at
   ``/etc/ckan/default/production.ini``).

5. Restart CKAN. For example if you've deployed CKAN with Apache on Ubuntu::

     sudo service apache2 reload


---------------
Config Settings
---------------

Document any optional config settings here. For example::

    # The minimum number of hours to wait before re-checking a resource
    # (optional, default: 24).
    ckanext.cob_theme.some_setting = some_default_value

-----------------
API Documentation
-----------------

To install API Documentation:

1. Install Sphinx and Alabaster theme on your virtual environement::
     sudo apt-get install python-sphinx
     pip install -e git+https://github.com/bitprophet/alabaster/#egg=alabaster

2. Run the doc generate python script and sphinx build command to create static html files::
     cd ckanext-cob_theme/docs/
     python generate.py ../../ckan/doc
     cp conf.py ./doc
     sphinx-build -b html ./doc ../ckanext/cob_theme/templates/docs/snippets

3. Use the doc-template file to add the header and footer to all the static html files::
     cd ../ckanext/cob_theme/templates/docs/snippets
     mkdir -p __static/docs
     mv _static __static/docs
     mv __static _static
