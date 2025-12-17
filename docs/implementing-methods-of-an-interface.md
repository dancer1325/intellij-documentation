[//]: # (Source: https://www.jetbrains.com/help/idea/implementing-methods-of-an-interface.html)
[//]: # (Downloaded: 2025-12-17 19:29:14)

## Change method body

The code template used for implementing methods (Implemented method body) accepts predefined template variables from the File Header include template (such as `${USER}`, `${DATE}`, and so on)

For example, consider the following file template:

#if ( $RETURN_TYPE != "void" )return $DEFAULT_RETURN_VALUE;#end // TODO ($USER, $DATE):To change the body of an implemented method, use File | Settings - Editor - File and Code Templates. 

Provided that the implemented interface contains two methods, this template expands into the following code:

@Override public void hunt() { // TODO (wombat, 9/21/12): To change the body of an implemented method, use File | Settings - Editor - File and Code Templates. } @Override public String sniff() { return null; // TODO (wombat, 9/21/12): To change body of implemented methods use File | Settings - Editor - File and Code Templates. } 

### Configure nullability annotations

You can configure the [nullability annotations](annotating-source-code.html) for the generated code.

  1. Press `Ctrl+Alt+S` to open settings and then select Settings | Editor | Inspections | Probable Bugs | Nullability and data flow problems. 

  2. Click Configure Annotations, then select the annotation in Annotation used for code generation.



