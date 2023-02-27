---
layout: default
title: Stucked add to cart
---

# Add to cart is stucked at 100%

Often we get complains from our customer that the add to cart is stucked at certain percentage. This issue can happen for servaral reasons.

We need to check few things to investigate this specific issue.

## Output format issue:

Open your browser console and check if there is any error while adding to cart. If the error is coming from our apps **canvas script** and realted to **PDF** or **FONT**, then the most possible reason is client using **"PDF Vector"** or **"SVG Vector"** as **"Output format"**. And the configuration have any custom font that have renderring issue with HTML5 Canvas.

If any fonts that have rendering issue with HTML CANVAS can interrupt the PDF Building process. In this case, client will need to change the fonts or use "PNG" as output format.

So first check by changing the **output format** to "PNG" and see if the issue get solved.

## Interrupted by other app scripts:

If the Client is using **PNG** as the **output format** and facing this issue, then the possible reason is some other app scripts interrupting our add to cart flow.

In this scenario, check the console and see if there is any error from our app or other scripts. Check if the error is add to cart process related.

Open the developer tools **Network Tab** and clear all the current scripts. While the tab is open, click on add to cart and check which scripts are running when the button is clicked. Try manually blocking other app scripts using devtools.

If you see the issue is solved by blocking other app script then we need to request the client to remove the app or script which is creating the conflict.

Here are some scripts that are previsouly reported as the cause of this issue:

- https://cdn.shopify.com/s/files/1/1538/0891/t/100/assets/carsonToolkit.js

Check if any of these scripts are available in the **Network Tab**.
