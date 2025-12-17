[//]: # (Source: https://www.jetbrains.com/help/idea/handling-issues.html)
[//]: # (Downloaded: 2025-12-17 19:28:37)

## Example

The example below shows how IntelliJ IDEA applies the mentioned rules to detect a reference to an issue in a commit message and compose a link to it in the issue tracking system.

![Add Issue Navigation Link dialog](https://resources.jetbrains.com/help/img/idea/2025.3/ij_add_issue_navigation_link.png)

Issue ID| A [regular expression](regular-expressions.html) that defines the format for issue references in commit messages.[A-Z]+\\-\d+This regular expression matches all character strings that consist of two substrings separated by an n-dash character:

  1. Substring 1: An unlimited number of upper-case alphabetic characters.
  2. Substring 2: An unlimited number of digital characters.

For more information about using special characters in regular expressions, refer to [Regular Expressions Syntax Reference](regular-expressions.html).  
---|---  
Issue link| A combination of the URL address of your issue tracking system and a regular expression that identifies issues in it.http://<mytracker>/issue/$0Here `$0` indicates a back reference to the entire match. This means that as soon as IntelliJ IDEA detects a match in a commit message, it is added to the URL address of the tracker as is.  
Matching issue ID| IntelliJ IDEA detects the following reference to an issue in the commit message of interest:MYPROJECT-110  
Composed issue link| In accordance with the above issue navigation pattern, the detected matching reference is added to the URL of the tracker as is, so the link to the referenced issue is composed as follows:http://mytracker/issue/MYPROJECT-110
