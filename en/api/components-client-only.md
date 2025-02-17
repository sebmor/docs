---
title: "API: The <client-only> Component"
description: Render a component only on client-side, and display a placeholder text on server-side.
---

# The &lt;client-only&gt; Component

> This component is used to purposely render a component only on client-side.


<div class="Alert Alert--orange">

**Warning:** If you are using a version of Nuxt < `v2.9.0`, use `<no-ssr>` instead of `<client-only>`

</div>


**Props**:
- placeholder: `string`
  - Use a text as placeholder until `<client-only />` is mounted on client-side.

```html
<template>
  <div>
    <sidebar />
    <client-only placeholder="Loading...">
      <!-- this component will only be rendered on client-side -->
      <comments />
    </client-side>
  </div>
</template>
```

**Slots**:

- placeholder:
  - Use a slot as placeholder until `<client-only />` is mounted on client-side.
 
 ```html
<template>
  <div>
    <sidebar />
    <client-only>
      <!-- this component will only be rendered on client-side -->
      <comments />
  
      <!-- loading indicator, rendered on server-side -->
      <comments-placeholder slot="placeholder" />
    </client-only>
  </div>
</template>
```

This component is imported from [egoist/vue-client-only](https://github.com/egoist/vue-client-only). Thanks [@egoist](https://github.com/egoist)!
