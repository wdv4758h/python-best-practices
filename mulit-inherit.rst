Multiple Inheritance
===============================================================================

.. highlight:: python


Invoking All Parents' Constructor
----------------------------------------------------------------------

``super`` is your friend. Forget the old style usage (``klass.__init__``).

::

    class M:
        def __init__(self):
            print('init M')
            super(M, self).__init__()

    class N:
        def __init__(self):
            print('init N')
            super(N, self).__init__()

    class Base:
        def __init__(self):
            print('init base')
            super(Base, self).__init__()

    class A(Base, M, N):
        def __init__(self):
            super(A, self).__init__()
