---
layout: product
title: AudioWatch
subtitle: Automated real-time audio monitoring
description: Analyses incoming broadcast feeds to detect sounds that are not safe for broadcast.
image: audiowatch.png
type: professional
date: 2021-09-01
order: 2
tags: [{name: AI, icon: fa-solid fa-microchip}]
---
With live broadcast, it is important to ensure that the output is always "broadcast safe" and does not contain any inappropriate sounds or language. As soon as unsafe audio is detected, the operator needs to work out which stream it is appearing on. This can be very challenging with numerous audio sources, as they must listen to each stream one-by-one. It can often take a minute or more to find the source, espeically if the sound is intermittent, during which time the broadcast remains muted.

AudioWatch is an audio AI system that uses automated audio tagging to identify potentially problematic audio and highlights the offending source on a video multiviewer. This system not only alerts an operator to the presence of unsafe audio, but also shows them exactly which stream it appears on, allowing them to deal with the issue within seconds rather than minutes.

<p class="video">
    <video width="1920" height="1080" controls>
        <source type="video/webm" src="/assets/vid/audiowatch.webm" />
    </video><br />
    <span class="video-credit">Credit: BBC Studios</span>
</p>

To create AudioWatch, we used the <a href="https://github.com/qiuqiangkong/audioset_tagging_cnn" target="_blank">PANNs</a> pre-trained classifier to detect the probability of various sounds occuring. We then optimised the trigger thresholds to create the right sensitivity for our target use case.

Fortunately, not much unsafe audio makes it to broadcast. However, this means there is very little training data on which to do the optimisation. To get around this, we used <a href="https://github.com/justinsalamon/scaper" target="_blank">Scaper</a> to programmatically generate thousands of hours of unsafe audio by mixing sound effects and speech in with clean broadcast output. As the position of the unsafe audio was known, we could calculate a confusion matrix of true and false positives/negatives so that we could set the right trigger points.

AudioWatch is in regular use by the BBC, and has been since 2021. Most notably, it has been employed by the Natural History Unit for Springwatch, Autumnwatch, and Winterwatch. These programmes are often accompanied by 12-hour live streams, which need to be monitored. With AudioWatch, a single operator is able to monitor the streams and very quickly deal with any problems.

<a class="button is-light" href="https://www.bbc.co.uk/rd/blog/2021-11-live-audio-monitoring-autumnwatch-ai" target="_blank">
    <span class="icon">
        <i class="fa-solid fa-up-right-from-square"></i>
    </span>
    <span>BBC R&D Blog</span>
</a>