# Flip Login

Default Login page which flips(rotates) to a sign up for a new user.

## Demo

```
npm i flipauthentication
```

## Installing

Download the package from npm.
```
npm i flipauthentication
```

###  Module
Import the component in your file and use.

```
<template>
  <flip-login></flip-login>
</template>
```

```
import FlipLogin from 'flipauthentication';
export default {
  components: {
    'flip-login': FlipLogin
  }
}
```

###  Usage
Use this template

```
<flip-login>
  <div slot="front">
    front
  </div>
  <div slot="back">
    back
  </div>
</flip-login>
```
You can flip the component whenever you want by changing the value of flipit to false/true. An example of the usage of this component
is given in src/pages/fliploginimplementation.vue
```
<flip-login :flipit="flipit"></flip-login>
```
You have to define the width of the component.
```
<flip-login  width= "40%"></flip-login>
```

