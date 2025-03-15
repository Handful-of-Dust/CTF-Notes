# What is OSINT?

OSINT stands for "open source intelligence." Simply put, this is the practice of finding things that are openly available on the internet. Sometimes all you need is a simple google search; sometimes more advanced tools and technical knowledge are needed. This file provides links for some of the most common tools.

Probably the most well-known collection of links out there is the [OSINT framework](https://osintframework.com/).

## Google Dorking

These are ways to filter out irrelevant results when performing Google searches. Boolean operators are probably familiar to most people.

`AND` gets results that contain both of the keywords or phrases you're looking for. For example: `cows AND ducks`

`OR` gets results that contain either of the keywords you're interested in: `cows OR ducks`

To exclude something from a search, you would use a minus sign. For example, this will search for results that mention cows and ducks but not platypuses: `cows AND ducks -platypus`

There's also a wildcard: `*` With this character, you can construct queries like this: `I had a * idea` This will return results for both "I had a bad idea" and "I had a good idea" and whatever other descriptive words people might use for their ideas online.

### Filters

These are separated from the keywords in your query by a colon:

You can filter for results only from a particular website: `site:fulladdressofsite.com`

You can also search for sites with a specific keyword in their URLs: `inurl:keyword`

You can search for particular kinds of files by keyword: `keyword filetype:pdf`

You can also still search for past versions of a site: `cache:fulladdressofsite.com`

These can get quite complicated as you search for specific keywords and filetypes. Exploit Database has a [Google hacking database](https://www.exploit-db.com/google-hacking-database) that might help if you're trying to do something specific and complicated.

## Using different search engines

It's always worth checking to see if a different search engine will turn up something you can use, even if it might not be your go-to to day-to-day searches.

* I find that [Bing](https://www.bing.com/) returns good results when trying to troubleshoot Microsoft products.
* If you're trying to get results in Russian, try Yandex. I've also found that Yandex has better image search capabilities than Google for some things...
* I've never tried Baidu, but it would likely be the best choice for anyone investigating the Chinese internet.

## The Wayback Machine

[The Wayback Machine](https://web.archive.org/) archives data that was once publicly available on the internet but may have since been removed. To use it, enter the URL you're interested in using the search box. You can then browse all available captures of that URL, which will show you if the site looked different in the past.
