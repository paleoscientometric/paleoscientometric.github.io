---
layout: single
permalink: /media/
---

<section class="blog-cat">
	<div class="container">
		<div class="text-center container-less resources-feed-heading">
			<h1 class="in-news h3 text-red font-italic" style="margin:0 0 1.5em;">In The News</h1>
      {% for news in site.data.news.main %}
			<img src="{{news.logo}}" alt="{{news.outlet}}" style="height:50px">

			<h2 class="news-feed-heading" style="margin:0.5em;">{{ news.title }}</h2>
			<p class="news-heading-intro h4 font-italic pt-3 font-weight-normal" style="margin:0.25em;">{{ news.excerpt}}</p>
      <p class="news-heading-intro text-pink" style="margin:0 0 0.5em;">{{news.date}}</p>
			<a class="btn btn-primary text-white mt-3" href="{{news.url}}" target="_blank" style="margin:0;">Read More</a>
			<br>
        {% endfor%}
		</div>
	</div>

  {% for news in site.data.news.sub %}
	<div class="fullbar-item w-100 cursor-pointer" onclick="location.href='#'">
		<div class="container">
			<div class="row py-3 py-md-5 align-items-center border-top">
				<div class="col-md-10">
					<h3 class="feed-item-heading m-0 font-weight-800">
						<a class="text-black" href="{{news.url}}" target="_blank">{{news.title}}</a>
					</h3>
				</div>
				<div class="col-md-2">
					<p class="m-0 text-pink text-uppercase" style="font-size:0.8em;"><em>{{news.outlet}}</em>, {{news.date}}</p>
				</div>
			</div>
		</div>
	</div>
  {%endfor%}

	<div class="text-center container-less resources-feed-heading">
		<h1 class="in-news h3 text-red font-italic" style="margin:0 0 1.5em;">Radio & Podcast</h1>
		</div>
{% for news in site.data.news.radio %}
<div class="fullbar-item w-100 cursor-pointer" onclick="location.href='#'">
	<div class="container">
		<div class="row py-3 py-md-5 align-items-center border-top">
			<div class="col-md-10">
				<h3 class="feed-item-heading m-0 font-weight-800">
					<a class="text-black" href="{{news.url}}" target="_blank">{{news.title}}</a>
				</h3>
			</div>
			<div class="col-md-2">
				<p class="m-0 text-pink text-uppercase" style="font-size:0.8em;"><em>{{news.outlet}}</em>, {{news.date}}</p>
			</div>
		</div>
	</div>
</div>

{%endfor%}
</section>
