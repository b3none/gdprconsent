# GDPR Consent
A super flexible GDPR consent solution that, if implemented correctly, will make your site GDPR compliant.

# Installation
To install this project you can simply include the following code before all other scripts get loaded. If you do not do this then your site will not be able to be fully GDPR compliant as we cannot prevent other scripts from executing.
```html
<!-- GDPR Consent -->
<script>
    // TODO: Implement config - https://github.com/b3none/gdprconsent#customisable-settings
    window.gdprconsent = {};
</script>
<script src="https://somecdn.com/"></script>

<!-- Other scripts below this mark -->
```

OR

If the use of CDNs really isn't your style then please download the [latest release](https://github.com/b3none/gdprconsent/releases/latest) and replace the CDN urls with your own hosted version.

# Customisable settings
This project allows you to specify custom settings.
To declare these settings you need to put a script tag above the library include containing the following:
```html
<script>
  window.gdprconsent = {
    sidebarBackground: "<ANY_CSS_COLOUR_VALUE>",
    sidebarTitleTextColour: "<ANY_CSS_COLOUR_VALUE>",
    services: [
      {
        storage_key: '<ANY_KEY_YOU_WANT>',
        title: '<TITLE_IN_SIDEBAR>',
        disable: function() {
          // Callback used to disable the functionality
        },
        enable: function() {
          // Callback to enable the functionality
        },
      }
    ]
  };
</script>
```

