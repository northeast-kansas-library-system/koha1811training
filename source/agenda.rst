Koha 18.11 Trainng Agenda
==========================

-  Koha homepage
  -  Patron notes on staff dashboard

-  Cataloging

  -  Z39.50
    -  Focus on ISBN field
    Quick demo.
    -  Additional columns in Z39.50 results
    Do a cataloging search for DAY OF THE JACKAL as example
  -  Add item reversion
  Show changes in alignment in add item table.
  -  Cataloging add record problem.
  More or less the same as the "Add item" problem


-  Circulation

  -  Collection code in checkout table
  Go to FROSTX011
  -  Circulation history - click barcode goes to item record
  Go to FROSTX011
  -  Patron information in left column is now hidden
  Go to FROSTX011

-  Fines changes

  -  Item "Lost" twice by the same patron isn't billed the second time.
  I can't really show you this situation, but this is an outline of the circumstances:
    -  Patron checks out an item and returns it more than 45 days overdue and is billed for the item
    -  Patron returns the item and the cost of the item is refunded
    -  Patron checks out the item again and keeps it more than 45 days overdue again
    -  Up until now, Koha has not been able to bill the patron for the second time the item has been declared "Lost"
  -  Paying fines on accounts with credits
  Also one I can't show you.  If a patron had a fee and a credit, a bug would sometimes cause additional payments to fail.
  -  Item home branch shows in fee table.
  This one I can show you.  Go to FROSTX011.
  -  Writeoff selected
  Also on FROSTX011 - demonstrate how to write off a specific fee (writeoff RED SPARROW and READY PLAYER ONE).
  -  Void credit.
  Demonstrate on FROSTX011.
  -  Email receipts for payments
  When a patron pays a fee or a fee is written off, AND the patron has an e-mail address, the patron will receive an e-mail receipt for the payment/writeoff.
    -  This is a global system setting - currently the messages cannot be configured on a library-by-library basis.

-  Holds/Requests

  -  BUG! - cannot place item level Requests
  This is a bug and should be fixed soon.  Our tentative date for the upgrade is June 15 and I will keep an eye on this bug and ask that we not be upgraded until it is fixed.  I'm pretty confident, though, that it should be fixed by June 15 (it may actually be fixed by May 15).
  -  Collection code added to holds table
  Search for RED SPARROW
  -  Split holds queue
  Demonstrate with 0003012081166
  -  Long standing bug should be fixed (mostly)
  Meg 0003008201823 and Bohemian rhapsody 0003008201838 -


-  OPAC

  -  Many CSS elements have changed - so if something looks weird or doesn't look right, be sure to let us know.  Dan and I should be able to change anything that doesn't work correctly caused by changes to the CSS.
  -  Cart opens with one click
  Demo on production and test.
  -  Login modal has changed
  Demo on production and test.
  -  Logging in during search keeps you in search.
  Search JACKAL and log in as FROSTX022 (12345!) in production and test.
  -  Browse the shelf and Browse results
  Code has been modified
  -  Expanded data for branchcode and userid in pages when a user is logged in
  This is a behind the scenes thing, but it can make parts of the OPAC customizable on a branch-by-branch basis


-  Searching, results, and details

  -  Split "Advanced search" button in Staff
  Appears on all pages.
  -  Facets for CCODE - Staff and OPAC
  Allows for more granular searching - Do a search for "Horses"
  -  Cart sorting and printing
  If you sort items in the cart, you can print them in the order you sort them in.  (stealth upgrade)
  -  Holdings count
  Tab will show a holdings count.  Production 0003008201343 - test 0003012081166; test 0003008201777.
  -  Date accessioned
  Date accessioned is visible on details page - and sortable
  -  Checkout history toolbar
  Column visibility tools - export to csv/copy/print
  -  526 now indexed
  Will allow for better accelerated reader searches - requires reindex

-  Patrons

  -  Guarantees sorted alphabetically
  This was a stealth upgrade - we already have it, I just wanted to point it out to everyone.
  -  Renewal date on details page.
  Go to FROSTX011.  Also a stealth upgrade.
  -  Updated date in left column on all patrons where the information is displayed
  Go to FROSTX011.


-  Reports

  -  Create charts in Reports
  Run report 3171 in test to demonstrate.
  -  Codemirror
  Line numbers in report creation tool.


-  Tools/Administration

  -  Circulation/fines/fees rules
    -  Notes on circulation rules
    This adds the ability to add a note to the circulation rules so that I'll be better able to track changes to circulation rules.

  -  Inventory
    -  Items scanned out of order
    -  Allow skipping items with waiting holds

  -  Label creator and Card creator
    -  Able to add descriptions
    Production and on Test - card batch 13998 in production - batch called "Batch of Movies" in test.  Card batch 8289 in production and test - Card batch 14002 in production vs 13334 in test.
    -  Pop-up when searching for patron in Card creator
    Demo on the Frosty list
    -  Flexibility in call number splitting rules
    This one is impossible to demonstrate today - it's going to require a ton of set up, but, basically, the current process with the label creator is that you can have it split the call numbers where the spaces occur - so that REF 823.43 SHA has "REF" "823.43" and "SHA" all on separate lines.  This new feature would allow you to customize where the splits occur.  It will, however require changing the frameworks so the 952$2 is visible and then changing the selection for the 952$2 on the items you want to create new labels for.

  -  Lists
    -  Sort list by date added
    James Bond films list Production and Test

  -  Notices
    -  Table is searchable

  -  Patron lists
    -  Share patron lists between staff

  -  Batch item modification
    -  Holds column
    Shows how many holds are on an item.
