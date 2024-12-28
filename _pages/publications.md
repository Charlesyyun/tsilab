---
title: "TSI Lab - Publications"
layout: gridlay
excerpt: "TSI Lab -- Publications."
sitemap: false
permalink: /publications/
---


# Publications

## Group highlights

**At the end of this page, you can find the [full list of publications and patents](#full-list-of-publications).**

{% assign number_printed = 0 %}
{% for publi in site.data.publist %}

{% assign even_odd = number_printed | modulo: 2 %}
{% if publi.highlight == 1 %}

{% if even_odd == 0 %}
<div class="row">
{% endif %}

<div class="col-sm-6 clearfix">
 <div class="well">
  <pubtit>{{ publi.title }}</pubtit>
  <img src="{{ site.url }}{{ site.baseurl }}/images/pubpic/{{ publi.image }}" class="img-responsive" width="33%" style="float: left" />
  <p>{{ publi.description }}</p>
  <p><em>{{ publi.authors }}</em></p>
  <p><strong><a href="{{ publi.link.url }}">{{ publi.link.display }}</a></strong></p>
  <p class="text-danger"><strong> {{ publi.news1 }}</strong></p>
  <p> {{ publi.news2 }}</p>
 </div>
</div>

{% assign number_printed = number_printed | plus: 1 %}

{% if even_odd == 1 %}
</div>
{% endif %}

{% endif %}
{% endfor %}

{% assign even_odd = number_printed | modulo: 2 %}
{% if even_odd == 1 %}
</div>
{% endif %}

<p> &nbsp; </p>


## Patents
<em>Ye, Y., Zhou, Z., Liang, H., Xie, J., Ying, C., Li, Z., & Che, Y.</em><br />The Human-Vehicle Interaction Simulation Method, System, and Application Based on the Improved Social Force Model<br /> Application No.: 2024119320397 (2024)

<em>Ye, Y., Li, Z., Liang, H., Sun, J., Che, Y. & Zhou, Z.</em><br />Assessment Method for Attention Allocation Mechanism of Pedestrian Crossing Based on Virtual Reality Simulation<br /> Authorised No.: CN118865280B, Patent No. ZL202411328427.4 (2024)

<em>Ye, Y., Xu, P., Li, Z., Zheng, P., Xing, L., Cao, S., & Miao, T.</em><br /> A Method and System for Analyzing Influencing Factors of Economic Losses Due to Accidents <br /> Application No.: 202411323810.0 (2024)

<em>Ye, Y., Liang, H., Sun, J., Chen, X., Zhou, Z., Xu, P., Che, Y. & Li, Z.</em><br /> A route choice optimization method for dynamic user equilibrium under strongly heterogeneous cost fields <br /> Publication No.: CN118607740A (2024)

<em>Zhang, S., Liu, Z., Ye, Y. & Xie, S.</em><br /> A method, device, electronic equipment, and storage medium for road network simulation <br /> Publication No.: CN118194480A (2024)

<em>Chen, X., Zhang, S., Chen, C., Chen, X., Zheng, H., Shen, K., Ye, Y. & Sun, W.</em><br /> An OD calibration method for residential trip using mobile phone data and dynamic traffic assignment <br /> Publication No.: CN106571032A (2017)

## Full List of publications

{% for publi in site.data.publist %}

  {{ publi.title }} <br />
  <em>{{ publi.authors }} </em><br /><a href="{{ publi.link.url }}">{{ publi.link.display }}</a>

{% endfor %}
