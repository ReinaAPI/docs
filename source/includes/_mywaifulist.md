# MyWaifuList

## Random

```js
const { get } = require('axios').default
get('https://reina-api.vercel.app/api/mwl/random').then((res) => console.log(res)).catch((err) => console.log(err))
```

> The response schema would be like this:

```JSON
{
    "status": 200,
    "error": false,
    "message": "Success",
    "data": {
        "name": "Rito Sudou",
        "gender": "Female",
        "likes": {
            "count": 9,
            "rank": 22608
        },
        "trash": {
            "count": 3,
            "rank": 18460
        },
        "image": "https://thicc.mywaifulist.moe/waifus/6865/26579d094b7569696a46e14802608e4b65af340c7150bd1ef2866524ff6c7fa6_thumb.jpeg",
        "slug": "rito-sudou",
        "tags": [],
        "isVTuber": false,
        "originalName": "須藤 りと",
        "romajiName": null,
        "appearances": [
            {
                "name": "Urahara",
                "slug": "urahara",
                "image": null,
                "description": "",
                "url": "https://mywaifulist.moe/waifu/urahara"
            }
        ],
        "origin": null,
        "age": null,
        "birthday": null,
        "height": null,
        "weight": null,
        "bloodType": null,
        "bust": null,
        "waist": null,
        "hip": null,
        "popularityRank": 22779,
        "description": "No biography written.",
        "url": "https://mywaifulist.moe/waifu/rito-sudou"
    }
}
```