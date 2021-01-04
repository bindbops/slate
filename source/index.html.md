---
title: Bindbops API Reference

language_tabs: # must be one of https://git.io/vQNgJ
  - shell

toc_footers:
  - <a href='https://console.bindbops.com'>Sign Up for a Developer Key</a>
  - <a href='https://github.com/slatedocs/slate'>Documentation Powered by Slate</a>

includes:
  #- errors

search: true

code_clipboard: true
---

# Introduction

Welcome to the Bindbops API! You can use our API to access Bindbops API endpoints, which can get information on your assets in our database.

You can use any REST API client to access the endpoints.

# Authentication

Authentication is made using the API key generated in the settings of your account.

<aside class="notice">
You must replace <code>secret_key</code> in the examples with your personal API key.
</aside>

# Assets

## Get All Assets

```shell
curl "https://api.bindbops.com/v1/assets?key=secret_key"
```

> The above command returns JSON structured like this:

```json
[
  {
    "hasLocation": false,
    "_id": "5fd7ffb663f8e0000aa58a6f",
    "model": "FDQ200B8V3B9",
    "sn": "5611128",
    "category": "hvac",
    "type": "696e646f6f722073706c6974",
    "properties": [
      {
        "net weight": "89 Kg"
      }
    ]
  },
  {
    "hasLocation": false,
    "_id": "5fd8004463f8e0000aa58a74",
    "model": "FTX25J3V1B",
    "sn": "J021466",
    "category": "hvac",
    "type": "696e646f6f722073706c6974",
    "properties": [
      {
        "manufactured by": "Daikin"
      }
    ],
    "installationProperties": [
      {
        "building": "Supermarket 1"
      }
    ]
  },
  {
    "hasLocation": true,
    "_id": "5fd861d977a026000aec4abd",
    "model": "НP29-653-3Μ",
    "sn": "5805F06962",
    "category": "hvac",
    "type": {
      "name": "outdoor split"
    },
    "installationProperties": [
      {
        "building": "Mall"
      }
    ],
    "lat": 38.099768752582264,
    "lon": 23.80085022753869
  }
]
```

This endpoint retrieves all assets.

### HTTP Request

`GET https://api.bindbops.com/v1/assets`

### Query Parameters

Parameter | Description
--------- | -----------
key | Your personal API key
