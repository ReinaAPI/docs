# MyWaifuList

## Random

```js
const { get } = require('axios').default
get('https://reina-api.vercel.app/api/mwl/random')
  .then((res) => console.log(res))
  .catch((err) => console.log(err))
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

This endpoint gets a random Waifu/Husbando from MyWaifuList and returns the information of the character.

### HTTP Request
`GET https://reina-api.vercel.app/api/mwl/random`

### Query Parameters
Parameter | Required | Description
--------- | -------- | -----------
type        | false     | Type of the character (waifu/husbando)

## Character Search By Slug

```js
const { get } = require('axios').default
const slug = 'kirisaki-chitoge'
get(`https://reina-api.vercel.app/api/mwl/character/slug/${slug}`)
  .then((res) => console.log(res))
  .catch((err) => console.log(err))
```

> The response schema would be like this:

```JSON
{
    "status": 200,
    "error": false,
    "message": "Success",
    "data": {
        "name": "Kirisaki Chitoge",
        "gender": "Female",
        "likes": {
            "count": 1987,
            "rank": 103
        },
        "trash": {
            "count": 640,
            "rank": 61
        },
        "image": "https://thicc.mywaifulist.moe/waifus/132/b5aae2947b7f7419d9f332f07a275db6784d9100bd003fc2a4fd4f382790c7b4_thumb.png",
        "slug": "kirisaki-chitoge",
        "tags": [
            "blonde hair"
        ],
        "isVTuber": false,
        "originalName": "桐崎 千棘, Ichijō Chitoge",
        "romajiName": null,
        "appearances": [
            {
                "name": "Nisekoi: False Love",
                "slug": "nisekoi-false-love",
                "image": "https://thicc.mywaifulist.moe/series/94/4deb14f4a2ab2b7f04a95db39f8ba2c2a2d5a20ba73988c79f1c0195ccd0066c_thumbnail.jpeg",
                "description": "Raku Ichijou, a first-year student at Bonyari High School, is the sole heir to an intimidating yakuza family. Ten years ago, Raku made a promise to his childhood friend. Now, all he has to go on is a pendant with a lock, which can only be unlocked with the key which the girl took with her when they parted.\r\n\r\nNow, years later, Raku has grown into a typical teenager, and all he wants is to remain as uninvolved in his yakuza background as possible while spending his school days alongside his middle school crush Kosaki Onodera. However, when the American Bee Hive Gang invades his family's turf, Raku's idyllic romantic dreams are sent for a toss as he is dragged into a frustrating conflict: Raku is to pretend that he is in a romantic relationship with Chitoge Kirisaki, the beautiful daughter of the Bee Hive's chief, so as to reduce the friction between the two groups. Unfortunately, reality could not be farther from this whopping lie—Raku and Chitoge fall in hate at first sight, as the girl is convinced he is a pathetic pushover, and in Raku's eyes, Chitoge is about as attractive as a savage gorilla. \r\n\r\nNisekoi follows the daily antics of this mismatched couple who have been forced to get along for the sake of maintaining the city's peace. With many more girls popping up his life, all involved with Raku's past somehow, his search for the girl who holds his heart and his promise leads him in more unexpected directions than he expects.\r\n\r\n[Written by MAL Rewrite]",
                "url": "https://mywaifulist.moe/waifu/nisekoi-false-love"
            }
        ],
        "origin": "America",
        "age": null,
        "birthday": "June 7th",
        "height": "160.00 cm",
        "weight": "46.00 kg",
        "bloodType": "B",
        "bust": null,
        "waist": null,
        "hip": null,
        "popularityRank": 78,
        "description": "Chitoge Kirisaki originally lived with her father in the United States until she transferred to another school in Japan — where she is now currently residing in. With her father being the leader of the infamous Bee Hive Gang, it has effectively caused multiple problems for Chitoge during her childhood as she was unable to make friends very easily due to being under constant watch by her bodyguard, Claude. However, when she was young, she met and befriended a hitwoman in-training, Tsugumi, who, to the current day, she is still friends with. Chitoge also seems to have a few problems with her mother, who has very high expectations for her, making Chitoge somewhat of a perfectionist who excels in both sports and academics.\n\nAt some point during her childhood, Chitoge had become close friends with Raku, Kosaki, Marika, and Yui through a summer vacation in Tegu Plateau. Chitoge and Kosaki had the strongest relationship between the whole group and both shared a love for a picture book Chitoge owned which was about a princess and prince falling in love and reuniting in heaven. Chitoge decided to give Kosaki the picture book as a sign of friendship and remembrance when they can longer see each other.",
        "url": "https://mywaifulist.moe/waifu/kirisaki-chitoge"
    }
}
```

This endpoint returns the character's information of the given character's slug from MyWaifuList.

### HTTP Request
`GET https://reina-api.vercel.app/api/mwl/character/slug/:slug`

### Path Parameters
Parameter | Required | Description
--------- | -------- | -----------
slug     | true     | Slug of the character from MyWaifuList

## Character Search by Name

```js
const { get } = require('axios').default
const query = 'Reina Izumi'
get(`https://reina-api.vercel.app/api/mwl/character/search?q=${query}`)
  .then((res) => console.log(res))
  .catch((err) => console.log(err))
```

> The response schema would be like this:

```JSON
{
    "status": 200,
    "error": false,
    "message": "Success",
    "pagination": {
        "currentPage": 1,
        "totalPages": 1,
        "hasNextPage": false
    },
    "data": [
        {
            "name": "Reina Izumi",
            "slug": "reina-izumi",
            "originalName": "和泉 玲奈",
            "appearances": [
                {
                    "name": "Myriad Colors Phantom World",
                    "originalName": "無彩限のファントム・ワールド",
                    "slug": "myriad-colors-phantom-world",
                    "url": "https://mywaifulist.moe/series/myriad-colors-phantom-world"
                }
            ],
            "image": "https://thicc.mywaifulist.moe/waifus/1232/6bd02a8775a3c1fe7632fc15545fab102af034df9a33d23e6d4fd58d15b28911_thumb.jpg",
            "url": "https://mywaifulist.moe/waifu/reina-izumi"
        }
    ]
}
```

This endpoint searches for a character by its name from MyWaifuList.

### HTTP Request
`GET https://reina-api.vercel.app/api/mwl/character/search`

### Query Parameters
Parameter | Required | Description
--------- | -------- | -----------
q        | false     | Name of the character to search
page     | false     | Page of the character search
type     | false     | Type of the character (all/husbando)