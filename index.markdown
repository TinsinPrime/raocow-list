---
layout: page
---
{%include header.html%}
<title>The raocow List</title>


<h1 style="text-align: center;">raocow's Let's Plays (in Chronological Order)</h1>
<table class="table table-sm table-hover">
<colgroup>
<col class="text-center"/>
<col class="text-center"/>
<col class="text-center"/>
<col class="text-center"/>
<col class="text-center"/>
</colgroup>

<thead>
<tr>
	<th class="text-center">Title</th>
	<th class="text-center">Link</th>
	<th class="text-center">Playlist</th>
	<th class="text-center">Start</th>
	<th class="text-center">End</th>
</tr>
</thead>

<tbody>
{% for game in site.data.list %}
<tr>
	<td class="text-center">{{game.name}}</td>
	<td class="text-center"><a href="{{game.link}}">{{game.link-type}}</a></td>
	<td class="text-center"><a href="{{game.pl}}">{{game.pl-src}}</a></td>
	{% if game.start == game.end %}
	<td class="text-center" colspan=2>{{game.start}}</td>	
	{% else %}
	<td class="text-center">{{game.start}}</td>
	<td class="text-center">{{game.end}}</td>
	{% endif %}
</tr>
{% endfor %}