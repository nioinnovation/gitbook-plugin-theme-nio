GitBook Theming for niolabs
==============

This plugin will give your gitbooks niolabs-styling.

## How to use

Add the plugin to your book.json file.

You point the plugin to the nioinnovation GitHub repo since `theme-nio` is not currently published to npm:

```json
"plugins": [
    "theme-nio@git://github.com/nioinnovation/gitbook-plugin-theme-nio.git"
  ]
```

Note: `theme-nio` is the name to use for the plugin, the standard `gitbook-plugin` prefix will automatically be prepended to this root when you run `gitbook install` on your book.

## Configuration

### Active Location in Header
To highlight the active location of your book in the header, specify `active-location` in the `pluginsConfig` for `theme-nio`

```json
"pluginsConfig": {
    "theme-nio": {
      "active-location": "workshop"
    }
  }
```

The active class will be added to the nav item with the corresponding id: `id="nav__list--${active-location}"`. For example, the above configuration will highlight any nav item where `id="nav__list--workshop"`.

## Blocks

### Video Embed
To embed a video, use the following block in the text of your book. The "watch" link will be transformed into a div containing an iframe with an embed url. Both YouTube and Vimeo links are supported.

```text
{% video %}https://www.youtube.com/watch?v=OkfVMPjzkhE{% endvideo %}
```

### Dynamic Year
The tag
```text
{% year %}{% endyear %}
```

Will display the current year.
