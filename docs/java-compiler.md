[//]: # (Source: https://www.jetbrains.com/help/idea/java-compiler.html)
[//]: # (Downloaded: 2025-12-17 19:30:11)

## Compiler and bytecode versions

Item| Description  
---|---  
Use compiler| Select the compiler to be used: 

  * [Javac](http://docs.oracle.com/javase/8/docs/technotes/tools/windows/javac.html). This may be the compiler included in the IntelliJ IDEA distribution or a compiler from one of the project JDKs.
  * Eclipse (also known as Eclipse Compiler for Java or ECJ). IntelliJ IDEA comes bundled with the Eclipse compiler.
  * [Groovy-Eclipse](http://andrewclement.blogspot.ru/2010/02/running-groovy-eclipse-joint-compiler.html). This compiler lets you perform joint compilation of Groovy and Java code using the Eclipse compiler.

  
Use '--release option' for cross-compilation (Java 9 and later)| By default, this option is selected. IntelliJ IDEA deduces from project settings when the cross-compilation is needed and automatically applies the `--release` compiler option for Java 9.  
Project bytecode version| Select the version of bytecode to be generated. (Roughly, this is the minimum target JVM version.) If no particular version is specified, the bytecode version is defined by the compiler.To specify different versions for particular modules, use the controls in the Per-module bytecode version area.  
Per-module bytecode version| If necessary, specify the target bytecode versions for individual modules (for example, if they should differ from that [set for the project](#bytecode)). Click ![Add](https://resources.jetbrains.com/help/img/idea/2025.3/app.expui.general.add.svg) and select the modules of interest in the dialog that opens. Then, for each of the modules, click the corresponding Target bytecode version cell and select the version from the list.Use ![Remove](https://resources.jetbrains.com/help/img/idea/2025.3/app.expui.general.remove.svg) to remove the selected module or modules from the list.
