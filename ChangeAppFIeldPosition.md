On the Impact theme the app field is placed under the "Quantity" field. Most of the client want to place it before "Quantity" field. If the app block postionling and
manual positioning by adding the class in backend do not work then use this small JQuery to move the app field in the correct position.

### Steps:

- Log in to the app's backend section.
- Go to "Custom JS" section and add this code.
- Check the "Quatity" section's class carefully. If it is different then just replace it with the correct class name in after($('.product-info\_\_quantity-selector')).

**Use the following code:**

```js
$(".product-personalizer").after($(".product-info__quantity-selector"));
```
