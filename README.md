# Duplicate Management
* Matching rule - The matching criteria to identify duplicate records.
  * Salesforce comes with three standard matching rules: 
    * one for business accounts; 
    * one for contacts and leads, 
    * and another for person accounts. 
* Duplicate rule - Depending on how you configure Duplicate Management, sales reps see an alert that they’re about to create a duplicate. Or your reps are blocked from creating the duplicate altogether.

Contact and Lead Field|Matching Algorithms|Special Handling|Example
--- | --- | --- | ---
Exact, Initials, Jaro-Winkler Distance, Metaphone 3, Name Variant|If the record contains a value for both First Name and Last Name fields, those values are transposed to consider possible data entry mistakes.|
## Resources 
* [Manage Duplicate Records](https://help.salesforce.com/articleView?id=managing_duplicates_overview.htm)
* [Standard Matching Rules](https://help.salesforce.com/articleView?id=matching_rules_standard_rules.htm)
* [Standard Duplicate Rules](https://help.salesforce.com/articleView?id=duplicate_rules_standard_rules.htm)
* [Customize Matching Rules](https://help.salesforce.com/articleView?id=matching_rules_create.htm)
* [Matching Rules](https://help.salesforce.com/articleView?id=matching_rule_map_of_reference.htm)
* [Duplicate Rules](https://help.salesforce.com/articleView?id=duplicate_rules_map_of_reference.htm)
