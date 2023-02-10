---
layout: default
title: Globally change personalizer button text
---

In our app we can't change the text of the "Personalization" button for all products globally. If a client want to change them they need to change it one product at a time.
This below script will change the text of all of the Personalization Buttons in a store. Add this script in the theme.liquid file so this will apply to all products.

### Steps:

- Go to `theme.liquid` file and add this script.
- Change the value of "Your Text" in here cutomizeButtonText("Your Text") to client's desired text.
- Save and this change will apply on all of the Personalization Buttons.

**Use the following code:**

```js
<script type="text/javascript">
// Listen for the pplrAppInitiated custom event
window.addEventListener('pplrAppInitiated' , function(e) {
  // bulk edit customize button text
  function cutomizeButtonText(text){
  // The text you want to show on all personalization button
      let value = text;
      let btn = document.querySelector(".pplr-c-button");
      btn.textContent = value;
    };
    // Call the function and pass the value
    cutomizeButtonText("Your Text");
  });
  </script>
```

**Provided by Al Amin Khan**
