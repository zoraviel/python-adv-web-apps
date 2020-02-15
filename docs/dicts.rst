Dictionaries
============

This section is based on chapter 5 in Sweigart’s `Automate the Boring Stuff with Python <https://automatetheboringstuff.com/>`_ (second edition).

`Python scripts for this section <https://github.com/macloo/python-adv-web-apps/tree/master/python_code_examples/dictionaries>`_

Introduction to dictionaries
----------------------------

The crucial concept to understand is that a **dictionary** consists of *key-value pairs*. ::

    { "Title": "Harry Potter and the Goblet of Fire", "Author": "J. K. Rowling", "Year": 2001 }

The **keys** in that dictionary are ``"Title"``, ``"Author"`` and ``"Year"``.

The **values** in that dictionary are ``"Harry Potter and the Goblet of Fire"``, ``"J. K. Rowling"`` and ``2001``.

Different from a **list**, a dictionary does not have indexes. You can’t depend on the *order* of items in a dictionary to stay the same. You cannot insert a new item into a particular position in a dictionary because the items do not have positions, or places. Thus we refer to **lists** as *ordered* and to dictionaries as *unordered*.

Although Sweigart refers to the keys as *indexes,* you shouldn't think of them behaving exactly as indexes do in lists.

The following ways to loop through a dictionary are demonstrated in the file `looping_keys_values.py <../python_code_examples/dictionaries/looping_keys_values.py>`_.

* ``for k in dict.keys():``
* ``for v in dict.values():``
* ``for k, v in dict.items():``

Naturally, your dictionary likely will not be named ``dict``.

Sweigart does an excellent job of explaining dictionaries in chapter 5.

Converting a CSV to a dictionary
--------------------------------

You can use Python's ``csv`` module and the ``DictReader()`` method to create a dictionary of dictionaries or a list of dictionaries from a CSV file. See *dictreader_example.py* in this folder.

Writing a dictionary into a CSV file
------------------------------------

xyz

Examples of complex dictionaries
--------------------------------

A list of dictionaries
++++++++++++++++++++++

In this data structure, several or many dictionaries are items in a Python list.

All the dictionaries contain the same keys. ::

    presidents_list = [
    {"Presidency":1,"President":"George Washington","Wikipedia_entry":"http://en.wikipedia.org/wiki/George_Washington","Took_office":"4/30/1789","Left_office":"3/4/1797","Party":"Independent ","Home_state":"Virginia","Occupation":"Planter","College":"None","Age_when_took_office":57,"Birth_date":"2/22/1732","Birthplace":"Westmoreland County, Virginia","Death_date":"12/14/1799","Location_death":"Mount Vernon, Virginia"},
    {"Presidency":2,"President":"John Adams","Wikipedia_entry":"http://en.wikipedia.org/wiki/John_Adams","Took_office":"3/4/1797","Left_office":"3/4/1801","Party":"Federalist ","Home_state":"Massachusetts","Occupation":"Lawyer","College":"Harvard","Age_when_took_office":61,"Birth_date":"10/30/1735","Birthplace":"Quincy, Massachusetts","Death_date":"7/4/1826","Location_death":"Quincy, Massachusetts"},
    {"Presidency":3,"President":"Thomas Jefferson","Wikipedia_entry":"http://en.wikipedia.org/wiki/Thomas_Jefferson","Took_office":"3/4/1801","Left_office":"3/4/1809","Party":"Democratic-Republican ","Home_state":"Virginia","Occupation":"Planter, Lawyer","College":"William and Mary","Age_when_took_office":57,"Birth_date":"4/13/1743","Birthplace":"Albemarle County, Virginia","Death_date":"7/4/1826","Location_death":"Albemarle County, Virginia"},
    {"Presidency":4,"President":"James Madison","Wikipedia_entry":"http://en.wikipedia.org/wiki/James_Madison","Took_office":"3/4/1809","Left_office":"3/4/1817","Party":"Democratic-Republican ","Home_state":"Virginia","Occupation":"Lawyer","College":"Princeton","Age_when_took_office":57,"Birth_date":"3/16/1751","Birthplace":"Port Conway, Virginia","Death_date":"6/28/1836","Location_death":"Orange County, Virginia"},
    {"Presidency":5,"President":"James Monroe","Wikipedia_entry":"http://en.wikipedia.org/wiki/James_Monroe","Took_office":"3/4/1817","Left_office":"3/4/1825","Party":"Democratic-Republican ","Home_state":"Virginia","Occupation":"Lawyer","College":"William and Mary","Age_when_took_office":58,"Birth_date":"4/28/1758","Birthplace":"Westmoreland County, Virginia","Death_date":"7/4/1831","Location_death":"New York, New York"}
    ]


A dictionary of dictionaries
++++++++++++++++++++++++++++

All dictionaries contain an identifying **key** (in this case, the name of a president) and a **value** that is itself a dictionary, containing the same keys as all the others. Note where the curly braces are used. ::

    presidents_dict = {
    { "George Washington": {"Presidency":1,"Wikipedia_entry":"http://en.wikipedia.org/wiki/George_Washington","Took_office":"4/30/1789","Left_office":"3/4/1797","Party":"Independent ","Home_state":"Virginia","Occupation":"Planter","College":"None","Age_when_took_office":57,"Birth_date":"2/22/1732","Birthplace":"Westmoreland County, Virginia","Death_date":"12/14/1799","Location_death":"Mount Vernon, Virginia"} },
    { "John Adams": {"Presidency":2,"Wikipedia_entry":"http://en.wikipedia.org/wiki/John_Adams","Took_office":"3/4/1797","Left_office":"3/4/1801","Party":"Federalist ","Home_state":"Massachusetts","Occupation":"Lawyer","College":"Harvard","Age_when_took_office":61,"Birth_date":"10/30/1735","Birthplace":"Quincy, Massachusetts","Death_date":"7/4/1826","Location_death":"Quincy, Massachusetts"} },
    { "Thomas Jefferson": {"Presidency":3,"Wikipedia_entry":"http://en.wikipedia.org/wiki/Thomas_Jefferson","Took_office":"3/4/1801","Left_office":"3/4/1809","Party":"Democratic-Republican ","Home_state":"Virginia","Occupation":"Planter, Lawyer","College":"William and Mary","Age_when_took_office":57,"Birth_date":"4/13/1743","Birthplace":"Albemarle County, Virginia","Death_date":"7/4/1826","Location_death":"Albemarle County, Virginia"} },
    { "James Madison": {"Presidency":4,"Wikipedia_entry":"http://en.wikipedia.org/wiki/James_Madison","Took_office":"3/4/1809","Left_office":"3/4/1817","Party":"Democratic-Republican ","Home_state":"Virginia","Occupation":"Lawyer","College":"Princeton","Age_when_took_office":57,"Birth_date":"3/16/1751","Birthplace":"Port Conway, Virginia","Death_date":"6/28/1836","Location_death":"Orange County, Virginia"} },
    { "James Monroe": {"Presidency":5,"Wikipedia_entry":"http://en.wikipedia.org/wiki/James_Monroe","Took_office":"3/4/1817","Left_office":"3/4/1825","Party":"Democratic-Republican ","Home_state":"Virginia","Occupation":"Lawyer","College":"William and Mary","Age_when_took_office":58,"Birth_date":"4/28/1758","Birthplace":"Westmoreland County, Virginia","Death_date":"7/4/1831","Location_death":"New York, New York"} },
    }

Chapter review: chapter 5
-------------------------

Key points
++++++++++

1. Differences between lists and dictionaries
2. Take care with use of quotes when both keys and values are strings
3. How to loop through keys, values, or both at once
4. Use ``list( dict.keys() )`` to get a list of all keys in a dictionary
5. Check for presence of a key or a value with ``in`` or ``not in``
6. Provide a default value (here, 0) in case a key is not present: ``dict.get(key, 0)``
7. Use ``dict.setdefault(key, value)`` to set a new key but prevent overwriting an existing value if the key is already present
8. Use ``import pprint`` if you need to print out a large dictionary's contents in the Terminal

We stop on page 112, “Using Data Structures to Model Real-World Things.” On page 117, Sweigart starts to discuss “dictionaries and lists that contain other dictionaries and lists,” also known as **nested dictionaries**. It's a rather brief discussion and not tremendously helpful.




.