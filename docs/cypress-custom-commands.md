[//]: # (Source: https://www.jetbrains.com/help/idea/cypress-custom-commands.html)
[//]: # (Downloaded: 2025-12-17 19:23:49)

## Custom Commands coding assistance

### Cypress-specific inspections

Cypress utilizes a [chaining mechanism](https://docs.cypress.io/guides/core-concepts/introduction-to-cypress#Chains-of-Commands) that allows you to write a sequence of commands where information is passed from one command to the next until the chain ends or an error occurs.

However, this mechanism has some specifics. For example, any [action command](https://docs.cypress.io/guides/core-concepts/interacting-with-elements#Actionability) must always be placed at the end of the chain and used only once.

In this example, the chain contains two action commands placed one after another, which is prohibited. The execution of this test will result in an error.

it('Click the search button and type Cypress', () => { cy.get("button[data-test='search-button']") .click() .type('Cypress') }) 

In this example, the chain is split in two, so each chain contains only one action command. This test will be executed without an issue.

it('Click the search button and type Cypress', () => { cy.get("button[data-test='search-button']").click() cy.get("input[data-test$='inner']").type('Cypress') }) 

Validation of the command chain is not performed in JavaScript/TypeScript, and in Cypress it is performed only at runtime, which may lead to issues during the test execution. IntelliJ IDEA, in its turn, provides an inspection for chained commands, highlighting incorrect usages.

![Inspection for an incorrect chained command](https://resources.jetbrains.com/help/img/idea/2025.3/aqua_incorrect_command_chain.png)

### Function-specific inspections

IntelliJ IDEA performs function-specific code inspections that detect and correct abnormal code in your project.

For example, if you provide an incorrect number or type of arguments for the command, the erroneous code gets highlighted. You can hover the mouse over the highlighted code to see the description of the error.

![Aqua ts function specific inspections](https://resources.jetbrains.com/help/img/idea/2025.3/aqua_ts_function_specific_inspections.png)

For more information, refer to [Code inspections](code-inspection.html).

### Renaming

If you need to rename the command, you can use the Rename refactoring. To do this:

  1. Highlight the command that you want to rename. 

![Highlighted command](https://resources.jetbrains.com/help/img/idea/2025.3/aqua_highlighted_command.png)
  2. Press `Shift+F6` and provide a new name for the command. 

![Rename the command](https://resources.jetbrains.com/help/img/idea/2025.3/aqua_rename_refactoring.png)
  3. (Optional) Configure additional search options and define scope.

  4. Click Refactor.




For more information, refer to [Rename refactorings](rename-refactorings.html).
