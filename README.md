# &lt;link is="puppet-redirect"&gt;

> Custom Element that redirects to a new URL when an attribute is changed. It can be configured to work using window location or History API.

## Demo

[Check it live!](http://PuppetJs.github.io/puppet-redirect)

## Install

Install the component using [Bower](http://bower.io/):

```sh
$ bower install puppet-redirect --save
```

Or [download as ZIP](https://github.com/PuppetJs/puppet-redirect/archive/master.zip).

## Usage

1. Import Web Components' polyfill, if needed:

    ```html
    <script src="bower_components/webcomponentsjs/webcomponents.js"></script>
    ```

2. Import Custom Element:

    ```html
    <link rel="import" href="bower_components/puppet-redirect/puppet-redirect.html">
    ```

3. Start using it!

    ```html
    <link is="puppet-redirect" url=""></puppet-redirect>
    ```

## Attributes

Attribute      | Options            | Default  | Description
---            | ---                | ---      | ---
`url`          | *String*           |          | Destination URL
`url`          | `current`          |          | If a string `"current"` is provided as the URL, the component reloads the page
`history`      |                    |          | If attribute `history` is present, the History API `pushState` is used instead of `window.location`
`target`       | *String*           | `_self`  | Target where to open the link. Use `"_blank"` to open in new tab

## Events

Name                       | Details             | Bubbles  | Description
---                        | ---                 | ---      | ---
`puppet-redirect-pushstate`| `{url: "/new/path"}` |   yes    | Triggers every tie `history.state` is changed by the element. This event is being listened by PuppetJs, and triggers updating its state.

## Methods

Name       | Parameters     | Returns                            | Description
---        | ---            | ---                                | ---
`redirect` | _{String}_ url | _{String}_ exact redirect location | Performs redirect to given url programmatically

## Contributing

1. Fork it!
2. Create your feature branch: `git checkout -b my-new-feature`
3. Commit your changes: `git commit -m 'Add some feature'`
4. Push to the branch: `git push origin my-new-feature`
5. Submit a pull request :D

## History

For detailed changelog, check [Releases](https://github.com/PuppetJs/redirect/releases).

## License

MIT
