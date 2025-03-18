{%- assign id = '#shopify-section-' | append: section.id -%}

{% style %}
 {{id}} .marquee {
    background:{{section.settings.color_accent}};
    position: relative;
    width: 100vw;
    max-width: 100%;
    height: 60px;
    overflow-x: hidden;
    display: flex;
    align-items: center;
  }
 {{id}} .marquee-content {
      display: flex;
      gap: 4rem;
  }
  {{id}} .track {
    position: absolute;
    white-space: nowrap;
    font-size:6rem;
    will-change: transform;
    animation: marquee 38s linear infinite;
  }

  @keyframes marquee {
    from { transform: translateX(0); }
    to { transform: translateX(-50%); }
  }

    {{id}} .marquee .track:hover {
      animation-play-state: paused;
    }
span.marquee-gap {
    font-size: 14px;
    text-transform: uppercase;
    font-weight: 600;
    text-shadow: none;
    letter-spacing: 2px;
}
{% endstyle %}

<div class="marquee">
  <div class="track">
    <div class="marquee-content">
      {% for i in (1..5) %}
        {% for block in section.blocks %}
          <span class="marquee-gap" style="color:{{ block.settings.color }}">{{ block.settings.text }}</span>
        {% endfor %}
      {% endfor %}
    </div>
  </div>
</div>

{% schema %}
  {
  "name": "Scrolling text",
  "settings": [
    {
  		"type": "color",
  		"id": "color_accent",
  		"label": "Buttons color",
  		"default": "#F1EFE6"
	}
  ],
  "blocks": [
    {
      "type": "ScrollingText",
      "name": "Scrolling Text",
      "limit": 4,
      "settings": [
        {
          "type": "text",
          "id": "text",
          "default": "Title",
          "label": "Scrolling Text"
        },
        {
          "type": "color",
          "id": "color",
          "default": "#000000",
          "label": "Text Color"
        }
      ]
    }
  ],
  "presets": [
    {
      "name": "Scrolling text"
    }
  ]
}
{% endschema %}
