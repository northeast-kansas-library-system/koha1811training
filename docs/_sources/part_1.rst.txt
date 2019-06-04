Koha 18.11 Trainng Part 1
=========================

**Koha homepage**
-----------------

*Patron notes on staff dashboard*
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

In Koha 17.05 we added a feature that allows patrons put a note or a comment on an item they have checked out - something along the lines of "When I got this home I realized that there were pages missing" etc.  One of the complaints we had about this feature was that there was no built in mechanism to inform staff that one of these notes had been placed.

In an attempt to fix this problem, when a patron leaves a note on an item they have checked out, those notes will appear on the homepage in the staff client:

  .. image:: /screenshots/0010.jpg

While this table is a good step in the right direction, the problem we will have is that nothing on the table indicates where the item was checked out or which library owns the item:

  .. image:: /screenshots/0020.jpg

----------------------------------------

**Cataloging**
--------------

*Z39.50*
^^^^^^^^
-  Focus on ISBN field

  Currently when you open a Z39.50 search window, the first thing you have to do is to put the cursor into an input field before you can start searching.  With the update, the cursor will automatically start in the ISBN field when the Z39.50 window opens.

    .. image:: /screenshots/0030.jpg

-  Additional columns in Z39.50 results

  We can now configure the interface to show additional Marc fields on the results page when doing a Z39.50 search:

    .. image:: /screenshots/0040.jpg

  (The cataloging committee will ultimately decide which fields shall be displayed here.  For the purposes of this demonstration we've added 245$h, 300$a, and 264$a,$b,$c)

*Add item reversion*
^^^^^^^^^^^^^^^^^^^^
There is a reversion on the Add/Edit items page.  I have been told that this change is in preperation for some changes coming soon to the cataloging interface.

  .. image:: /screenshots/0050.jpg

*Cataloging add record problem*
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
There is also a change on the Add/Edit record page.  Again, we've been told that this change is in preperation for some future changes coming soon to the cataloging interface.

  .. image:: /screenshots/0060.jpg

----------------------------------------

**Circulation**
---------------

*Collection code in checkout table*
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
Collection codes will not appear on the check-out table when checking out items to patrons:

  .. image:: /screenshots/0070.jpg

*Circulation history - click barcode goes to item record*
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
When you click on a patron's circulation history, you will now be able to click on the item barcode number to go straight to the item record rather than having to go to the bibliographic record and then search for the item barcode number.

  .. image:: /screenshots/0080.jpg

*Patron information in left column is now hidden*
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
A patron's contact information will no longer appear in the column on the left hand side of the page.

  - Before:

    .. image:: /screenshots/0090.jpg

  - After:

    .. image:: /screenshots/0100.jpg

  - Patron's contact information will still appear on the patron's "Details" page:

    .. image:: /screenshots/0110.jpg
