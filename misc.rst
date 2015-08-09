========================================
Misc
========================================

Accessing attribute by string
========================================

somebody may come up with :

.. code-block:: python

    result = eval('myclass.{}()'.format(name))


better :

.. code-block:: python

    result = getattr('myclass', name)()
