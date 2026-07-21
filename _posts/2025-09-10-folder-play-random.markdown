---
layout: post
title:  "Weighted folder & Non-repeating shuffle"
date:   2025-09-10 10:30:00 +0800
categories: jekyll update
---

### Weighted folder playlists

A couple of days ago, I released version V1.2.0 of LotusPlayerLite, which includes a major update.

Recently, an enthusiastic user requested a playback mode that cycles through folders while shuffling the tracks within each one.

After looking into it, I found that there was indeed a demand for this; essentially, it is a weighted folder playback mode. While it wasn't difficult to implement, I was surprised to find that most standard music players overlook this requirement.

I quickly added this playback mode. Here is how it works:

1. Users can select multiple folders to create a playlist; the app then plays through this list of folders sequentially.
2. Each folder can be assigned a weight—or what could be described as "random selections per pass." For instance, if set to 5, the player will randomly select and play five tracks from that folder before moving on to the next one.

### Non-repeating shuffle design

Users also requested a non-repeating shuffle algorithm—meaning they wouldn't hear a recently played track again too soon.

I researched this and found many user complaints regarding the issue. Fundamentally, the "randomness" users expect differs from true mathematical randomness.

In this update, I modified the app's shuffle function to align with this user-centric definition of randomness.

To illustrate: under our new shuffle algorithm, if there are 100 tracks in total and you have just played a specific song, you are guaranteed not to hear that same song again for at least the next 50 random selections (half the total count).

Our new feature is now live; we invite anyone interested to give it a try.
