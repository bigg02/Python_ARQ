# Python_ARQ

Python wrapper for the A.R.Q. API.

[![Python](http://forthebadge.com/images/badges/made-with-python.svg)](https://python.org)
[![GitHub](https://forthebadge.com/images/badges/built-by-developers.svg)](https://github.com/)

## Requirements

- Python 3.8 or newer.
- API URL and KEY, from [here](https://t.me/PatheticProgrammers).

## Installation

```sh
$ pip install python-arq
```

## Usage

For Example, to get a song link from deezer, you can do this

```py
from asyncio import run
from aiohttp import ClientSession
from python_arq import ARQ

session = ClientSession()
arq = ARQ(api_url, api_key, session)


async def main():
    results = await arq.deezer("Never gonna give you up", 1)
    song = results.result[0]
    title = song.title
    link = song.url
    print(link)


asyncio.run(main())
```

## Documentation

There is no documentation as of now, however, you can take help from the docstrings this way:

```py
from python_arq import ARQ

print(help(ARQ.deezer))
```

## Features as of now [List of APIs]

1. Deezer
2. Jiosaavn
3. Youtube
4. YoutubeDL
4. PronHub
5. Reddit
6. Torrent
7. Wallpapers
8. Urban Dictionary
9. Luna AI Chatbot
10. Lyrics
11. Wikipedia
12. NSFW Image Classification
13. Optical Character Recognition (OCR)
14. Proxy Scraper
15. The Movie Database [TMDB]
16. Quotly [TELEGRAM]
17. Translate
18. PypiPackageSearch

## Note

1. I'll add more features soon.
2. If you're stuck somewhere, [Pathetic Programmers](https://t.me/PatheticProgrammers) are there to help.
