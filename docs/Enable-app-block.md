---
layout: default
title: Enable app block
---

# Enable App Block

- [Introduction](#introduction)
- [Steps](#steps)
  - [Add Block Type](#add-block-type)
  - [Create JSON File](#create-json-file)

<a name="introduction"></a>

## Introduction

If one user uses the older version of Shopify Themes, then he will be able to enable `App Block` for any section of his theme with the below steps.

<a name="steps"></a>

## Steps

- Add Block Type in specific liquid file
- Create a JSON file under template folder

<a name="add-block-type"></a>

## Add Block Type

Suppose, you want to add an App Block in Home Page `Featured Product` Section. Under `{\% schema \%}` add the below code blocks

```json
"blocks": [
    {
        "type": "@app"
    }
]
```

<a name="create-json-file"></a>

## Create JSON File

If you want to enable App Block for a theme, you must have a JSON file under `template` folder. Suppose, we want to modify the homepage, then we need a file `index.json`. Add the below code for homepage

```json
{
  "sections": {},
  "order": []
}
```

N.B: If you have any file like `index.liquid`, remove that and create a new one `index.json`

Hope it will work.
