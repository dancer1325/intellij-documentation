[//]: # (Source: https://www.jetbrains.com/help/idea/coding-assistance-for-rest-development.html)
[//]: # (Downloaded: 2025-12-17 19:20:55)

## Code Inspection and Quick Fixes

IntelliJ IDEA supports [code inspections](code-inspection.html) and suggests [quick fixes](resolving-problems.html) in the following cases:

Issue| Default Quick Fix  
---|---  
Inconsistency between a method annotation and the method return type: a `@GET` annotated method returns void value.| Change to String.  
Resource methods errors.| Remove `@Path` annotation.  
Incorrect parameter type.| Validation for parameters annotated with `@QueryParam` or `@PathParam` annotations.  
`@DefaultValue` issues.|  @GET public String get(@DefaultValue("33.5") @QueryParam("str") int str) { return "Hello"; }  `DefaultValue` is marked red with the description "Can't convert to int".  
Rest `@Path` and `@PathParam` annotations inspections.  
Rest References resolve problems.| References in `@PathParam` annotations are resolved to templates in `@Path` annotations  
This method should have only one HTTP method designator.| Example:  @GET @POST public String get(){ return "Hello"; }  `@POST` is marked red.
