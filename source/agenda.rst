Koha 18.11 Trainng Agenda
==========================

#. Koha homepage
  #. Patron notes on staff dashboard

#. Cataloging

  #. Z39.50
    #. Focus on ISBN field
    Quick demo.
    #. Additional columns in Z39.50 results
    Do a cataloging search for DAY OF THE JACKAL as example
  #.


#. Circulation

  #. Collection code in checkout table
  Go to FROSTX011
  #. Circulation history - click barcode goes to item record
  Go to FROSTX011
  #. Patron information in left column is now hidden
  Go to FROSTX011

#. Fines changes

  #. Item "Lost" twice by the same patron isn't billed the second time.
  I can't really show you this situation, but this is an outline of the circumstances:
    #. Patron checks out an item and returns it more than 45 days overdue and is billed for the item
    #. Patron returns the item and the cost of the item is refunded
    #. Patron checks out the item again and keeps it more than 45 days overdue again
    #. Up until now, Koha has not been able to bill the patron for the second time the item has been declared "Lost"
  #. Paying fines on accounts with credits
  Also one I can't show you.  If a patron had a fee and a credit, a bug would sometimes cause additional payments to fail.
  #. Item home branch shows in fee table.
  This one I can show you.  Go to FROSTX011.
  #. Writeoff selected
  Also on FROSTX011 - demonstrate how to write off a specific fee (writeoff RED SPARROW and READY PLAYER ONE).
  #. Void credit.
  Demonstrate on FROSTX011.
  #. Email receipts for payments
  When a patron pays a fee or a fee is written off, AND the patron has an e-mail address, the patron will receive an e-mail receipt for the payment/writeoff.
    #. This is a global system setting - currently the messages cannot be configured on a library-by-library basis.

#. Holds/Requests

  #. Split holds queue
  Demonstrate with 0003012081166
  #. Collection code added to holds table
  Search for RED SPARROW

#. OPAC

  #. Browse the shelf
  Code has been modified
  #. Hooks for patron branchcode and userid in pages when a user is logged in
  This is a behind the scenes thing, but it can make parts of the OPAC customizable
  

#. Searching

  #. Split "Advanced search" button
  Appears on all pages.


#. Patrons

  #. Guarantees sorted alphabetically
  This was a stealth upgrade - we already have it, I just wanted to point it out to everyone.
  #. Renewal date on details page.
  Go to FROSTX011.  Also a stealth upgrade.
  #. Updated date in left column on all patrons where the information is displayed
  Go to FROSTX011.


#. Reports

  #. Create charts in Reports
  Run report 3171 in test to demonstrate.
  #. Codemirror
  Line numbers in report creation tool.

#. Tools

  #. Inventory
    #. Items scanned out of order
    #. Allow skipping items with waiting holds

  #. Notices
    #. Table is searchable

  #. Patron lists
    #. Share patron lists between staff

  #. Batch item modification
    #. Holds column
    Shows how many holds are on an item.
