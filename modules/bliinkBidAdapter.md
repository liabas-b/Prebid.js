# Overview

```
Module Name: BLIINK Bidder Adapter
Module Type: Bidder Adapter
Maintainer: samuel@bliink.io | jonathan@bliink.io
gdpr_supported: true
tcf2_supported: true
media_types: banner, native, video
```

# Description

Module that connects to BLIINK demand sources to fetch bids.

# Test Parameters

## Sample Banner Ad Unit

```js
const adUnits = [
  {
    code: '/19968336/test',
    mediaTypes: {
      banner: {
        sizes: [[300, 250]]
      }
    },
    bids: [
      {
        bidder: 'bliink',
        params: {
          placement: 'banner',
          tagId: '14f30eca-85d2-11e8-9eed-0242ac120007'
        }
      }
    ]
  }
]
```

## Sample Instream Video Ad Unit

```js
const adUnits = [
  {
    code: '/19968336/prebid_cache_video_adunit',
    sizes: [[640,480]],
    mediaType: 'video',
    mediaTypes: {
      video: {
        context: 'instream',
        playerSize: [640, 480],
        mimes: ['video/mp4'],
        protocols: [1, 2, 3, 4, 5, 6, 7, 8],
        playbackmethod: [2],
        skip: 1
      }
    },
    bids: [
      {
        bidder: 'bliink',
        params: {
          tagId: '41',
          placement: 'video',
        }
      }
    ]
  }
]
```
