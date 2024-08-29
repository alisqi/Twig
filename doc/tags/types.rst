``types``
=========

The ``types`` tag declares the types for template variables.

To do this, specify a :ref:`mapping <twig-expressions>` of names to their types as strings. 

Here is how you declare that variable ``foo`` is a boolean, while ``bar`` is an integer (see note below):

.. code-block:: twig

    {% types {
        foo: 'bool',
        bar: 'int',
    } %}

You can declare variables as optional by adding the '?' suffix:

.. code-block:: twig

    {% types {
        foo: 'bool',
        bar?: 'int',
    } %}

By default, this tag does not affect the template compilation or runtime behavior.

Its purpose is to enable designers and developers to document and specify the context's available
and/or required variables. While Twig itself does not validate variables or their types, this tag enables extensions
to do this.

Additionally, :ref:`Twig extensions <creating_extensions>` can analyze these tags to perform compile-time and
runtime analysis of templates in order to increase code quality.

.. note::

    The syntax for and contents of type strings are intentionally left out of scope. 
    
