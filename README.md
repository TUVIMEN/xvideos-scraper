# xvideos-scraper

A bash script for scraping xvideos videos, profiles, channels and pornstars metadata in json.

## Requirements

 - [reliq](https://github.com/TUVIMEN/reliq)
 - [jq](https://github.com/stedolan/jq)

## Installation

    install -m 755 xvideos-scraper /usr/bin

## Json format

Here's example of a [video](video-example.json) and [profile](profile-example.json).

## Usage

Profiles, channels and pornstars have the same format and are treated the same way.

Data is saved into files named by the sha256sum of their url.

Download metadata of video to DIR

    xvideos-scraper -d DIR -v URL -v URL -v URL
    xvideos-scraper -d DIR URL URL URL

Download metadata of profile, channel or pornstar using 8 threads

    xvideos-scraper -t 8 -p URL -p URL -p URL
    xvideos-scraper -t 8 URL URL URL

Download metadata of all profiles, channels and pornstars from sitemap

    xvideos-scraper -P

Pass video URLS into the recursive spider

    xvideos-scraper -V URL URL URL

Get some help

    xvideos-scraper -h
