[//]: # (Source: https://www.jetbrains.com/help/idea/copyright.html)
[//]: # (Downloaded: 2025-12-17 19:22:37)

## Configure copyright profiles

In IntelliJ IDEA, copyright profiles can be local and shared.

Shared profiles are stored in the .idea/copyright in .xml files and are available to other members of your team through VCS.

Local copyright profiles are stored on the IDE level and are available in all projects that you open in the current IDE instance.

### Create a new copyright profile

A profile allows you to define a copyright text that you can later insert across the project or add to specific files only.

  1. Press `Ctrl+Alt+S` to open settings and then select Editor | Copyright | Copyright Profiles. 

To configure the default profile for all newly created projects, select File | New Projects Setup | Settings for New Projects and go to Editor | Copyright | Copyright Profiles.

  2. Click ![Add](https://resources.jetbrains.com/help/img/idea/2025.3/app.expui.general.add.svg) and name the new profile.

  3. Select Share through VCS to place this profile in the .idea folder and share it with your team or deselect the checkbox to keep this profile locally and make it available in all projects.

  4. Enter the copyright notice text.

You can enter plain text or configure a Velocity template. For the template, use [variables](#variables), and click Validate to make sure that it is configured correctly.

![Configuring a copyright profile](https://resources.jetbrains.com/help/img/idea/2025.3/copyright_profile_sample.png)



Once the profile is configured, you can [select the scope of files](#assign-profile-to-scope) to which you want to add the text or [set this profile as the default profile](#default) for all files in the project that are not included in any scope.

### Copyright variables

Currently, the following variables are available in the Velocity context:

Name| Type| Comment  
---|---|---  
`$today`| `DateInfo`| The current date and time.  
`$file.fileName`| `String`| The name of the currently opened file where the notice is to be generated.  
`$file.pathName`| `String`| The complete path and name of the currently opened file where the notice is to be generated.  
`$file.className`| `String`| The name of the currently opened Java file where the notice is to be generated.  
`$file.qualifiedClassName`| `String`| The fully qualified name of the currently opened file where the notice is to be generated.  
`$file.lastModified`| `DateInfo`| The date and time when the current file was last changed.  
`$project.name`| `String`| The name of the current project.  
`$module.name`| `String`| The name of the current module.  
`$username`| `String`| The name of the current user.  
`DateInfo` has the following properties:  
`year`| `int`| The current year.  
`month`| `int`| The current month (1-12).  
`day`| `int`| The current date of month (1-31).  
`hour`| `int`| The current hour (0-11).  
`hour24`| `int`| The current hour (0-23).  
`minute`| `int`| The current minute of the hour (0-59).  
`second`| `int`| The current second of the minute (0-59).  
`DateInfo` has the following method:  
`format(String format)`| `String`| Date and time formats that are specified by date and time pattern strings. See java.text.SimpleDateFormat format options.  
  
### Examples of the copyright template text

Example 1:

Copyright (c) $today.year $username File: $file.fileName Project: $project.name Created on: $today.format("yyyy-MM-dd HH:mm") Last modified: $file.lastModified.format("yyyy-MM-dd HH:mm") 

/* * Copyright (c) 2025 jetbrains * File: Alphabet.java * Project: Samples * Created on: 2025-05-26 15:18 * Last modified: 2025-01-27 13:14 */ 

Example 2:

Copyright © $today.year JetBrains. All rights reserved. Project: $project.name Module: $module.name Author: $username Created on: $today.format("yyyy-MM-dd HH:mm:ss") File path: $file.pathName Last Edit: $file.lastModified.format("yyyy-MM-dd HH:mm:ss") 

/* * Copyright © 2025 JetBrains. All rights reserved. * * Project: Samples * Module: Samples * Author: jetbrains * Created on: 2025-05-26 15:23:13 * File path: /Users/jetbrains/Projects/Samples/src/Alphabet.java * Last Edit: 2025-05-26 15:22:44 */ 

Example 3:

Copyright © $today.year $username <$username@jetbrains.com> This file is part of the $project.name project. Licensed under the Apache License, Version 2.0 (the "License"); you may not use this file except in compliance with the License. You may obtain a copy of the License at http://www.apache.org/licenses/LICENSE-2.0 File: $file.qualifiedClassName Last Updated: $file.lastModified.format("yyyy-MM-dd HH:mm:ss") 

/* * Copyright © 2025 jetbrains <jetbrains@jetbrains.com> * * This file is part of the Samples project. * * Licensed under the Apache License, Version 2.0 (the "License"); * you may not use this file except in compliance with the License. * You may obtain a copy of the License at * * http://www.apache.org/licenses/LICENSE-2.0 * * File: Alphabet * Last Updated: 2025-05-26 15:25:49 */ 

### Dates in the copyright template

By default, the copyright template contains two years: the original year that and the current year.

If you insert a new copyright notice, the original year is going to match the current year, so only one year is going to be added (for example, `2021`). The next year, when you update your copyright, you will be able to regenerate the notice, so that the original year is going to appear alongside the current year (`2021 – 2022`). This way you don't have to add the year manually every time you update the copyright.

In the template, the original year is pulled with the `$originalComment.match("Copyright \(c\) (\d+)", 1, "-")` code, and the current year is inserted with `$today.year`. Learn more from the [source code on GitHub](https://github.com/JetBrains/intellij-community/blob/cb3d161687f1306eda1106d2ea98a6407cc17bb6/plugins/copyright/src/com/maddyhome/idea/copyright/pattern/CommentInfo.java).

![Copyright template in settings](https://resources.jetbrains.com/help/img/idea/2025.3/copyright-template.png)

Note that the year is going to update correctly if the format of the new copyright matches the format of the previous copyright in the template. So, make sure to edit the part of the template that pulls the year from files so that it matches the format of the original copyright.

For example, if your original notice was `Copyright 2019-2021 MongoDB, Inc.`, remove the copyright sign `(c)` from the template: `$originalComment.match("Copyright (\d+)", 1, "-")`.

### Assign a profile to a scope of files

Select the [scope](configuring-scopes-and-file-colors.html) of files to which you want to add the configured copyright text:

  1. Press `Ctrl+Alt+S` to open settings and then select Editor | Copyright.

  2. Click ![Add](https://resources.jetbrains.com/help/img/idea/2025.3/app.expui.general.add.svg) (or press `Alt+Insert`), and select an existing shared [scope](configuring-scopes-and-file-colors.html) from the list.

You can define a new scope if necessary. Click the Select Scopes to add scopes or modify existing ones link in the lower part of the page.

  3. From the Copyright list, select the profile that you want to link with the scope.

  4. Apply the changes and close the dialog.

![Associating a profile with a scope](https://resources.jetbrains.com/help/img/idea/2025.3/copyright_dialog.png)



After that, you can [add the copyright](#paste-copyright) to the necessary files.

### Set the default copyright profile

The settings of the default profile will be applied to files that are not explicitly included in any scope covered by a profile.

  1. Press `Ctrl+Alt+S` to open settings and then select Editor | Copyright.

  2. From the Default project copyright list, select the profile you want to use as the default profile.

  3. Apply the changes and close the dialog.

After that, you can [add the copyright](#paste-copyright) to the necessary files.




### Configure the copyright text format

By default, the IDE pastes a block comment before other comments with a prefix in each line and adds a blank line after the block.

![copyright notice in the default format](https://resources.jetbrains.com/help/img/idea/2025.3/copyright-default-format.png)

You can change the default format for all files or for each file type separately:

  1. Press `Ctrl+Alt+S` to open settings and then select Editor | Copyright | Formatting.

  2. On this page, you can configure the formatting for all types of files.

To change the formatting for a specific file type, select it under the Formatting node.

  3. Configure the formatting options. Use the preview section to make sure that the new formatting looks as intended.

![Changing the formatting for copyright notice](https://resources.jetbrains.com/help/img/idea/2025.3/ij-copyright-formatting-settings.png)



### Import a copyright profile

If you want to use a profile in another project, copy the .xml file with the profile settings to a different location and then import it:

  1. Press `Ctrl+Alt+S` to open settings and then select Editor | Copyright | Copyright Profiles.

  2. Click ![Import Profile](https://resources.jetbrains.com/help/img/idea/2025.3/app.expui.general.import.svg) and in the dialog that opens, select the .xml file containing the profile that you want to use.

  3. Change the name of the profile if necessary and click OK.

If the settings are imported successfully, you will see a confirmation popup.

![Popup confirming that copyright profile is imported](https://resources.jetbrains.com/help/img/idea/2025.3/import_copyright_profile.png)


