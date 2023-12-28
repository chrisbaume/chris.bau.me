---
layout: product
title: BBC Notes
subtitle: Live digital programme notes
description: Displays timed text, images, and links to audiences during live events, live broadcasts, and on-demand.
image: notes.png
type: consumer
date: 2019-01-01
order: 1
tags: [{name: React, icon: fa-brands fa-react}]
---
<p>
Radio programmes tell stories using music, words and sounds. However, visual information could be used to aid this type of storytelling. The prevalence of smartphones, tablets and laptops provide the opportunity to display this information to the audience. The BBC Philharmonic saw that by sending information to audiences they could tell the stories behind the music as it happens. Their hope was that this feature would help break down barriers for people who may not be familiar with orchestral concerts, and attract younger audience members who have grown up with smartphones and multi-screen experiences. Since 2016, the orchestra has been using Venue Explorer to deliver timed ‘programme notes’ to share these stories with the concert hall audience using their smartphones.
</p>
<p>
BBC Notes is a web app that shows text, images, and links to audiences to enhance their listening experience during live events, live broadcasts, and on demand. This information is shown at specific times to guide listeners through the programme and to illustrate the story or music
</p>
<p class="video">
    <video width="1920" height="1080" controls>
        <source type="video/webm" src="/assets/vid/notes.webm" />
    </video><br />
    <span class="video-credit">Credit: BBC R&amp;D</span>
</p>
<p>
One of the biggest challenges we faced was designing the system in a way that could send notes to potentially hundreds of thousands of people that might be listening to a live performance on the radio. Venue Explorer used WebSockets to create direct connections to devices for sending real-time information, but this limited us to only a few hundred connections per server. To overcome this limitation, we used a product called AppSync to handle Websockets in a way that can automatically scale to millions of users in an efficient and cost-effective way. We will find out how successful this approach is in our upcoming trials.
</p><p>
We have also made the system accessible by using text-to-speech to generate audio description, and by including support for screen readers. This will allow visually impaired listeners, or those who can’t look at their phone (if doing chores for example), to have the information read out to them. We also included the ability to see a definition of any jargon used by simply clicking on underlined words.
</p><p>
95% of respondents agreed that it improved their understanding and enjoyment of the music. Some spoke of how it helped them to understand the context of the music, focus on certain aspects of it and follow their progress through the event.
</p>
<div class="buttons">
    <a class="button is-light" href="https://www.bbc.co.uk/rd/blog/2019-08-proms-programme-notes" target="_blank">
        <span class="icon">
            <i class="fa-solid fa-up-right-from-square"></i>
        </span>
        <span>BBC R&D Blog</span>
    </a>
    <a class="button is-light" href="https://www.bbc.co.uk/rd/blog/2019-10-bbc-notes-proms" target="_blank">
        <span class="icon">
            <i class="fa-solid fa-up-right-from-square"></i>
        </span>
        <span>BBC R&D Blog</span>
    </a>
</div>