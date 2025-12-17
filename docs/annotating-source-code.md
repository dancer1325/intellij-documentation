[//]: # (Source: https://www.jetbrains.com/help/idea/annotating-source-code.html)
[//]: # (Downloaded: 2025-12-17 19:18:16)

## Code contract annotations

There is also a class of annotations describing code semantics and contracts. They can be used by developers to better understand the implications of using a particular API as well as assist static analyzers to identify problematic areas.

public @Nullable List<Double> getDiscounts() { return discounts; } 

IntelliJ IDEA recognizes popular Java annotations and takes them into account when analyzing code. Examples of such annotation frameworks are [Checker Framework](https://checkerframework.org) and [ErrorProne](https://errorprone.info)

For information on JetBrains' `@Contract` annotation, refer to the [official repository](https://github.com/JetBrains/java-annotations/blob/master/src/jvmMain/java/org/jetbrains/annotations/Contract.java).

### Nullability annotations

Nullability annotations are a subset of code contract annotations. By explicitly declaring the nullability of elements, the code becomes easier to maintain and less prone to nullability-related errors.

On the other hand, IntelliJ IDEA's static analysis will be using these annotations to catch potential errors at design-time. For example, IntelliJ IDEA will analyze the data flow in your project and report attempts to dereference a variable that can potentially be `null`, or vice versa, suggest getting rid of redundant guard conditions where they are safe to remove.

### Configure nullability annotations

While IntelliJ IDEA recognizes the popular nullability annotations, you may still want to add your custom annotations to the list. IntelliJ IDEA will then use them for determining the nullability of a symbol.

  1. Go to Settings | Editor | Inspections | Probable bugs | Nullability and data flow problems.

  2. Under Options, select Configure Annotations.




#### Default nullability annotations

By default, the following annotations are recognized by IntelliJ IDEA:

  * android.support.annotation.Nullable

  * androidx.annotation.Nullable

  * androidx.annotation.RecentlyNullable

  * com.android.annotations.Nullable

  * edu.umd.cs.findbugs.annotations.Nullable

  * io.reactivex.annotations.Nullable

  * io.reactivex.rxjava3.annotations.Nullable

  * jakarta.annotation.Nullable

  * javax.annotation.CheckForNull

  * javax.annotation.Nullable

  * org.checkerframework.checker.nullness.compatqual.NullableDecl

  * org.checkerframework.checker.nullness.compatqual.NullableType

  * org.checkerframework.checker.nullness.qual.Nullable

  * org.eclipse.jdt.annotation.Nullable

  * org.jetbrains.annotations.Nullable

  * org.jspecify.annotations.Nullable




  * android.support.annotation.NonNull

  * androidx.annotation.NonNull

  * androidx.annotation.RecentlyNonNull

  * com.android.annotations.NonNull

  * edu.umd.cs.findbugs.annotations.NonNull

  * io.reactivex.annotations.NonNull

  * io.reactivex.rxjava3.annotations.NonNull

  * jakarta.annotation.Nonnull

  * javax.annotation.Nonnull

  * lombok.NonNull

  * org.checkerframework.checker.nullness.compatqual.NonNullDecl

  * org.checkerframework.checker.nullness.compatqual.NonNullType

  * org.checkerframework.checker.nullness.qual.NonNull

  * org.eclipse.jdt.annotation.NonNull

  * org.jetbrains.annotations.NotNull

  * org.jspecify.annotations.NonNull




### Disable nullability assertions

When you compile your project with IntelliJ IDEA build tool, the IDE adds assertions to all code elements annotated with `@NotNull`. These assertions will throw an error if the elements happen to be `null` at runtime. This fail-fast behavior may help you to diagnose the problems at an early stage. If this is not the desired effect for you, you can disable these assertions.

  * Go to Settings `Ctrl+Alt+S` | Build, Execution, Deployment | Compiler and uncheck the Add runtime assertions for notnull-annotated methods and parameters option.




### Infer nullity

If your project is missing nullability annotations, completely or partially, you can have IntelliJ IDEA infer and insert the nullability annotations for you.

  1. Make sure the library with annotations is configured for your project. IntelliJ IDEA uses the annotation specified in Annotation used for code generation in Settings | Editor | Inspections | Probable Bugs | Nullability and data flow problems | Configure Annotations.

If you want to use [JetBrains annotations](#jetbrains-annotations), and you are using IntelliJ IDEA build tool, the IDE will detect the missing dependency and suggest to add it automatically

  2. In the main menu, go to Code | Analyze Code | Infer Nullity.

  3. In the Specify Infer Nullity Scope dialog, select the scope of the analysis. If you want to include test sources or annotate local variables, select the corresponding checkboxes.




### JetBrains annotations dependency

IntelliJ IDEA has its own annotations set available as a separate dependency. It contains annotations for expressing nullability, ranges, contracts, mutability, purity, and more.

The package consists of several dozens of annotations. Some of the most common are:

  * `@Nullable` and `@NotNull` – indicate a variable, parameter, or return value that can or cannot be null.

  * `@Nls` – indicates that an annotated code element is a string that needs to be localized.

  * `@NonNls` – indicates that an annotated code element is a string which is not visible to users, which doesn't require localization, and which doesn't contain strings requiring localization. When you annotate an element with `@NonNls`, localization tools will skip this element and strings inside it.

  * `@PropertyKey` – indicates that a method parameter accepts arguments that must be valid property keys in a specific resource bundle. When a string literal that is not a property key in a bundle is passed as a parameter, IntelliJ IDEA highlights it as an error. The annotation is also used to provide completion in string literals passed as parameters.

  * `@TestOnly` – indicates that a method or a constructor must be called from testing code only.

  * `@Contract` – lets you specify a set of rules (a contract) that a method must follow. If the contract is violated, IntelliJ IDEA reports a problem.

  * `@Language` – injects code written in another language in a Java String.




For full annotations' descriptions, use quick documentation `Ctrl+Q` or refer to the [package repository](https://github.com/JetBrains/java-annotations).

### Add JetBrains Annotations dependency to the project

  * When you use a JetBrains annotation in your code, the Add 'annotations' to classpath intention action will help you quickly add the required dependency.

![Annotations quick fix](https://resources.jetbrains.com/help/img/idea/2025.3/annotations-quick-fix.png)
  * Otherwise, you can add it manually, using the following artifact coordinates: <https://central.sonatype.com/artifact/org.jetbrains/annotations/24.0.1>

<dependencies> <dependency> <groupId>org.jetbrains</groupId> <artifactId>annotations</artifactId> <version>26.0.2</version> <scope>provided</scope> </dependency> </dependencies>

dependencies { compileOnly 'org.jetbrains:annotations:26.0.2' } 

dependencies { compileOnly("org.jetbrains:annotations:26.0.2") } 

Go to Project Structure `Ctrl+Alt+Shift+S` | Libraries. Click ![](https://resources.jetbrains.com/help/img/idea/2025.3/app.expui.general.add.svg), and select From Maven. In the search field, type `org.jetbrains:annotations:26.0.2`. Click OK.

For JDK 1.5 through 1.7, use the [annotations-java5](https://mvnrepository.com/artifact/org.jetbrains/annotations-java5) artifact.



