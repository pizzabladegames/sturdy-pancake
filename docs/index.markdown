---
layout: default
title: Sturdy Pancake
numCols: 3
---

## Available Books

<table>
  {% for row in site.data.books %}
      {% assign new_row = forloop.index0 | modulo:3 %}
      {% if forloop.first  == true%}
        <tr>
        <td>
          <img src="{{ site.baseurl }}{{ row.thumbnail }}" style="width: 128px; image-rendering: pixelated;" />
        </td>
      {% elsif new_row == 0 %}
        </tr>
        <tr>
          <td>
            <img src="{{ site.baseurl }}{{ row.thumbnail }}" style="width: 128px; image-rendering: pixelated;" />
          </td>
      {% else %}
          <td>
            <img src="{{ site.baseurl }}{{ row.thumbnail }}" style="width: 128px; image-rendering: pixelated;" />
          </td>
      {% endif %}
  {% endfor %}
  </tr>
</table>

