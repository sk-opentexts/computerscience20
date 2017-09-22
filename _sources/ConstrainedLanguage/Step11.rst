Step 11: If/Else
=================

Tutorial
---------

While learning how to program is fun, you should not spend all your
time in front of the computer. When you are at home, ``if`` it rains, keep reading, otherwise, go outside and play!

Two choices...
--------------

Let's rewrite the sentence that starts with ``if`` above::

    if it rains,
        keep reading,
    otherwise,
        go outside and play

If this were Python, we might have written it like this instead:

.. code-block:: python

    if it_rains():
        keep_reading()
    else:
        go_outside_and_play()

Yes, Python includes the possibility of more than one choice with
the keyword ``else``. Let's use it with another example. Reeborg can see
if there's a wall right in front him, using the function ``front_is_clear()``. This can be used with ``if/else`` to write a program that will guide Reeborg around a rectangular world. Something like the following should do the trick:

.. code-block:: python

    def move_or_turn():
        if front_is_clear():
            # something
        else:
            # something else

    repeat 40:
        move_or_turn()


Your Turn
---------

Open Step 11 on the `Reeborg website <http://wmcicompsci.ca/reeborg>`_ .

.. image:: images/step11.png

Reeborg wants to make some bouquets of flowers for it's friends, Zoe and Eli. Reeborg has permission to ``take()`` tulips from some of his neighbor's gardens. Unfortunately for Reeborg, each of the gardens is different. Reeborg does know that the garden will be rectangular, that it will take 23 steps to get around the garden, and that there will be a tulip in each corner of the garden. 

Create a program to have Reeborg walk around the outside of the garden, picking up a tulip if it can, and moving ahead if it cannot. You **must** use a ``repeat 23:`` and ``if/else``.


If You're Having Trouble (a more detailed explanation)
------------------------------------------------------

We have seen how ``def``\ s and ``if`` statements could be thought
of as being (sometimes) equivalent to inserting a code block; the
exception was when the condition of the ``if`` statement was ``False``,
in which case we ignored the code block which is equivalent to deleting
it. ``if/else`` statements can be thought as inserting one or the other
code block. Thus

.. code-block:: python

    move()
    if True:
        turn_right()
    else:
        turn_left()
    move()

is equivalent to

.. code-block:: python

    move()
    turn_right()
    move()

whereas

.. code-block:: python

    move()
    if False:
        turn_right()
    else:
        turn_left()
    move()

is equivalent to

.. code-block:: python

    move()
    turn_left()
    move()

We can represent this as a flowchart:

.. figure:: images/flowcharts/else.jpg
   :align: center