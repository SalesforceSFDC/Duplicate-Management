# Duplicate Management
* Matching rule - The matching criteria to identify duplicate records.
  * Salesforce comes with three standard matching rules: 
    * one for business accounts; 
    * one for contacts and leads, 
    * and another for person accounts. 
* Duplicate rule - Depending on how you configure Duplicate Management, sales reps see an alert that they’re about to create a duplicate. Or your reps are blocked from creating the duplicate altogether.
#
* Matching rule determines whether the record a user is creating or updating is similar enough to other records to be considered a duplicate.
* Duplicate rule tells Salesforce what action to take when duplicates are identified. 
### Sharing Rules
Specify how your organization's sharing rules determine which records the matching rule compares.

Enforce sharing rules: The matching rule compares only records that the user has access to, and the resulting list of possible duplicates includes only records the user has access to.

Bypass sharing rules: The matching rule compares all records, regardless of user access, but the resulting list of possible duplicates includes only records the user has access to.
### Manage Duplicate Records
Starting in Spring ‘15, all new Salesforce orgs come with Duplicate Management features already
set up and turned on for accounts, contacts, and leads. 

#### New Records
* (1) When a user attempts to save a new record, the record is first compared with existing Salesforce
records to identify possible duplicates.
* (2) The criteria used to compare records and identify the possible duplicates are defined by
a matching rule. 
* (3) A list of possible duplicates is returned 
* (4) The record being saved is identified as a possible duplicate depends on what’s defined in the duplicate rule 
  *  For example, the duplicate rule could block users from saving the
possible duplicate record or allow them to save it anyway. Both the Block and Allow options include an alert, which tells users why they can’t save the record and what they need to do. The Allow option includes the ability to report on the duplicate records.

#### Edited Records
* When a user attempts to save an edited record, the record is first checked to see if the user has changed the value of a matching rule
field. If so, the duplicate management process works as described for new records. If not, no further action is taken and duplicates
are not detected.



Contact and Lead Field|Matching Algorithms|Special Handling|Example
--- | --- | --- | ---
First Name|Exact, Initials, Jaro-Winkler Distance, Metaphone 3, Name Variant|If the record contains a value for both First Name and Last Name fields, those values are transposed to consider possible data entry mistakes. |The first name is Luis and the last name is Antonio. The matching rule evaluates the first name as Antonio and the last name as Luis.
Last Name|Acronym, Exact, Kullback-Liebler Distance|Considers acronyms and full titles.|The title is VP. The matching rule considers VP and Vice President.
## Resources 
* [Manage Duplicate Records](https://help.salesforce.com/articleView?id=managing_duplicates_overview.htm)
* [Standard Matching Rules](https://help.salesforce.com/articleView?id=matching_rules_standard_rules.htm)
* [Standard Duplicate Rules](https://help.salesforce.com/articleView?id=duplicate_rules_standard_rules.htm)
* [Customize Matching Rules](https://help.salesforce.com/articleView?id=matching_rules_create.htm)
* [Matching Rules](https://help.salesforce.com/articleView?id=matching_rule_map_of_reference.htm)
* [Duplicate Rules](https://help.salesforce.com/articleView?id=duplicate_rules_map_of_reference.htm)
