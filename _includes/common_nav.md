{%- include ui.html %}
<nav class="_common_nav mv">
<a href="#back" onclick="{{onclick}}(function(w){var h=w.history;w.opener?w.close():h.length>1?h.back():w.location.href='/';})(window)" class="button" title="Back to previous page">👈 Back</a>{{-}}
<a href="{{ site.home_url }}/" class="button" title="Go to Home Page">Home</a>{{-}}
<a href="{{ site.baseurl }}/pages" class="button" title="Go to Pages">Pages</a>{{-}}
<a href="{{ site.baseurl }}/posts" class="button" title="Go to Posts">Posts</a>{{-}}
</nav>