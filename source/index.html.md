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

# Personal Accounts

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
    "assetProperties": [
      {
        "net weight": "89 Kg"
      }
    ],
    "assetType": "indoor split",
    "uuid": "e45abd1e-06d0-40d6-8cae-a5f31b9bf37d",
    "id": "5fd7ffb663f8e0000aa58a6f"
  },
  {
    "hasLocation": false,
    "_id": "5fd8004463f8e0000aa58a74",
    "model": "FTX25J3V1B",
    "sn": "J021466",
    "category": "hvac",
    "installationProperties": [
      {
        "building": "Mall"
      }
    ],
    "assetProperties": [
      {
        "manufactured by": "Daikin"
      }
    ],
    "assetType": "indoor split",
    "uuid": "f797954d-8ee3-4b71-9be8-46503a8b3033",
    "id": "5fd8004463f8e0000aa58a74"
  }
]
```

This endpoint retrieves all assets.

### HTTP Request

`GET https://api.bindbops.com/v1/assets`

### Query Parameters

| Parameter | Description           |
| --------- | --------------------- |
| key       | Your personal API key |

## Get A Specific Asset

```shell
curl "https://api.bindbops.com/v1/assets/e35abd1e-06d0-40d6-8cae-a5f31b9bf37d?key=secret_key"
```

> The above command returns JSON structured like this:

```json
{
  "hasLocation": false,
  "_id": "5fd7ffb663f8e0000aa58a6f",
  "model": "FDQ200B8V3B9",
  "sn": "5611128",
  "category": "hvac",
  "assetProperties": [
    {
      "net weight": "89 Kg"
    }
  ],
  "assetType": "indoor split",
  "uuid": "e45abd1e-06d0-40d6-8cae-a5f31b9bf37d",
  "id": "5fd7ffb663f8e0000aa58a6f"
}
```

This endpoint retrieves a specific asset given its UUID.

### HTTP Request

`GET https://api.bindbops.com/v1/assets/<UUID>`

### Path Parameters

| Parameter | Description           |
| --------- | --------------------- |
| UUID      | The UUID of the asset |

### Query Parameters

| Parameter | Description           |
| --------- | --------------------- |
| key       | Your personal API key |
