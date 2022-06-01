madaf
~~~~~

A superfast key-value database in development.

.. code:: sh

    pip install madaf

It works like a dictionary, except everything gets stored to disk and the database size can vastly exceed system memory.

.. code:: python

    from madaf import Madaf

    db = Madaf("/tmp/mydb")
    db["some_key"] = "some_value"
    db["blah_blah"] = {"hello": "world", "foo": True}
    print(db["some_key"])
    print(db["blah_blah"])
    del db["some_key"]
    print(db["some_key"]) # throws KeyError

You can think of madaf as a faster and more efficent shelve package.