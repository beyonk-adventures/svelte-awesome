# Svelte-Awesome
[![Build Status](https://semaphoreci.com/api/v1/robbrazier/svelte-awesome/branches/master/shields_badge.svg)](https://semaphoreci.com/robbrazier/svelte-awesome)
[![npm](https://img.shields.io/npm/v/svelte-awesome.svg)](https://www.npmjs.com/package/svelte-awesome)
[![Code Climate](https://img.shields.io/codeclimate/maintainability/RobBrazier/svelte-awesome.svg)](https://codeclimate.com/github/RobBrazier/svelte-awesome/maintainability)
[![Code Climate](https://img.shields.io/codeclimate/c/RobBrazier/svelte-awesome.svg)](https://codeclimate.com/github/RobBrazier/svelte-awesome/test_coverage)
[![semantic-release](https://img.shields.io/badge/%F0%9F%93%A6%F0%9F%9A%80-semantic--release-e10079.svg)](https://github.com/semantic-release/semantic-release)
 [![PRs Welcome](https://img.shields.io/badge/PRs-welcome-brightgreen.svg)](http://makeapullrequest.com)

> Awesome SVG icon component for Svelte JS, built with Font Awesome icons. Based on [Justineo/vue-awesome][vue-awesome]

Svelte-Awesome is built upon [Font-Awesome][font-awesome] `v4.7.0`

## This version

This version adapts the original `svelte-awesome` library to not import *all* the icons at once, to save space in your browser bundle. This means you need to import the icons individually and use the `data=` attribute.

## Installation
### NPM
```
$ npm install --save @beyonk/svelte-awesome
```

## Usage

```js
  import Icon from '@beyonk/svelte-awesome/src/components/Icon.html'
  import beer from '@beyonk/svelte-awesome/src/icons/beer'
  
  export default {
    data () {
      return {
        beer
      }
    },

    components: {
      Icon
    }
  }
```

```html
<!-- basic -->
<Icon data="{beer}"></Icon>

<!-- with options -->
<Icon data="{refresh}" scale="2"></Icon>
<Icon data="{comment}" flip="horizontal"></Icon>
<Icon data="{code-fork}" label="Forked Repository"></Icon>

<!-- stacked icons [WIP] -->
<Icon label="No Photos">
  <Icon data="{camera}"></Icon>
  <Icon data="{ban}" scale="2" class="alert"></Icon>
</Icon>
```
