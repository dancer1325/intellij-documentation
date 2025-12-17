[//]: # (Source: https://www.jetbrains.com/help/idea/language-services.html)
[//]: # (Downloaded: 2025-12-17 19:31:16)

## Configure memory handling

Although IntelliJ IDEA strives at providing slick integration with language services, there may still arise out-of-memory errors induced by a language service rather than by IntelliJ IDEA itself. 

### Memory handling modes

When a language service runs out of memory, IntelliJ IDEA first attempts to restart it. After two sequential attempts fail, the language service stops and IntelliJ IDEA indicates the error in the Language Services widget on the status bar and displays a popup with an error message.

To prevent out-of-memory errors or have them solved seamlessly, thus ensuring stable operation of language services, you can configure memory handling in the following two modes: 

#### Increase memory automatically

In this mode, IntelliJ IDEA automatically adds 1000MB when an out-of-memory error is to occur and restarts the language service in the background.

IntelliJ IDEA continues silently with this approach until the maximum memory limit of 25% RAM is reached, whereupon the language service stops and IntelliJ IDEA displays a popup with an error message.

For information on possible steps to improve the situation, refer to [Troubleshooting](#ls_troubleshooting).

#### Set memory limit

In this mode, you manually specify maximum memory a language service can use. Until this limit is reached, IntelliJ IDEA suggests adding 1000MB on each out-of-memory error.

When the specified limit is reached, the language service stops and IntelliJ IDEA displays a popup with an error message.

For information on possible steps to improve the situation, refer to [Troubleshooting](#ls_troubleshooting).

### Configure memory handling for TypeScript language service

Memory handling settings for Vue, Svelte, Astro, and other language services are always inherited from the TypeScript language service. 

  1. Open settings by pressing `Ctrl+Alt+S` and navigate to Settings | Languages & Frameworks | Language Services | TypeScript. 

  2. In the Language Services Memory area, choose the memory handling mode:

     * Select Automatically increase memory, if available to have memory increased and language services restarted silently.

     * Alternatively, select Set memory limit and specify the maximum memory to use by a language service.

If the specified memory size exceeds the available RAM, IntelliJ IDEA suggests an appropriate value in a tooltip.

Make sure your computer has enough available RAM. If you are already at a high allocation, for example, 8GB+, consider [upgrading/downgrading](#ls_upgrade_downgrade) or [limiting your project scope](#ls_limit_project_scope).



