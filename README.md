<h3 align="center">
  Sanity Note Fields
</h3>
<p align="center">
  <strong>✨ Display inline notes in your schemas ✨</strong>
  Now Ready for Sanity Studio V3
</p>

![sanity-note-field](https://user-images.githubusercontent.com/737188/110528285-fcad1600-80e5-11eb-9551-1809cb8c42a3.png)

## Install

Run the following command in your studio folder using the Sanity CLI:

```sh
npm i sanity-plugin-note-field
```

## Usage

Add it to your Sanity config `new in V3`.

```js
import { note } from 'sanity-plugin-note-field'

export default createConfig([
	{
		name: 'default',
		title: '',
		projectId: '',
		dataset: '',
		basePath: '',
		plugins: [
			note()
		],
		schema: {
			types: schemaTypes
		}
	}
])
```

Use it in your schema types:

```js
{
  name: 'note',
  type: 'note',
  options: {
    message: 'Your custom Message...'
  }
}
```

## Options

When using an HTML message in Typescript ensure you're in a .tsx file.
You can also customize the color, add an icon and/or headline:

```js
import React from 'react'

...

{
  name: 'gridNote2',
  type: 'note',
  options: {
    icon: FiAlertCircle,
    headline: 'Hold up!',
    message: <>A custom HTML message: <a href="#0" target="_blank">click here</a></>,
    tone: 'caution'
  }
}
```

| Name     | Type      | Default   | Description                                                    |
| -------- | --------- | --------- | -------------------------------------------------------------- | 
| icon     | Component | `null`    | Specify an Icon Component, just as you would for your schemas  |
| headline | string    | `null`    | Displays a headline above your note message                    |
| message  | string    | `null`    | Required. Your note message (accepts HTML)                     |
| tone     | string    | `primary` | Color style for your note, based on the Sanity UI Card options. <br />Values: `default` `transparent` `positive` `caution` `critical` `brand` |



## License

### MIT
> [nickdimatteo.com](https://nickdimatteo.com) &nbsp;&middot;&nbsp;
> Github [@ndimatteo](https://github.com/ndimatteo) &nbsp;&middot;&nbsp;
> Github [@svey](https://github.com/svey-xyz) &nbsp;&middot;&nbsp;
> Instagram [@ndimatteo](https://instagram.com/ndimatteo)
