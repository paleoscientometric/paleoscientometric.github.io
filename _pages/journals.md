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
---
<div class="small">

Press <Shift> and click on the arrows next to the columns headers of your choice to order by multiple columns
<br>
<br>

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
</div>

<script>

// multicolumn sorting
$('#example').DataTable( {
  columnDefs: [ {
            targets: [ 0 ],
            orderData: [ 0, 1 ]
        }, {
            targets: [ 1 ],
            orderData: [ 1, 0 ]
        }, {
            targets: [ 4 ],
            orderData: [ 4, 0 ]
        } ]
} );
</script>
