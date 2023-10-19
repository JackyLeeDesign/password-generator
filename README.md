
# Vue Password Generator

This is a simple password generator component in VueJS.

## Installation

1. Copy the `passwordGenerator.vue` file into your project's `src/components` directory.
2. Import the `passwordGenerator` component in VueJS from `src/components/passwordGenerator.vue`.

```javascript
import passwordGenerator from './components/passwordGenerator.vue'
```

3. Use the component in your Vue instance or component.

```javascript
new Vue({
  el: '#app',
  components: {
    'password-generator': passwordGenerator
  },
});
```

## Usage

```html
<password-generator></password-generator>
```

Once the button is clicked, a new 10-character password is visually created. You can further customize this by changing the length and charset variables in the `generatePassword` function.
