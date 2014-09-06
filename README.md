## Craft URL2PNG
Lets you embed screenshots of webpages via the URL2PNG API.

## Installation
* Place the **url2png** folder inside your **craft/plugins** folder
* Go to **settings/plugins** and install URL2PNG.
* Get your API key and secret from [url2png.com](https://www.url2png.com/)
* Add the key/secret under URL2PNG settings

## Usage
```twig
{{ craft.url2png.img({
            url: 'http://buildwithcraft.com',
            width: 500
}) | raw }}́
``

## Options
| Name                     | Description                                                          | Default  |
| -------------            | : ------------------------------------------------------------------ | ------ : |
| url                      | The url of the webpage you want to fetch                             ||
| thumbnail_max_width      | Constrain screenshot based on width. i.e. 500                        | 1:1 |
| viewport                 | Set viewport dimensions, adjust to your hearts content. i.e. 500x500 | 1480x1037 |
| fullpage                 | Will attempt to capture entire document canvas.                      | false |
| unique                   | Forces a fresh screenshot by varying this value. i.e. a timestamp.   ||
| user_agent               | Pass a custom user user agent                                        ||
| accept_languages         | Override the default HTTP Accept-Language header.                    | en-US,en;q=0.8 |
| custom_css_url           | Fetches a CSS stylesheet and injects it.                             ||
| say_cheese               | Delay screenshot until <div id='url2png-cheese'></div> is available. ||
| ttl                      | Set the TTL or "time to live" value for a screenshot in seconds. Defaults to 2592000 (30 days) ||
| alt                      | Sets the alt attribute                                               ||
| class                    | Sets the class attribute                                             ||
| width                    | Sets the width attribute                                             ||
| height                   | Sets the height attribute                                            ||