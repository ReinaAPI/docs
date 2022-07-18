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
        "nsfw": false,
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

## Get Character Details By Slug

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
        "nsfw": false,
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

## Get Waifu of the day

```js
const { get } = require('axios').default
get('https://reina-api.vercel.app/api/mwl/waifu-of-the-day')
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
        "name": "Charlotte",
        "gender": "Female",
        "likes": {
            "count": 138,
            "rank": 3713
        },
        "trash": {
            "count": 10,
            "rank": 8004
        },
        "image": "https://thicc.mywaifulist.moe/waifus/30250/c98c9d19ee63a671c5346d974934bd1dbf968485d5e8d29f0d273174da064b86_thumb.jpeg",
        "slug": "charlotte-7",
        "nsfw": false,
        "tags": [],
        "isVTuber": false,
        "originalName": "シャーロット",
        "romajiName": "Charlotte",
        "appearances": [
            {
                "name": "Fly Me to the Moon (Manga)",
                "slug": "fly-me-to-the-moon-manga",
                "image": "https://thicc.mywaifulist.moe/series/3804/b15840735762aa56a0b4716089105e0632ef7e66d8662c04ce4c263c7f969b27_thumbnail.jpeg",
                "description": "Having grown up ridiculed for his bizarre name, Nasa Yuzaki strives to be remembered for something more. Fortunately, it seems he's on the right path, ranking first in the nation's mock exams and set to enter his high school of choice.\r\n\r\nHowever, everything changes in a single night when he notices a girl across the street on his way home. Enraptured by her overwhelming cuteness, it's love at first sight for Nasa. But in his infatuated daze, he fails to notice the approaching danger speeding down the road and finds himself at death's door. Barely alive thanks to the girl's intervention, Nasa musters the courage to confess his love to her, fearing she might otherwise vanish from his life. She accepts his proposal on one condition: marriage, to which Nasa gladly accepts before passing out from his injuries. Upon waking, however, the girl is nowhere to be found.\r\n\r\nAfter recovering from his injuries, Nasa tosses his previous ambitions aside and dedicates his life to finding the girl that captured his heart, yet several years pass to no avail. But one night, when an unexpected visitor comes knocking on his door, Nasa finds himself facing a woman that would forever change his world: his wife.",
                "url": "https://mywaifulist.moe/waifu/fly-me-to-the-moon-manga"
            },
            {
                "name": "Fly Me to the Moon",
                "slug": "fly-me-to-the-moon",
                "image": "https://thicc.mywaifulist.moe/series/5229/b40d16cc1cffb4564a4798d4861d02fb2a22ceac0c62653fda7cd48e229e46f9_thumbnail.jpeg",
                "description": "Having grown up ridiculed for his bizarre name, Nasa Yuzaki strives to be remembered for something more. Fortunately, it seems he's on the right path, ranking first in the nation's mock exams and set to enter his high school of choice.\r\n\r\nHowever, everything changes in a single night when he notices a girl across the street on his way home. Enraptured by her overwhelming cuteness, it's love at first sight for Nasa. But in his infatuated daze, he fails to notice the approaching danger speeding down the road and finds himself at death's door. Barely alive thanks to the girl's intervention, Nasa musters the courage to confess his love to her, fearing she might otherwise vanish from his life. She accepts his proposal on one condition: marriage, to which Nasa gladly accepts before passing out from his injuries. Upon waking, however, the girl is nowhere to be found.\r\n\r\nAfter recovering from his injuries, Nasa tosses his previous ambitions aside and dedicates his life to finding the girl that captured his heart, yet several years pass to no avail. But one night, when an unexpected visitor comes knocking on his door, Nasa finds himself facing a woman that would forever change his world: his wife.",
                "url": "https://mywaifulist.moe/waifu/fly-me-to-the-moon"
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
        "popularityRank": 4155,
        "description": "She always wears her maid outfit while at work and has very long wavy hair.",
        "url": "https://mywaifulist.moe/waifu/charlotte-7"
    }
}
```

This endpoint returns the data for waifu of the day in MyWaifuList.

### HTTP Request
`GET https://reina-api.vercel.app/api/mwl/waifu-of-the-day`

## Get Popular Waifus

```js
const { get } = require('axios').default
get('https://reina-api.vercel.app/api/mwl/popular')
  .then((res) => console.log(res))
  .catch((err) => console.log(err))
```

> The reponse schema would be like this:

```JSON
{
    "status": 200,
    "error": false,
    "message": "Success",
    "data": {
        "title": "Most Popular Anime Waifus",
        "data": [
            {
                "rank": 1,
                "waifu": {
                    "name": "Megumin",
                    "originalName": "めぐみん",
                    "slug": "megumin-konosuba-god-s-blessing-on-this-wonderful-world",
                    "image": "https://thicc.mywaifulist.moe/waifus/319/2b9e5c31ae2168b769d64350f07526363208d7e2ca2d6b11bf4ca7bba8de9dc6_thumb.png",
                    "popularityRank": 1,
                    "likeRank": 1,
                    "trashRank": 4,
                    "url": "https://mywaifulist.moe/waifu/megumin-konosuba-god-s-blessing-on-this-wonderful-world"
                }
            },
            {
                "rank": 2,
                "waifu": {
                    "name": "Rem",
                    "originalName": "レム",
                    "slug": "rem-re-zero-starting-life-in-another-world",
                    "image": "https://thicc.mywaifulist.moe/waifus/41/5d01a3827544918e005287f16d1e7132d0b873dbb628a9d565449745c0ed60c1_thumb.jpg",
                    "popularityRank": 2,
                    "likeRank": 2,
                    "trashRank": 6,
                    "url": "https://mywaifulist.moe/waifu/rem-re-zero-starting-life-in-another-world"
                }
            },
            {
                "rank": 3,
                "waifu": {
                    "name": "Asuna Yuuki",
                    "originalName": "結城 明日奈",
                    "slug": "asuna-yuuki-sword-art-online",
                    "image": "https://thicc.mywaifulist.moe/waifus/58/c73fb4b96627b9ba3b52cc3ae051fd10e0efe87c30c026473ae9936220e6949c_thumb.jpg",
                    "popularityRank": 3,
                    "likeRank": 14,
                    "trashRank": 1,
                    "url": "https://mywaifulist.moe/waifu/asuna-yuuki-sword-art-online"
                }
            },
            {
                "rank": 4,
                "waifu": {
                    "name": "Zero Two",
                    "originalName": "ゼロツー",
                    "slug": "zero-two-darling-in-the-franxx",
                    "image": "https://thicc.mywaifulist.moe/waifus/9215/7e6b971558af535d52397df6854c3c90bb66a41c5faaa07395d0a65e4e20fead_thumb.jpeg",
                    "popularityRank": 4,
                    "likeRank": 4,
                    "trashRank": 13,
                    "url": "https://mywaifulist.moe/waifu/zero-two-darling-in-the-franxx"
                }
            },
            {
                "rank": 47,
                "waifu": {
                    "name": "Historia Reiss",
                    "originalName": "ヒストリア・レイス",
                    "slug": "historia-reiss-attack-on-titan",
                    "image": "https://thicc.mywaifulist.moe/waifus/2950/aabd70daa845cc70a9ee26eff355cd7a12be34ca727a51b8ea924421bd3f31f1_thumb.png",
                    "popularityRank": 47,
                    "likeRank": 44,
                    "trashRank": 86,
                    "url": "https://mywaifulist.moe/waifu/historia-reiss-attack-on-titan"
                }
            },
            {
                "rank": 48,
                "waifu": {
                    "name": "Wiz",
                    "originalName": "ウィズ",
                    "slug": "wiz",
                    "image": "https://thicc.mywaifulist.moe/waifus/1804/73dfaee92b1f25d94c32829dc7bb37f782b2d4e2b21afba9a511f9dad13f3726_thumb.jpg",
                    "popularityRank": 48,
                    "likeRank": 42,
                    "trashRank": 131,
                    "url": "https://mywaifulist.moe/waifu/wiz"
                }
            },
            {
                "rank": 49,
                "waifu": {
                    "name": "Tamamo-no-Mae",
                    "originalName": "玉藻の前",
                    "slug": "tamamo-no-mae-fate-extra",
                    "image": "https://thicc.mywaifulist.moe/waifus/685/584e6c3b17d316cec3b9ada0ab27d9eed4a3baaec8af09bdeb119502269878d4_thumb.jpeg",
                    "popularityRank": 49,
                    "likeRank": 49,
                    "trashRank": 68,
                    "url": "https://mywaifulist.moe/waifu/tamamo-no-mae-fate-extra"
                }
            },
            {
                "rank": 50,
                "waifu": {
                    "name": "Shino Asada",
                    "originalName": "朝田 詩乃",
                    "slug": "shino-asada-sword-art-online",
                    "image": "https://thicc.mywaifulist.moe/waifus/528/464a10e4e9e446df154b19185055c404c494caf825ec398c3bf9bc95297199c9_thumb.jpg",
                    "popularityRank": 50,
                    "likeRank": 46,
                    "trashRank": 87,
                    "url": "https://mywaifulist.moe/waifu/shino-asada-sword-art-online"
                }
            }
        ]
    }
}
```

This endpoint returns the ranking of the most popular waifus of all time in MyWaifuList.

### HTTP Request
`GET https://reina-api.vercel.app/api/mwl/popular`

## Get Best Waifus

```js
const { get } = require('axios').default
get('https://reina-api.vercel.app/api/mwl/best')
  .then((res) => console.log(res))
  .catch((err) => console.log(err))
```

> The reponse schema would be like this:

```JSON
{
    "status": 200,
    "error": false,
    "message": "Success",
    "data": {
        "title": "Best Anime Waifus",
        "data": [
            {
                "rank": 1,
                "waifu": {
                    "name": "Mizore Shirayuki",
                    "originalName": "白雪 みぞれ",
                    "slug": "mizore-shirayuki-rosario-vampire",
                    "image": "https://thicc.mywaifulist.moe/waifus/720/09eea57d6ecd06353aa75e6689a7da955ac183e5d5e26d314e2e742492b0e13b_thumb.jpg",
                    "popularityRank": 419,
                    "likeRank": 363,
                    "trashRank": 1587,
                    "url": "https://mywaifulist.moe/waifu/mizore-shirayuki-rosario-vampire"
                }
            },
            {
                "rank": 2,
                "waifu": {
                    "name": "Dr. Franken Stein",
                    "originalName": "フランケン•シュタイン",
                    "slug": "dr-franken-stein",
                    "image": "https://thicc.mywaifulist.moe/waifus/23998/fd3a43f719a3b39f5fb0273c8b98d0c6eb446d32a869e118a5d3fa51395ded0c_thumb.jpg",
                    "popularityRank": 5154,
                    "likeRank": 4402,
                    "trashRank": 16648,
                    "url": "https://mywaifulist.moe/waifu/dr-franken-stein"
                }
            },
            {
                "rank": 3,
                "waifu": {
                    "name": "Rit",
                    "originalName": "リット",
                    "slug": "rit-banished-from-the-hero-s-party-i-decided-to-live-a-quiet-life-in-the-countryside",
                    "image": "https://thicc.mywaifulist.moe/waifus/29717/358ea2d48e8b689353fe38d7913aee0c68cb4fcd5b57def1c3e0831edafdcb97_thumb.jpeg",
                    "popularityRank": 3276,
                    "likeRank": 2821,
                    "trashRank": 10124,
                    "url": "https://mywaifulist.moe/waifu/rit-banished-from-the-hero-s-party-i-decided-to-live-a-quiet-life-in-the-countryside"
                }
            },
            {
                "rank": 4,
                "waifu": {
                    "name": "Miko Yotsuya",
                    "originalName": "四谷みこ",
                    "slug": "miko-yotsuya-mieruko-chan",
                    "image": "https://thicc.mywaifulist.moe/waifus/37299/2a6a7ace7e7a1e962e587a3102d6ce667b95dd336960aab51b76f9d11f62298a_thumb.jpg",
                    "popularityRank": 615,
                    "likeRank": 535,
                    "trashRank": 2293,
                    "url": "https://mywaifulist.moe/waifu/miko-yotsuya-mieruko-chan"
                }
            }
        ]
    }
}
```

This endpoint returns the ranking of the best waifus of all time in MyWaifuList.

### HTTP Request
`GET https://reina-api.vercel.app/api/mwl/best`

## Get Popular V-Tubers

```js
const { get } = require('axios').default
get('https://reina-api.vercel.app/api/mwl/vtubers')
  .then((res) => console.log(res))
  .catch((err) => console.log(err))
```

> The reponse schema would be like this:

```JSON
{
    "status": 200,
    "error": false,
    "message": "Success",
    "data": {
        "title": "Most Popular Virtual Youtubers",
        "data": [
            {
                "rank": 1,
                "waifu": {
                    "name": "AI Kizuna",
                    "originalName": "キズナアイ",
                    "slug": "kizuna-ai-youtube",
                    "image": "https://thicc.mywaifulist.moe/waifus/1608/0cfc122410eeb4182bcc67aea3f8074e017147f855559edfc6bc6f119d39cd45_thumb.jpg",
                    "popularityRank": 189,
                    "likeRank": 166,
                    "trashRank": 358,
                    "url": "https://mywaifulist.moe/waifu/kizuna-ai-youtube"
                }
            },
            {
                "rank": 2,
                "waifu": {
                    "name": "Gura Gawr",
                    "originalName": "がうる・ぐら",
                    "slug": "gura-gawr-hololive-production",
                    "image": "https://thicc.mywaifulist.moe/waifus/32382/ff8853b7432256707ee547591a8c9023285ec9224048d1275273d87615666203_thumb.jpg",
                    "popularityRank": 219,
                    "likeRank": 224,
                    "trashRank": 273,
                    "url": "https://mywaifulist.moe/waifu/gura-gawr-hololive-production"
                }
            },
            {
                "rank": 17,
                "waifu": {
                    "name": "Subaru Oozora",
                    "originalName": "大空スバル",
                    "slug": "subaru-oozora-hololive-production",
                    "image": "https://thicc.mywaifulist.moe/waifus/28462/4ecf9001d7a0d04f1f5e222655fce6bbbd7b076cd8e92fd1d17d7e0d8cb60344_thumb.jpg",
                    "popularityRank": 811,
                    "likeRank": 695,
                    "trashRank": 2669,
                    "url": "https://mywaifulist.moe/waifu/subaru-oozora-hololive-production"
                }
            },
            {
                "rank": 18,
                "waifu": {
                    "name": "Towa Tokoyami",
                    "originalName": "常闇トワ",
                    "slug": "towa-tokoyami-hololive-production",
                    "image": "https://thicc.mywaifulist.moe/waifus/29235/3dd4aee02988ac4e2fa648b34556ddf7c7f192507e7d5bda4e7ca333207915e6_thumb.jpg",
                    "popularityRank": 894,
                    "likeRank": 774,
                    "trashRank": 3061,
                    "url": "https://mywaifulist.moe/waifu/towa-tokoyami-hololive-production"
                }
            },
            {
                "rank": 19,
                "waifu": {
                    "name": "Mio Ookami",
                    "originalName": "大神ミオ",
                    "slug": "mio-ookami-azur-lane",
                    "image": "https://thicc.mywaifulist.moe/waifus/25062/d405aad29c40629ef950b96779128c92f27aac89cd3b810a216f95b62ec872ac_thumb.png",
                    "popularityRank": 925,
                    "likeRank": 803,
                    "trashRank": 3165,
                    "url": "https://mywaifulist.moe/waifu/mio-ookami-azur-lane"
                }
            },
            {
                "rank": 20,
                "waifu": {
                    "name": "Miko Sakura",
                    "originalName": "さくらみこ",
                    "slug": "miko-sakura-hololive-production",
                    "image": "https://thicc.mywaifulist.moe/waifus/30238/5f8e8156d90a79ed01e2181353db359cf6bea5a46a6fbfdaadf3450a9f4e3ff3_thumb.png",
                    "popularityRank": 945,
                    "likeRank": 823,
                    "trashRank": 2981,
                    "url": "https://mywaifulist.moe/waifu/miko-sakura-hololive-production"
                }
            }
        ]
    }
}
```

This endpoint returns the ranking of the most popular v-tubers of all time in MyWaifuList.

### HTTP Request
`GET https://reina-api.vercel.app/api/mwl/vtubers`

## Get Trash Waifus

```js
const { get } = require('axios').default
get('https://reina-api.vercel.app/api/mwl/trash')
  .then((res) => console.log(res))
  .catch((err) => console.log(err))
```

> The reponse schema would be like this:

```JSON
{
    "status": 200,
    "error": false,
    "message": "Success",
    "data": {
        "title": "Worst Anime Waifus",
        "data": [
            {
                "rank": 1,
                "waifu": {
                    "name": "Malty S Melromarc",
                    "originalName": "マルティ＝S＝メルロマルク",
                    "slug": "malty-melromarc-the-rising-of-the-shield-hero",
                    "image": "https://thicc.mywaifulist.moe/waifus/2090/e94dd823bf4895d1f788739261ef40bdf62e0b6ec6c1ac35a66a8eb5c5175926_thumb.jpeg",
                    "popularityRank": 23,
                    "likeRank": 1476,
                    "trashRank": 2,
                    "url": "https://mywaifulist.moe/waifu/malty-melromarc-the-rising-of-the-shield-hero"
                }
            },
            {
                "rank": 2,
                "waifu": {
                    "name": "Akemi Hinazuki",
                    "originalName": "雛月明美",
                    "slug": "akemi-hinazuki",
                    "image": "https://thicc.mywaifulist.moe/waifus/3907/b6a3d87181ef185a390b96e5fe541513a5b6d86e5d3a8e257743f8d623c3f6c7_thumb.jpeg",
                    "popularityRank": 62,
                    "likeRank": 6769,
                    "trashRank": 3,
                    "url": "https://mywaifulist.moe/waifu/akemi-hinazuki"
                }
            },
            {
                "rank": 3,
                "waifu": {
                    "name": "Nobuyuki Sugou",
                    "originalName": "須郷伸之",
                    "slug": "nobuyuki-sugou-sword-art-online",
                    "image": "https://thicc.mywaifulist.moe/waifus/6102/fe5056fa3f431b73be1b9bfd203e3b725c8b988f534dff09aaaaa6d7cc769939_thumb.jpeg",
                    "popularityRank": 114,
                    "likeRank": 7197,
                    "trashRank": 9,
                    "url": "https://mywaifulist.moe/waifu/nobuyuki-sugou-sword-art-online"
                }
            },
            {
                "rank": 4,
                "waifu": {
                    "name": "Motoyasu Kitamura",
                    "originalName": "北村元康",
                    "slug": "motoyasu-kitamura-the-rising-of-the-shield-hero",
                    "image": "https://thicc.mywaifulist.moe/waifus/21066/4bd15973c397efb0dfea4d52d933475ac324a1f9507a8af168b788ba4dc85032_thumb.jpeg",
                    "popularityRank": 137,
                    "likeRank": 6586,
                    "trashRank": 10,
                    "url": "https://mywaifulist.moe/waifu/motoyasu-kitamura-the-rising-of-the-shield-hero"
                }
            },
            {
                "rank": 5,
                "waifu": {
                    "name": "Shinji Matou",
                    "originalName": "間桐 慎二",
                    "slug": "shinji-matou-fate-stay-night",
                    "image": "https://thicc.mywaifulist.moe/waifus/6104/087b8ce0b1d8c5c0d83912d4b868e67e37fb6ccc673697d80f4eee1faf4f7169_thumb.jpeg",
                    "popularityRank": 141,
                    "likeRank": 5407,
                    "trashRank": 11,
                    "url": "https://mywaifulist.moe/waifu/shinji-matou-fate-stay-night"
                }
            },
            {
                "rank": 49,
                "waifu": {
                    "name": "Public Safety Commission President",
                    "originalName": "公安委員会会長",
                    "slug": "public-safety-commission-president",
                    "image": "https://thicc.mywaifulist.moe/waifus/19503/cd53af713e8c7fd7ccf79fddb03cca49dde14c965c0a2a0fdfcf4ccde54f5633_thumb.png",
                    "popularityRank": 5319,
                    "likeRank": 25949,
                    "trashRank": 810,
                    "url": "https://mywaifulist.moe/waifu/public-safety-commission-president"
                }
            },
            {
                "rank": 50,
                "waifu": {
                    "name": "Kamado Ueshita",
                    "originalName": "上下 かまど",
                    "slug": "kamado-ueshita",
                    "image": "https://thicc.mywaifulist.moe/waifus/22664/68bf3f51332ddba18212710a1243d873c3f454a66d6b1ee045da5d7770f6090a_thumb.png",
                    "popularityRank": 5279,
                    "likeRank": 22984,
                    "trashRank": 830,
                    "url": "https://mywaifulist.moe/waifu/kamado-ueshita"
                }
            }
        ]
    }
}
```

This endpoint returns the ranking of the worst waifus of all time in MyWaifuList.

### HTTP Request
`GET https://reina-api.vercel.app/api/mwl/trash`

## Get Popular Waifus for the current Season

```js
const { get } = require('axios').default
get('https://reina-api.vercel.app/api/mwl/current/popular')
  .then((res) => console.log(res))
  .catch((err) => console.log(err))
```

> The reponse schema would be like this:

```JSON
{
    "status": 200,
    "error": false,
    "message": "Success",
    "data": {
        "title": "Summer 2022 Most Popular Waifus",
        "data": [
            {
                "rank": 1,
                "waifu": {
                    "name": "Albedo",
                    "originalName": "アルベド",
                    "slug": "albedo-overlord",
                    "image": "https://thicc.mywaifulist.moe/waifus/651/805deb0689c2b3e850e8e9e851694b36ac2a98f6d7b78b6299182181ade157a3_thumb.jpg",
                    "popularityRank": 39,
                    "likeRank": 38,
                    "trashRank": 122,
                    "url": "https://mywaifulist.moe/waifu/albedo-overlord"
                }
            },
            {
                "rank": 2,
                "waifu": {
                    "name": "Hestia",
                    "originalName": "ヘスティア",
                    "slug": "hestia-is-it-wrong-to-try-to-pick-up-girls-in-a-dungeon",
                    "image": "https://thicc.mywaifulist.moe/waifus/794/dbb11133b0183184cb32f528bf4ea3d1d0cb5ca75f78fd8d18addb9aac0af359_thumb.png",
                    "popularityRank": 58,
                    "likeRank": 57,
                    "trashRank": 155,
                    "url": "https://mywaifulist.moe/waifu/hestia-is-it-wrong-to-try-to-pick-up-girls-in-a-dungeon"
                }
            },
            {
                "rank": 3,
                "waifu": {
                    "name": "Chizuru Ichinose",
                    "originalName": "一ノ瀬 千鶴",
                    "slug": "chizuru-ichinose-rent-a-girlfriend",
                    "image": "https://thicc.mywaifulist.moe/waifus/13496/5896d38e5b89cb3b8d5de733dfbd6a8b7ed59d835621f22f7f9a50ee62294285_thumb.jpeg",
                    "popularityRank": 84,
                    "likeRank": 73,
                    "trashRank": 286,
                    "url": "https://mywaifulist.moe/waifu/chizuru-ichinose-rent-a-girlfriend"
                }
            },
            {
                "rank": 14,
                "waifu": {
                    "name": "Suzune Horikita",
                    "originalName": "堀北 鈴音",
                    "slug": "suzune-horikita-classroom-of-the-elite",
                    "image": "https://thicc.mywaifulist.moe/waifus/6297/0778d0589411a5d553cd17d9b2bc0cfe951e670024b7399f4daea3a6cbc42aab_thumb.png",
                    "popularityRank": 358,
                    "likeRank": 323,
                    "trashRank": 1135,
                    "url": "https://mywaifulist.moe/waifu/suzune-horikita-classroom-of-the-elite"
                }
            },
            {
                "rank": 15,
                "waifu": {
                    "name": "Mary Saotome",
                    "originalName": "早乙女 芽亜里",
                    "slug": "mary-saotome-kakegurui-compulsive-gambler",
                    "image": "https://thicc.mywaifulist.moe/waifus/6168/1fe3077110d9840524eaf2e50f48253c4fd394a7fafe4fb686ff8fa115b7a32c_thumb.jpg",
                    "popularityRank": 368,
                    "likeRank": 333,
                    "trashRank": 910,
                    "url": "https://mywaifulist.moe/waifu/mary-saotome-kakegurui-compulsive-gambler"
                }
            }
        ]
    }
}
```

This endpoint returns the most popular waifus for the current season in MyWaifuList.

### HTTP Request
`GET https://reina-api.vercel.app/api/mwl/current/popular`

## Get Best Waifus for the current Season

```js
const { get } = require('axios').default
get('https://reina-api.vercel.app/api/mwl/current/best')
  .then((res) => console.log(res))
  .catch((err) => console.log(err))
```

> The reponse schema would be like this:

```JSON
{
    "status": 200,
    "error": false,
    "message": "Success",
    "data": {
        "title": "Summer 2022 Best Waifus",
        "data": [
            {
                "rank": 1,
                "waifu": {
                    "name": "Chizuru Ichinose",
                    "originalName": "一ノ瀬 千鶴",
                    "slug": "chizuru-ichinose-rent-a-girlfriend",
                    "image": "https://thicc.mywaifulist.moe/waifus/13496/5896d38e5b89cb3b8d5de733dfbd6a8b7ed59d835621f22f7f9a50ee62294285_thumb.jpeg",
                    "popularityRank": 84,
                    "likeRank": 73,
                    "trashRank": 286,
                    "url": "https://mywaifulist.moe/waifu/chizuru-ichinose-rent-a-girlfriend"
                }
            },
            {
                "rank": 2,
                "waifu": {
                    "name": "Evileye",
                    "originalName": "イビルアイ",
                    "slug": "evileye-overlord",
                    "image": "https://thicc.mywaifulist.moe/waifus/8967/75dbc4ac7652e778c7d462e6b04ca0072da0e693a5719bb923c274280e717d2b_thumb.png",
                    "popularityRank": 697,
                    "likeRank": 612,
                    "trashRank": 1787,
                    "url": "https://mywaifulist.moe/waifu/evileye-overlord"
                }
            },
            {
                "rank": 3,
                "waifu": {
                    "name": "Arisu Sakayanagi",
                    "originalName": "坂柳 有栖",
                    "slug": "arisu-sakayanagi-classroom-of-the-elite",
                    "image": "https://thicc.mywaifulist.moe/waifus/10726/4fbee3e2c3d1ddccc143d0dad752a22f2215af9176d37af073283e9f580f8eaa_thumb.jpg",
                    "popularityRank": 1683,
                    "likeRank": 1500,
                    "trashRank": 4244,
                    "url": "https://mywaifulist.moe/waifu/arisu-sakayanagi-classroom-of-the-elite"
                }
            },
            {
                "rank": 19,
                "waifu": {
                    "name": "Honami Ichinose",
                    "originalName": "一之瀬 帆波",
                    "slug": "honami-ichinose-classroom-of-the-elite",
                    "image": "https://thicc.mywaifulist.moe/waifus/7838/225705d66045525ff784b2649a3fffad6dfaf8537d224707607ef1d9354f1456_thumb.jpg",
                    "popularityRank": 595,
                    "likeRank": 505,
                    "trashRank": 2292,
                    "url": "https://mywaifulist.moe/waifu/honami-ichinose-classroom-of-the-elite"
                }
            },
            {
                "rank": 20,
                "waifu": {
                    "name": "Lilith",
                    "originalName": "",
                    "slug": "lilith-my-recently-hired-maid-is-suspicious",
                    "image": "https://thicc.mywaifulist.moe/waifus/28232/63a2d4cc5e99010932e2b80f9e1e458e75d330d2604aac0d55353d851af12845_thumb.png",
                    "popularityRank": 7408,
                    "likeRank": 6322,
                    "trashRank": 23120,
                    "url": "https://mywaifulist.moe/waifu/lilith-my-recently-hired-maid-is-suspicious"
                }
            }
        ]
    }
}
```

This endpoint returns the ranking of the best waifus for the current season in MyWaifuList.

### HTTP Request
`GET https://reina-api.vercel.app/api/mwl/current/best`

## Get Trash Waifus for the current Season

```js
const { get } = require('axios').default
get('https://reina-api.vercel.app/api/mwl/current/trash')
  .then((res) => console.log(res))
  .catch((err) => console.log(err))
```

> The reponse schema would be like this:

```JSON
{
    "status": 200,
    "error": false,
    "message": "Success",
    "data": {
        "title": "Summer 2022 Worst Waifus",
        "data": [
            {
                "rank": 1,
                "waifu": {
                    "name": "Mami Nanami",
                    "originalName": "七海麻美",
                    "slug": "mami-nanami-rent-a-girlfriend",
                    "image": "https://thicc.mywaifulist.moe/waifus/27411/b9496a6944b1ef43b6ee700486fbf8cdaf02242ea15a4620c7606d8fe988eec9_thumb.jpeg",
                    "popularityRank": 234,
                    "likeRank": 1002,
                    "trashRank": 34,
                    "url": "https://mywaifulist.moe/waifu/mami-nanami-rent-a-girlfriend"
                }
            },
            {
                "rank": 2,
                "waifu": {
                    "name": "Kazuya Kinoshita",
                    "originalName": "木ノ下 和也",
                    "slug": "kazuya-kinoshita-rent-a-girlfriend",
                    "image": "https://thicc.mywaifulist.moe/waifus/27410/7176096a2040be5459258871aae093ae4ede73c773735211620185bb2c66bfa8_thumb.jpeg",
                    "popularityRank": 1143,
                    "likeRank": 6747,
                    "trashRank": 99,
                    "url": "https://mywaifulist.moe/waifu/kazuya-kinoshita-rent-a-girlfriend"
                }
            },
            {
                "rank": 3,
                "waifu": {
                    "name": "Apollo",
                    "originalName": "アポロン",
                    "slug": "apollo-is-it-wrong-to-try-to-pick-up-girls-in-a-dungeon",
                    "image": "https://thicc.mywaifulist.moe/waifus/23094/fbcf881affc384ded4d0640a05fc589b32a5889dce49b9a20f19ebed5cfbed6a_thumb.png",
                    "popularityRank": 1349,
                    "likeRank": 15792,
                    "trashRank": 112,
                    "url": "https://mywaifulist.moe/waifu/apollo-is-it-wrong-to-try-to-pick-up-girls-in-a-dungeon"
                }
            },
            {
                "rank": 4,
                "waifu": {
                    "name": "Bete Loga",
                    "originalName": "",
                    "slug": "bete-loga",
                    "image": "https://thicc.mywaifulist.moe/waifus/4662/1441c3b7f8c3ae91fe94d16756d60c6c6ba4e795f4657dabee9a4c1ea01146d5_thumb.png",
                    "popularityRank": 1320,
                    "likeRank": 4777,
                    "trashRank": 152,
                    "url": "https://mywaifulist.moe/waifu/bete-loga"
                }
            },
            {
                "rank": 18,
                "waifu": {
                    "name": "Sayuri Sadaoka",
                    "originalName": "一 いち ノ 瀬 せ 小 さ 百合 ゆり",
                    "slug": "sayuri-sadaoka",
                    "image": "https://thicc.mywaifulist.moe/waifus/38061/d0952841664e2f8832c947bd1c24d4caee92e52eaf42a660d96acab85c272c3a_thumb.png",
                    "popularityRank": 13453,
                    "likeRank": 21586,
                    "trashRank": 4714,
                    "url": "https://mywaifulist.moe/waifu/sayuri-sadaoka"
                }
            },
            {
                "rank": 19,
                "waifu": {
                    "name": "Nasrene Belt Cure",
                    "originalName": "ナスレネ・ベルト・キュール",
                    "slug": "nasrene-belt-cure-overlord",
                    "image": "https://thicc.mywaifulist.moe/waifus/19102/e2ba22ed08c8bd1f35a61947954ee85af838a2312f7e8e55ba53c386e73cbdd9_thumb.png",
                    "popularityRank": 16798,
                    "likeRank": 24844,
                    "trashRank": 6235,
                    "url": "https://mywaifulist.moe/waifu/nasrene-belt-cure-overlord"
                }
            },
            {
                "rank": 20,
                "waifu": {
                    "name": "Albert Ende",
                    "originalName": "アルバート・エンデ",
                    "slug": "albert-ende",
                    "image": "https://thicc.mywaifulist.moe/waifus/36817/af12d97b132cfe734dd51d473704d94008d03680b0e60d1125f4574757bcbd97_thumb.png",
                    "popularityRank": 25044,
                    "likeRank": 33841,
                    "trashRank": 10116,
                    "url": "https://mywaifulist.moe/waifu/albert-ende"
                }
            }
        ]
    }
}
```

This endpoint returns the ranking of the worst waifus for the current season in MyWaifuList.

### HTTP Request
`GET https://reina-api.vercel.app/api/mwl/current/trash`