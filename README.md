Estate Ownership Ledger
A lightweight, browser-based tool for reconstructing and verifying complex ownership chains using fractional interests. Designed for title review, estate reconstruction, and situations where ownership evolves through inheritance and conveyances.

Purpose
This tool helps track how ownership interests move over time and verifies that the final ownership structure adds up correctly.
It is particularly useful when:


ownership is fragmented across generations


fractions use different bases (72, 288, 360, etc.)


documents are inconsistent or incomplete


you need a clean “final ownership” view from messy history



Core Concept
The ledger uses a tree structure:


A row represents an ownership interest


Subrows represent a division of that interest


Only rows marked as Counted contribute to final totals


This allows you to:


model inheritance chains


track conveyances


separate historical structure from current ownership



Features
1. Hierarchical Ownership Tracking


Add rows and subrows (“Divide”)


Each level represents a breakdown of the parent interest


Visual indentation shows structure


2. Fraction + Percentage Sync


Enter either fraction (e.g., 1/72) or percentage


The other field auto-updates


Internally computed as decimals


3. Final Ownership Control


Each row has a Count checkbox


Only checked rows are included in:


Grand Total


Owner Summary




4. Owner Summary


Aggregates all counted rows by name


Displays:


Fraction


Percentage


1440-unit normalization




5. 1440 Unit System


Converts all interests into a common base (1440)


Avoids denominator mismatch issues


Makes comparison and validation easier


6. Drag and Reorder


Drag rows using the handle (☰)


Reorders within the same level only


Structure is preserved (no accidental nesting)


7. Column Resizing


Drag column edges to resize


Table expands horizontally as needed


8. Local Persistence


Data is saved in localStorage


Survives page refresh


No backend required


9. CSV Export


Export the entire ledger


Includes hierarchy levels and count status



How to Use
Build the Chain


Add a main row for the starting owner


Use Divide to break into heirs or transfers


Continue building down the chain


Track Transfers


Represent conveyances as new rows under the relevant party


Use notes to document deed references


Mark Final Owners


Check Count only for current ownership interests


Leave historical rows unchecked


Verify Totals


Grand Total should equal 1 / 100% / 1440


Owner Summary shows final distribution by owner



Example
Final result:


Carl Brass → 111/360


Joseph Brass → 85/360 (split internally if needed)


John Brass Revocable Trust → 39/360


M&E Farms → 125/360


The tool ensures:


totals reconcile


structure remains traceable


inconsistencies are visible



Design Philosophy
This tool separates:
History (how ownership got here)
from
State (who owns what now)
It avoids:


double counting


denominator confusion


reliance on inconsistent summaries



Known Limitations


Does not validate legal correctness of title


Assumes user input is accurate


Does not enforce deed-level constraints


Complex conveyances must be modeled manually



When to Use
Use this tool when:


reconstructing ownership from multiple documents


analyzing inconsistencies in title reports


validating whether interests properly sum to 1


preparing for title underwriting or review



When Not to Use
Do not rely on this tool as a substitute for:


official title search


recorded deed verification


legal opinion on ownership



Summary
This tool provides a structured way to:


model ownership chains


reconcile fractions


isolate inconsistencies


produce a clean final ownership view


It is a working analysis tool, not an authoritative record.
