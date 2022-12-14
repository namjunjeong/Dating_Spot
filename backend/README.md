# Backend-Server

โญ๏ธ OpenSource Project โญ๏ธ

### ๐จ Local Server URL (Server Host) ๐จ

```text
http://127.0.0.1:3000
```

### ๐ธ Overview

| HTTP METHOD |  End Point   |  Description  |
| :---------: | :----------: | :-----------: |
|    POST     |    /user     |   ํ์๊ฐ์    |
|     GET     |    /user     |   ์ ์  ์กฐํฌ   |
|   DELETE    |    /user     |   ์ ์  ํํด   |
|    POST     | /auth/login  |    ๋ก๊ทธ์ธ     |
|     GET     | /auth/logout |   ๋ก๊ทธ์์    |
|    POST     | /auth/guest  | ๊ฒ์คํธ ๋ก๊ทธ์ธ |
|    POST     |    /data     | ์นด์นด์ค๋งต ์ ๋ณด |
|    POST     |    /spot     |   ์คํ ์ถ๊ฐ   |
|     GET     |    /spot     |   ์คํ ์กฐํ   |

---

#### ๐งก ํ์๊ฐ์

##### ๐ Request Body

```json
{
  "id": "guest",
  "password": "1234",
  "email": "guest@example.com",
  "username": "elon"
}
```

##### ๐ Server Response

```json
{
  "status": 200,
  "message": "ํ์๊ฐ์ ์ฑ๊ณต"
}
```

---

#### ๐งก ์ ์  ์กฐํ

##### ๐ Server Response

```json
{
  "status": 200,
  "data": {
    "_id": "63904cc6ace7c48b96001fb5",
    "id": "guest",
    "password": "abcdefghijklmn",
    "email": "guest@example.com",
    "username": "elon",
    "created_at": "2022-12-07T08:20:22.441Z",
    "__v": 0
  }
}
```

---

#### ๐งก ์ ์  ํํด

##### ๐ Server Response

```json
{
  "status": 200,
  "message": "ํํด ์ฑ๊ณต"
}
```

---

#### ๐งก ๋ก๊ทธ์ธ

##### ๐ Request Body

```json
{
  "id": "guest",
  "password": "1234"
}
```

##### ๐ Server Response

```json
{
  "status": 200,
  "message": "๋ก๊ทธ์ธ ์ฑ๊ณต"
}
```

---

#### ๐งก ๋ก๊ทธ์์

##### ๐ Server Response

```json
{
  "status": 200,
  "message": "๋ก๊ทธ์์"
}
```

---

#### ๐งก ๊ฒ์คํธ ๋ก๊ทธ์ธ

##### ๐ Server Response

```json
{
  "status": 200,
  "message": "๋ก๊ทธ์ธ ์ฑ๊ณต"
}
```

---

#### ๐งก ์นด์นด์ค๋งต ์ ๋ณด

##### ๐ Request Body

```json
{
  "x": 126.923778562273,
  "y": 37.5568707448873,
  "catagory": "cafe"
}
```

##### ๐ Server Response

```json
{
  "status": 200,
  "data": {
    "x": 126.923778562273,
    "y": 37.5568707448873,
    "list": [
      {
        "place_name": "1984",
        "x": 126.922881704192,
        "y": 37.5573639089622,
        "picture_url": "image.jpg",
        "id": 123,
        "place_url": "https://place.map.kakao.com/23634722",
        "rate": 4.7
      },
      {
        "place_name": "์นดํ๊ณต๋ช",
        "x": 126.926352615326,
        "y": 37.5598708965573,
        "picture_url": "image.jpg",
        "id": 124,
        "place_url": "https://place.map.kakao.com/1797970569",
        "rate": 3.8
      }
    ]
  }
}
```

---

#### ๐งก ์คํ ์ถ๊ฐ

##### ๐ Request Body

```json
{
  "x": 126.923778562273,
  "y": 37.5568707448873,
  "cafe": [
    {
      "place_name": "1984",
      "x": 126.922881704192,
      "y": 37.5573639089622,
      "picture_url": "t1.kakaocdn.net/thumb/T800x0.q80/?fname=http%3A%2F%2Ft1.daumcdn.net%2Fplace%2F34E424DE54454CCB8C5623E96B979B9F",
      "place_url": "https://place.map.kakao.com/23634722",
      "rate": 4.3
    },
    {
      "place_name": "์นดํ๊ณต๋ช",
      "x": 126.926352615326,
      "y": 37.5598708965573,
      "picture_url": "t1.kakaocdn.net/thumb/T800x0.q80/?fname=http%3A%2F%2Ft1.daumcdn.net%2Flocalfiy%2Fsearchregister_1919726515",
      "place_url": "https://place.map.kakao.com/1797970569",
      "rate": 4.3
    }
  ],
  "restaurant": [
    {
      "place_name": "ํ์ด๋๋ผ์ค ํ๋์ง์ ",
      "x": "126.924760602353",
      "y": "37.5571921297692",
      "picture_url": "t1.kakaocdn.net/thumb/T800x0.q80/?fname=http%3A%2F%2Ft1.daumcdn.net%2Fplace%2FCC5A124B50294DFCB690BD5E9EC7F28E",
      "place_url": "http://place.map.kakao.com/1622865435",
      "rate": 4.3
    },
    {
      "place_name": "์คํ๋ณต์ถ",
      "x": "126.924296449184",
      "y": "37.5595596531777",
      "picture_url": "t1.kakaocdn.net/thumb/T800x0.q80/?fname=http%3A%2F%2Ft1.kakaocdn.net%2Fmystore%2FA19E0A5AF48C42F681B4C5CC56E70F42",
      "place_url": "https://place.map.kakao.com/965893653",
      "rate": 4.3
    }
  ]
}
```

##### ๐ Server Response

```json
{
  "status": 200,
  "message": "์คํ ์ถ๊ฐ ์ฑ๊ณต"
}
```

---

#### ๐งก ์คํ ์กฐํ

##### ๐ Server Response

```json
[
  {
    "_id": "6391de41e4b8c980a0724c59",
    "email": "guest@example.com",
    "x": 126.923778562273,
    "y": 37.5568707448873,
    "cafe": [
      {
        "place_name": "1984",
        "x": 126.922881704192,
        "y": 37.5573639089622,
        "picture_url": "t1.kakaocdn.net/thumb/T800x0.q80/?fname=http%3A%2F%2Ft1.daumcdn.net%2Fplace%2F34E424DE54454CCB8C5623E96B979B9F",
        "place_url": "https://place.map.kakao.com/23634722",
        "rate": 4.3,
        "_id": "6391de41e4b8c980a0724c5a"
      },
      {
        "place_name": "์นดํ๊ณต๋ช",
        "x": 126.926352615326,
        "y": 37.5598708965573,
        "picture_url": "t1.kakaocdn.net/thumb/T800x0.q80/?fname=http%3A%2F%2Ft1.daumcdn.net%2Flocalfiy%2Fsearchregister_1919726515",
        "place_url": "https://place.map.kakao.com/1797970569",
        "rate": 4.3,
        "_id": "6391de41e4b8c980a0724c5b"
      }
    ],
    "restaurant": [
      {
        "place_name": "ํ์ด๋๋ผ์ค ํ๋์ง์ ",
        "x": 126.924760602353,
        "y": 37.5571921297692,
        "picture_url": "t1.kakaocdn.net/thumb/T800x0.q80/?fname=http%3A%2F%2Ft1.daumcdn.net%2Fplace%2FCC5A124B50294DFCB690BD5E9EC7F28E",
        "place_url": "http://place.map.kakao.com/1622865435",
        "rate": 4.3,
        "_id": "6391de41e4b8c980a0724c5c"
      },
      {
        "place_name": "์คํ๋ณต์ถ",
        "x": 126.924296449184,
        "y": 37.5595596531777,
        "picture_url": "t1.kakaocdn.net/thumb/T800x0.q80/?fname=http%3A%2F%2Ft1.kakaocdn.net%2Fmystore%2FA19E0A5AF48C42F681B4C5CC56E70F42",
        "place_url": "https://place.map.kakao.com/965893653",
        "rate": 4.3,
        "_id": "6391de41e4b8c980a0724c5d"
      }
    ],
    "stroll": [],
    "gallery": [],
    "themeCafe": [],
    "shopping": [],
    "hopping": [],
    "drink": [],
    "created_at": "2022-12-08T12:53:21.412Z",
    "__v": 0
  }
]
```

---
