.. image:: https://travis-ci.org/GregHilmes/pokebase.svg?branch=master
   :target: https://travis-ci.org/GregHilmes/pokebase

******
README
******

pokebase is a simple but powerful Python interface to the `PokéAPI database <https://pokeapi.co/>`_

============
Installation
============

``pip install pokebase``

It can't get much easier than that.

=====
Usage
=====

  >>> import pokebase as pb
  >>> chesto = pb.NamedAPIResource('berry', 'chesto')
  >>> chesto.name
  'chesto'
  >>> chesto.natural_gift_type.name
  'water'
  >>> chesto = pb.berry('chesto')  # direct lookup.
  >>> chesto.name
  'chesto'
  >>>

... And it's just that simple.

===============
Version Support
===============

pokebase currently (officially) supports Python 2.7 and 3.6 versions.

=======
Testing
=======

Python unittests are in a separate ``tests`` directory, and can be run via ``python -m tests.test_pokebase``.


Important
---------

The quick data lookup for a Pokémon type, is ``pokebase.type_('type-name')``, not ``pokebase.type('type-name')``. This is because of a naming conflict with the Python language.
