---
layout: base
title: Home
---



<script>
$(document).ready(function() {
    $('#main').DataTable( {
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
} );
</script>



# Betacoronavirus predictions

> Becker, D., Albery, G. F., Sjodin, A. R., Poisot, T., Dallas, T., Eskew, E. A., ... & Carlson, C. J. (2020). Predicting wildlife hosts of betacoronaviruses for SARS-CoV-2 sampling prioritization. bioRxiv. doi: https://doi.org/10.1101/2020.05.22.111344





<body>



<table id="main" class="display" style="width:100%">
  <thead>
  <tr>
    <th> Species </th>
    <th> Betacov </th>
    <th> Trait1 </th>
    <th> Trait2 </th>
    <th> Trait3 </th>
    <th> Network1 </th>
    <th> Network2 </th>
    <th> Network3 </th>
    <th> Network4 </th>
    <th> Ensemble </th>
  </tr>
  </thead>

  <tbody>
  {% for row in site.data.predictions %}
	{% if forloop.first %}
  {% endif %}
  {% tablerow pair in row %}
    {{ pair[1] }}
  {% endtablerow %}
  {% endfor %}

  </tbody>
</table>



</body>






