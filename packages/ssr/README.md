---
title: SSR
---

## renderStatic

Function that takes the HTML of a page (as a string) and returns:

- `html`: (type: `string`) original HTML that was passed in
- `ids`: (type: `Array<string>`) array of ids (class names referencing styles
  created by Emotion)
- `css`: (type: `string`) CSS generated by Emotion from the static HTML string
  that was passed to it
