# Vue3-ArtPlayer
ArtPlayer Module for Vuejs 3.0

## How to use it?
### Step 1 - Install ArtPlayer from npm
```
npm install artplayer
```

### Step 2 - Import this vue module
Here is a example

- For VitePress:
```javascript
// .vitepress/theme/index.ts

import { h } from 'vue'
import Theme from 'vitepress/theme'
import './style.css'

import Player from '../../components/Player.vue'; 

export default {
  extends: Theme,
  Layout: () => {
    return h(Theme.Layout, null, {
      // https://vitepress.dev/guide/extending-default-theme#layout-slots
    })
  },
  enhanceApp({ app, router, siteData }) {
    // ...
    app.component('Player', Player)
  }
}
```

### Step 3 - Use it
Here is a example

```html
<Player src="video link" />
```