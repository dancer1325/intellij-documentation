[//]: # (Source: https://www.jetbrains.com/help/idea/components-properties.html)
[//]: # (Downloaded: 2025-12-17 19:21:27)

## Code Binding Properties

The properties covered in this section are related to binding of GUI forms and components to source code.

Property| Description  
---|---  
bind to class| This is a property of Forms only. It specifies the name of a class that contains the logic to make the form work. When this property is set to a valid class, we say the Form is bound to the class.If no target class exists yet, you can still type in the name of this _future_ class. IntelliJ IDEA will offer a quick-fix to create a class of the specified name for you whenever the property is focused. You can use the quick-fix to create the class whenever you are ready.  
field name| This is a property of components. It specifies the name of the field in the parent form's class to which the component is bound. For most components, a default field name is automatically entered, and a corresponding declaration is written to the Form's bound source file. You can change the default field name in the Inspector if you wish, and the source will be updated automatically. You can optionally [change the field name](rename-refactorings.html) in the source file, and the change will reflect in the Inspector when you return to the GUI Designer.  
Custom Create| This is a property of components. If the option is checked, it means that you want to call a non-default constructor for the component, rather than generate a default constructor during the runtime build of the GUI. Code generation will ignore the component and assume you have written a constructor method.If a non-default constructor does not yet exist, IntelliJ IDEA will show you a quick-fix whenever the Custom Create property is focused in the Inspector. You can use this to create the constructor in the source file bound to the parent Form.
