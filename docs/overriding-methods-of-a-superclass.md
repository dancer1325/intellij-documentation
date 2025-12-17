[//]: # (Source: https://www.jetbrains.com/help/idea/overriding-methods-of-a-superclass.html)
[//]: # (Downloaded: 2025-12-17 19:33:41)

## Change the method body

The code template used for overriding methods (Overridden method body) accepts predefined template variables from the File Header include template (such as `${USER}`, `${DATE}`, and so on).

For example, consider the following code template:

#if ( $RETURN_TYPE != "void" )return $DEFAULT_RETURN_VALUE;#end // TODO ($USER, $DATE):To change the body of an implemented method, use File | Settings - Editor - File and Code Templates. 

Provided that the overridden class contains two methods, this template expands into the following code:

public void breathe() { // TODO (wombat, 9/21/22): To change the method body, use Settings - Editor - File and Code Templates. } public void eat() { // TODO (wombat, 9/21/22): To change the method body, use Settings - Editor - File and Code Templates. } 
