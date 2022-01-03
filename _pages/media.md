---
layout: single
permalink: /media/
---
<section class="blog-cat mt-5 pb-5">
	<div class="container mb-5">
		<div class="text-center container-less resources-feed-heading">
			<h1 class="in-news h3 text-red font-italic">In The News</h1>
      {% for news in site.data.news.main %}
			<h2 class="news-feed-heading h1 lead">{{ news.title }}</h2>
			<p class="news-heading-intro h4 font-italic pt-3 font-weight-normal">{{ news.excerpt}}</p>
      <p class="news-heading-intro text-pink"><em>{{news.outlet}}</em></p>
			<a class="btn btn-primary text-white mt-3" href="{{news.url}}" target="_blank">Read More</a>
        {% endfor %}
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
					<p class="m-0 text-pink text-uppercase"><em>{{news.outlet}}</em>, {{news.date}}</p>
				</div>
			</div>
		</div>
	</div>
  {%endfor%}
</section>
