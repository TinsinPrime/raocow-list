---
layout: default
---
{%include header.html%}

<h1 style="text-align: center;">raocow's Let's Plays (in Chronological Order)</h1>

<table class="table table-sm table-hover">
<colgroup>
<col style="text-align:center;"/>
<col style="text-align:center;"/>
<col style="text-align:center;"/>
<col style="text-align:center;"/>
<col style="text-align:center;"/>
</colgroup>

<thead>
<tr>
	<th style="text-align:center;">Title</th>
	<th style="text-align:center;">Link</th>
	<th style="text-align:center;">Playlist</th>
	<th style="text-align:center;">Start</th>
	<th style="text-align:center;">End</th>
</tr>
</thead>

<tbody>
{% for game in site.data.list %}
<tr>
	<td style="text-align:center;">{{game.name}}</td>
	<td style="text-align:center;"><a href="{{game.link}}">{{game.link-type}}</a></td>
	<td style="text-align:center;"><a href="{{game.pl}}">{{game.pl-src}}</a></td>
	<td style="text-align:center;">{{game.start}}</td>
	<td style="text-align:center;">{{game.end}}</td>
</tr>
<tr>
{% endfor %}
</tr>
