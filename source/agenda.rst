Koha 18.11 Trainng Page
=======================

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

----------------------------------------

**Fines changes**
-----------------

*Item "Lost" twice by the same patron isn't billed the second time*
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
This cannot be shown, but this is an outline of the circumstances:
  #.  Patron checks out an item and returns it more than 45 days overdue and is billed for the item
  #.  Patron returns the item and the cost of the item is refunded
  #.  Patron checks out the item again and keeps it more than 45 days overdue again
  #.  Up until now, Koha has not been able to bill the patron for the second time the item has been declared "Lost"

*Paying fines on accounts with credits*
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
Also can't be shown.  If a patron had a fee and a credit, a bug would sometimes cause additional payments to fail.

*Item home branch shows in fee table*
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
The patron's fines table will now show item home library information.

  .. image:: /screenshots/0120.jpg

*Writeoff selected*
^^^^^^^^^^^^^^^^^^^
Multiple fee lines can be written off at once with the new "Write off selected" button.

  .. image:: /screenshots/0130.jpg

*Void credits and writoffs*
^^^^^^^^^^^^^^^^^^^^^^^^^^^
It is now possible to void writeoffs and credits.  This should simplify some of the payment issues we've had as the accounts rewrite has been underway.

  .. image:: /screenshots/0140.jpg

*Email receipts for payments*
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
When a patron pays a fee or a fee is written off, AND the patron has an e-mail address, the patron will receive an e-mail receipt for the payment/writeoff.

  .. image:: /screenshots/0150.jpg

  - This is a global system setting - currently the messages cannot be configured on a library-by-library basis.

----------------------------------------

**Holds/Requests**
------------------

*BUG! - cannot place item level Requests*
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
  This is a bug and should be fixed soon.  Our tentative date for the upgrade is June 15 and I will keep an eye on this bug and ask that we not be upgraded until it is fixed.  I'm pretty confident, though, that it should be fixed by June 15 (it may actually be fixed by May 15).

*Collection code added to holds table*
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
Collection codes will be added to the holds table in a separate column:

  Before:

    .. image:: /screenshots/0160.jpg

  After:

    .. image:: /screenshots/0170.jpg

*Split holds queue*
^^^^^^^^^^^^^^^^^^^
The layout of the holds queue is going to look radically different.  It will show the holds for each library in a separate group.

  Before:

    .. image:: /screenshots/0180.jpg

  After:

    .. image:: /screenshots/0190.jpg

----------------------------------------

**OPAC**
--------

*Many CSS elements have changed - so if something looks weird or doesn't look right, be sure to let us know.  Dan and I should be able to change anything that doesn't work correctly caused by changes to the CSS.*
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

*Cart opens with one click*
^^^^^^^^^^^^^^^^^^^^^^^^^^^^
Currently you have to click twice to open the cart on the OPAC.  Only one click will be necessary after the upgrade.

  Before:

    .. image:: /screenshots/0200.gif

  After:

    .. image:: /screenshots/0210.gif


*Login modal has changed*
^^^^^^^^^^^^^^^^^^^^^^^^^
The Login window for patrons has changed.  This will look different to patrons.

  Before:

    .. image:: /screenshots/0220.jpg

  After:

    .. image:: /screenshots/0230.jpg


*Logging in during search keeps you in search*
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
Currently if a patron does a search in the OPAC before they log into their account, once they log in, they have to re-run the search.  In the new version, after logging in, the patron will be redirected to the search they were in the middle of.

  Before:

    .. image:: /screenshots/0240.gif

  After:

    .. image:: /screenshots/0250.gif

*Expanded data for branchcode and userid in pages when a user is logged in*
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
This is a behind the scenes thing, but it can make some parts of the OPAC customizable on a branch-by-branch basis

----------------------------------------

**Searching, results, and details**
-----------------------------------

*Split "Advanced search" button in Staff*
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
Beginning with Koha 18.05, in order to get to "Advanced search" you have to hover the mouse pointer over "Search" and then select "Advanced search" from the options.  With the new version, just clicking on "Search" will take you to the "Advanced search" page.

  Before:

    .. image:: /screenshots/0260.jpg

  After:

    .. image:: /screenshots/0270.jpg

*Facets for CCODE - Staff and OPAC*
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
Collection codes will be added to the search facets on the left hand side of the screen.

  Before:

    .. image:: /screenshots/0280.jpg

  After:

    .. image:: /screenshots/0290.jpg

*Cart sorting and printing*
^^^^^^^^^^^^^^^^^^^^^^^^^^^
If you sort items in the cart, you can print them in the order you sort them in.

  .. image:: /screenshots/0300.jpg

*Holdings count*
^^^^^^^^^^^^^^^^
Tab will show a holdings count.  Production 0003008201343 - test 0003012081166; test 0003008201777.

  Before:

    .. image:: /screenshots/0310.jpg

  After:

    .. image:: /screenshots/0320.jpg

*Date accessioned*
^^^^^^^^^^^^^^^^^^
Date accessioned is visible on details page - and sortable

  Before:

    .. image:: /screenshots/0330.jpg

  After:

    .. image:: /screenshots/0340.jpg

*Checkout history toolbar*
^^^^^^^^^^^^^^^^^^^^^^^^^^
An expanded toolbar will be added to the checkout history table:

  Before:

    .. image:: /screenshots/0350.jpg

  After:

    .. image:: /screenshots/0360.jpg

*526 now indexed*
^^^^^^^^^^^^^^^^^
The 526 fields are the "Study program information note" fields in the Marc record.  The most common thing we have stored in these fields are Accelerated Reader program information.  526$a = program name; 526$b = interest level; 526$c = reading level; 526$d = points.  These fields will be indexed after the upgrade which will make them easier to search.

  .. image:: /screenshots/0370.jpg

----------------------------------------

**Patrons**
-----------

*Guarantees sorted alphabetically*
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
In previous versions of Koha, guarantees would be sorted in the order they were added to the adult's account.  They will now sort alphabetically.

  .. image:: /screenshots/0380.jpg

*Renewal date on details page*
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
The date of the last time a patron's account was renewed has been added to the "Details" page.

  .. image:: /screenshots/0390.jpg

*Updated date in left column on all patrons where the information is displayed*
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
The date of the last time a patron's account was modified has been added to the information column on the left hand side of the page.

  .. image:: /screenshots/0400.jpg

----------------------------------------

**Reports**
-----------

*Create charts in Reports*
^^^^^^^^^^^^^^^^^^^^^^^^^^
Koha can now create charts from report data.  Unfortunately there is not currently a way to download the charts it creates.

  .. image:: /screenshots/0410.jpg

*Codemirror*
^^^^^^^^^^^^
Koha now has a plugin called "Codemirror" which can help those writing reports in various ways.  One example is by showing line numbers.

  .. image:: /screenshots/0420.jpg

----------------------------------------

**Tools/Administration**
------------------------

*Circulation/fines/fees rules*
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
- Notes on circulation rules
  The upgrade adds the ability to add a note to the circulation rules so that we'll be better able to track changes to circulation rules.

    .. image:: /screenshots/0430.jpg

----------------------------------------

*Inventory*
^^^^^^^^^^^^
- Items scanned out of order

  For those using the inventory tool, when you upload a list of barcodes that have been scanned, the inventory tool will now tell you if the scanned items were out of order on the shelf.

    .. image:: /screenshots/0440.jpg

- Allow skipping items with waiting holds

  This is also a new option with the inventory tool.

    .. image:: /screenshots/0450.jpg

----------------------------------------

*Label creator and Card creator*
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
- You will now be able to add descriptions to batches of labels and batches of patrons in the card creator tool

    Before:

      .. image:: /screenshots/0460.jpg

    After:

      .. image:: /screenshots/0470.jpg

    Add a name to a batch on the "Batch edit" pages

      .. image:: /screenshots/0480.jpg

- Pop-up when searching for patron in Card creator

  When you want to add a patron to a batch in the card creator tool, if you have to search by name, if you choose the wrong patron you can't go back - you have to re-start the entire search.  This bug has been fixed.

    .. image:: /screenshots/0490.jpg


- Flexibility in call number splitting rules
  This change is impossible to demonstrate today - it's going to require a ton of set up, but, basically, the current process with the label creator is that you can have it split the call numbers where the spaces occur - so that REF 823.43 SHA has "REF" "823.43" and "SHA" all on separate lines.  This new feature would allow you to customize where the splits occur.  It will, however require changing the frameworks so the 952$2 is visible and then changing the selection for the 952$2 on the items you want to create new labels for.

----------------------------------------

*Lists*
^^^^^^^^
*Sort list by date added*

  It will be possible with the new version to sort a list by the date an item was added in addition to title, author, and publication date.  The default option will now be "Date added."

    Before:

      .. image:: /screenshots/0540.jpg

    After:

      .. image:: /screenshots/0550.jpg

    Date added will appear in the drop-down on the edit list page

      .. image:: /screenshots/0560.jpg

----------------------------------------

*Notices*
^^^^^^^^^
- Table is searchable

  A toolbar has been added to the notices table - making the notices table searchable (at long last).

    Before:

      .. image:: /screenshots/0500.jpg

    After:

      .. image:: /screenshots/0510.jpg

----------------------------------------

*Patron lists*
^^^^^^^^^^^^^^
- Share patron lists between staff

  Patron lists can now be shared among staff members with permission to view lists.

      .. image:: /screenshots/0520.jpg

----------------------------------------

*Batch item modification*
^^^^^^^^^^^^^^^^^^^^^^^^^
- Holds column

  A new column will show how many request are on an item that is being modified.

    .. image:: /screenshots/0530.jpg
