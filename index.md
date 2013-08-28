---
layout: page
title: 首页
tagline: keep going
---



<div style="margin: 0 auto;">
	<div style="float: right; width: 200px;">
		<h3>最新文章</h3>
		<hr />
		<ul class="tag_box inline">
			{% for post in site.posts limit:10 %}
			<p><a href="{{ post.url }}">{{ post.title }}</a></p>
			{% endfor %}
		</ul>
	</div>

	<div style="width: 560px; float: left;">
		<h4>技术也好，做人也好，要学会思考。</h4>
		<img src="http://i403.photobucket.com/albums/pp118/InterUrbanArt/yosemite.jpg" />
	</div>
</div>

{% include JB/setup %}

