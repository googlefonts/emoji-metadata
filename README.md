This repository provides metadata to support UX around emoji. In particular, it describes how to construct an emoji picker with full support for skin tones. The json files describe a grid layout for an emoji picker with 9 emoji per row:

* `emoji_13_0_ordering.json` for Emoji 13.0.
* `emoji_13_1_ordering.json` for Emoji 13.1.
* `emoji_14_0_ordering.json` for Emoji 14.0.
* `emoji_15_0_ordering.json` for Emoji 15.0.
* `emoji_15_1_ordering.json` for Emoji 15.1.
* `emoji_16_0_ordering.json` for Emoji 16.0.
* `emoji_17_0_ordering.json` for Emoji 17.0.

As emoji evolves new orderings will be added. 

Demo: https://jsbin.com/kesuteh/1/edit?css,js,output

A snippet is shown annotated below:

```js
  {
  	// The is the people section
    "group": "People",
    "emoji": [
      {
      	// This is the codepoint sequence for the emoji that should show in the grid
      	// Generally the base is the most neutral version available, such as the
      	// genderless gold skintone version.
        "base": [
          128583
        ],
        // These are alternate versions, typically shown as a long-press flyout
        "alternates": [
          [
            128583
          ],
          [
            128583,
            127995
          ],
          // ...etc...
        ],
        // Emoticon(s)
        "emoticons": [
          ">:P"
        ],
        // Shortcode(s)
        "shortcodes": [
          ":smirk:"
        ],
        // Whether there is an animated version for the base emoji
        "animated": true,
        // [15.1]: whether the alternates include directional emoji
        "directional": false
      },
```

Here is what the people section could look like:

![People](images/people.png)

Here are the alternates for Santa, as might be shown on long-press for the base Santa:

![People](images/santa-alternates.png)

The https://github.com/googlefonts/noto-emoji repository provides Google's Emoji.

