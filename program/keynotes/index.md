---
layout: page
title: Keynote Speakers
---

{% comment %}Speaker details live in _data/keynotes.yml, which also feeds the home page preview.{% endcomment %}
# Keynote Speakers
We are excited to announce our keynote speakers for the 2027 workshop. Talk titles will be announced soon.

<div class="speaker-grid">
{%- for speaker in site.data.keynotes %}
<div class="speaker-card">
    <div class="speaker-image-container">
        <img src="{{ speaker.photo | relative_url }}" alt="{{ speaker.name }}" class="speaker-image">
    </div>
    <div class="speaker-details">
        <div class="speaker-header">
            <h2 class="speaker-name">{{ speaker.name }}</h2>
            <p class="speaker-role">{{ speaker.role | xml_escape }}</p>
        </div>
        
        <div class="talk-section">
            <div class="talk-label">Talk Title</div>
            <h3 class="talk-title">{{ speaker.talk_title | default: "To Be Announced" }}</h3>
        </div>
        
        <div class="speaker-bio">
            {{ speaker.bio }}
        </div>
    </div>
</div>
{%- endfor %}
</div>
