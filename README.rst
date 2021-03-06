OPDS generator
##############

This is a simple OPDS generator in python.
Here is an exemple of usage

.. code-block:: python

    from opds_generator import Catalog

    catalog = Catalog(title=title, **options)
    catalog.add_entry(
      uuid='91883979-5cd8-48a4-9dfb-2821425cd186',
      title='Welcome to Europe refugees website'
      issued=datetime.datetime(2010, 1, 10),
      updated=datetime.datetime(2016, 6, 23),
      languages=('en', 'fr')
      urls={'application/zip+html': 'http://filer.bsf-intranet.org/w2eu/w2eu.zip'},
      file_size='112722208',
      checksum='a3d3738d3d53922b3571ba772c0aea7794687cc263c28627cdff8c214967ded4')

    return to_opds(catalog, url)

How do I install?
=================

Currently this code is not released on PyPI, please clone this repository.

::

  $ git clone https://github.com/almet/opds-generator.py.git
  $ virtualenv venv
  $ venv/bin/pip install -e .
