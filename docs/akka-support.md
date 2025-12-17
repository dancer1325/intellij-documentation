[//]: # (Source: https://www.jetbrains.com/help/idea/akka-support.html)
[//]: # (Downloaded: 2025-12-17 19:18:02)

## Work with Akka code in the editor

Besides basic code completion, code generation, and code navigation support, IntelliJ IDEA supports Akka inspections, find usages with Akka context, and specific code generation actions for Akka.

### Use Akka code inspections

You can check the list of available Akka inspections and their descriptions in the Editor | Inspections settings page `Ctrl+Alt+S`.

![the Inspections settings](https://resources.jetbrains.com/help/img/idea/2025.3/akka_inspections.png)

In the editor, IntelliJ IDEA displays suggestion hints where the inspections could work, and you can check the following examples with suggested changes that might improve your code:

  * Replace dynamic invocation with a constructor invocation: part of code could be simplified with a replacement. 

![Active editor](https://resources.jetbrains.com/help/img/idea/2025.3/factory_method_simplified.png)

Code example:

import akka.actor._ abstract class Foo extends AbstractActor object Foo { def props: Props = Props(classOf[Foo]) } 

import akka.actor._ abstract class Foo extends AbstractActor object Foo { def props: Props = Props(new Foo()) } 

  * Replace with a factory method call: dynamic constructor call could be safely replaced with a factory method call. 

![Intention Action](https://resources.jetbrains.com/help/img/idea/2025.3/replace_with_factory_methodcall.png)

Code example:

import akka.actor._ class Foo(foo: String, bar: Int) extends AbstractActor { override def createReceive(): AbstractActor.Receive = ??? } object Foo { def props(foo: String, bar: Int): Props = Props(new Foo(foo, bar)) } Props(classOf[Foo], "foo", 42) 

import akka.actor._ class Foo(foo: String, bar: Int) extends AbstractActor { override def createReceive(): AbstractActor.Receive = ??? } object Foo { def props(foo: String, bar: Int): Props = Props(new Foo(foo, bar)) } Foo.props("foo", 42) 

  * Appropriate actor constructor not found: the inspection will work in a place where a constructor with inappropriate arguments is called. 

![Actor constructor not found](https://resources.jetbrains.com/help/img/idea/2025.3/akka_actor_constructor.png)
  * Akka mutable state: the inspection detects if the Actor has a mutable state. 

Code example:

import scala.collection.mutable class MyActor extends Actor { val isInSet = mutable.Set.empty[String] def receive = { case Add(key) => isInSet += key case Contains(key) => sender() ! isInSet(key) } } 

import collection.immutable.Set class MyActor extends Actor { def receive = active(Set.empty) def active(isInSet: Set[String]): Receive = { case Add(key) => context become active(isInSet + key) case Contains(key) => sender() ! isInSet(key) } } 




### Use intentions in Akka

You can check the list of available intention actions for Scala and Akka in the Editor | Inspections settings page `Ctrl+Alt+S`.

![Akka intentions settings](https://resources.jetbrains.com/help/img/idea/2025.3/akka_intentions.png)

In the editor, IntelliJ IDEA displays the ![the Intention action icon](https://resources.jetbrains.com/help/img/idea/2025.3/app.expui.codeInsight.intentionBulb.png) popup with suggestions to improve your code. Check the following examples of the related intentions for Akka:

  * Generate actor factory methods: IntelliJ IDEA supports the automatic generation of factory methods. In the editor, place the caret inside the companion object of an `Actor`, press `Alt+Insert` and select the intention. 

  * Create a corresponding factory method: IntelliJ IDEA supports the automatic generation of the corresponding factory methods. 

  * IntelliJ IDEA supports intentions for refactorings. For example, when you extract variable `Ctrl+Alt+V`, IntelliJ IDEA will suggest a name and a type for the inline refactoring. 



