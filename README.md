﻿﻿﻿﻿﻿﻿﻿﻿﻿﻿﻿archivesspace_ui===========The customizations for the ArchivesSpace Public User Interfaceneeded by  the Shelby White and Leon Levy Archives Center at the **Institute for Advanced Study**This plugin was developed against [ArchivesSpace Version 3.2.0](https://github.com/archivesspace/archivesspace/tree/v3.0.2)_Some of this work is adapted from [Harvard's PUI Plugin](https://github.com/harvard-library/aspace-hvd-pui)_.- change font families, color themes and other style sheet elements- customize of terminology and language for several screens- remove Classifications from top horizontal menu- remove repositories from top horizontal menu- remove repository in breadcrumbs- adapt the Harvard PUI's Search boxes - change internal navigation look in Collection display:  - make "collection organization" the left sidebar  - remove List of Containers; replace with Digital Materials  -  when displaying a collection's digital materials:     -  display list of digital objects in the order of the _first_ associated archival object     - synch display of individual digital object with the collection organization sidebar- remove "More about" from right sidebar of Subject display## <a name="install">Installation</a>This is a regular  [ArchivesSpace Plug-in](https://github.com/archivesspace/tech-docs/blob/master/customization/plugins.md).To install this plug-in:  Either clone this plugin, or download the latest version:   - Clone the plug-in from this [GitHub repository](https://github.com/crizzo-ias/archivesspace_ui) into the ArchivesSpace **/plugins/** directory.  - Download the [zipfile] (https://github.com/crizzo-ias/archivesspace_ui/archive/refs/heads/main.zip). Unzip the download into the **/plugins/** directory.  You will probably need to rename the top folder/directory to **archivesspace_ui**. You do not need to run the plugin initializer script.See the [Technical Documentation](techdoc.md) for information on the modifications included in this plugin.The `plugin_init.rb` script contains some settings that override any settings in the ArchivesSpace core's configuration file (`config.rb`).  If you have access to the `config.rb` file, you may wish to migrate those settings:```rubyAppConfig[:pui_hide][:repositories] = trueAppConfig[:pui_hide][:subjects] = falseAppConfig[:pui_hide][:agents] = falseAppConfig[:pui_hide][:accessions] = trueAppConfig[:pui_hide][:classifications] = trueAppConfig[:pui_branding_img] = "/assets/ias.png"AppConfig[:pui_branding_img_alt_text] = "Institute for Advanced Study"AppConfig[:pui_page_actions_print] = trueAppConfig[:pui_page_actions_cite] = trueAppConfig[:pui_page_actions_request] = trueAppConfig[:pui_page_actions_print] = true```