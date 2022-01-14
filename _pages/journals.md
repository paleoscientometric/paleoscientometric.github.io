---
layout: single
author_profile: false
permalink: /journals/
title: "Paleontological Journals"
header:
  #overlay_filter: 0.7 # same as adding an opacity of 0.5 to a black background
  #caption: "Photo: [**Pexels**](https://www.pexels.com/photo/abstract-art-blur-bright-373543/)"
  overlay_image: assets/images/bg.jpg
classes: wide
datatable: true
---
<table id="example" class="display" style="width:100%">
<thead>
{% for row in site.data.journals %}
    {% if forloop.first %}
    <tr>
      {% for pair in row %}
        <th>{{ pair[0] }}</th>
      {% endfor %}
    </tr>
    {% endif %}
{% endfor %}

</thead>

<tbody>
  {% for row in site.data.journals %}
    {% tablerow pair in row %}
      {{ pair[1] }}
    {% endtablerow %}
    
  {% endfor %}
  </tbody>
</table>

<script>
$('#example').DataTable( {
} );
</script>