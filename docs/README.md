## This documentation site is under construction
Please excuse the mess as we get the docs site set up.
The files for the Documentation site for CrankShaft will be in /docs/ and hosted by github pages.
If you'd like to contribute [here are all of the Issues related to the docs](https://github.com/TheWebTech/CrankShaft/projects/2).

**CrankShaft is not yet stable, we do not advise using it for a production website. With your help though we can get it there!**


## How to use CrankShaft
CrankShaft was designed to be downloaded to your computer unzipped, and then using [HubSpot's FTP](https://designers.hubspot.com/docs/tools/hubspot-ftp) uploaded to your HubSpot portal. 

The file structure looks a bit like this:
```
CrankShaft
├── code/
│   ├── cs/
│   │   ├── cs-defaults.css
│   │   └── cs-grid.css
│   ├── css/
│   │   ├── theme-module-customizations.css
│   │   └── theme.css
│   ├── hubl/
│   │   ├── theme-macros.css
│   │   └── theme-variables.css
│   ├── js/
│   │   └── theme.js
├── globals/
│   ├── global-groups/
│   └── global-modules/
├── modules/
│   └── dependencies/
└── templates/
    ├── blog/
    ├── page/
    └── system/
```

### Set your Theme settings
Once uploaded go into CrankShaft/code/hubl/theme-variables.css 

This is where you set all of your sites settings using HubL variables. Turn on and off features like the CrankShaft Grid. We added comments to the code to keep it clear what does what. Some features add CSS and/or JS. These variables will enable/disable the code regardless of it's type meaning you're only loading what you want to load.

### Styling your site
CrankShaft was designed to enforce HubSpot development best practices and encourage Templates, Custom Modules, and Themes to be built site agnostically. A more in-depth explanation of what this means will be added, but the basic jist: 
* Custom modules should not depend on the template's styles to function. This makes modules able to work even after a site redesign. This also makes these modules perfect for the [marketplace](https://marketplace.hubspot.com/products) or [HubSpot Code Gallery](https://designers.hubspot.com/code-gallery)
* Templates should not contain files required for custom module's to function. This prevents unnecessary code from loading if said modules are not even in the page.

#### Template Styles
Navigate to CrankShaft/code/css/theme.css
This is your site's stylesheet. Put all of your template specific CSS here.

#### Custom Module Theming
Custom Modules on CrankShaft are designed to be site agnostic. Only Styles required for the functionality of the module should be included in the custom module itself. Any colors and flair specific to modules in this theme should be done in CrankShaft/code/css/theme-module-customizations.css
