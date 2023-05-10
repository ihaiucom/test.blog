---
title: 分类
layout: page
---


<style type="text/css">


  .nav1 {
    background: #2B6600;
    border-radius: 6px 6px 6px 6px;
    box-shadow: 0 0 0 1px #5F5A4B, 1px 1px 6px 1px rgba(10, 10, 0, 0.5);
    color: #FFFFFF;
    font-weight: bold;
    margin: 12px 0px;
    padding: 5px 0px 5px 10px;
    text-shadow: 2px 2px 3px #222222;
  }

  .nav2 {
       background: #2B6695;
       border-radius: 6px 6px 6px 6px;
       box-shadow: 0 0 0 1px #5F5A4B, 1px 1px 6px 1px rgba(10, 10, 0, 0.5);
       color: #FFFFFF;
       font-weight: bold;
       margin: 18px 0px;
       padding: 8px 0px 5px 5px
       text-shadow: 2px 2px 3px #222222;
  }

  #tag_cloud a
  {
    line-height: 2rem; 
    display: block; 
    float: left; 
    padding: 0.5rem 1rem;
    margin: 0.2rem 1rem;
  }


   #tag_cloud a
  {
    line-height: 2rem; 
    display: block; 
    float: left; 
    padding: 0.5rem 1rem;
    margin: 0.2rem 1rem;
  }

  .listing-seperator{font-weight:bold;}
  .listing-item,.listing-seperator{list-style-type:none;}

  .listing-item a{
    padding:.2em 1em;

  }

  

  .listing-item
  {
      clear: both;
      border-bottom: 1px solid #9f9f9f;
      cursor: pointer;
      -webkit-user-select: none;
      -moz-user-select: none;
      text-align: left;
      color: Black;
      position: relative;
      font-family: 'Courier New', 'Courier New', monospace;
      font-size: 10pt;
      padding: 1px !important;
  }
  .listing-item-selected
  {
      background-color: #3875d7;
      color: White !important;
  }

</style>


<div id='tag_cloud'>
{% for cat in site.categories %}
<a class="nav2"  href="#{{ cat[0] }}" title="{{ cat[0] }}" rel="{{ cat[1].size }}">{{ cat[0] }} ({{ cat[1].size }})</a>
{% endfor %}
<div class="cls"></div>
</div>
<br />

<ul class="listing">
{% for cat in site.categories %}
  <li class="listing-seperator nav1" id="{{ cat[0] }}">{{ cat[0] }}</li>
{% for post in cat[1] %}
  <li class="listing-item">
  <time datetime="{{ post.date | date:"%Y-%m-%d" }}">{{ post.date | date:"%Y-%m-%d" }}</time>
  <a href="{{ post.url }}" title="{{ post.title }}">{{ post.title }}</a>
  </li>
{% endfor %}
<br />
<br />
{% endfor %}
</ul>

<!-- <script src="/media/js/jquery.tagcloud.js" type="text/javascript" charset="utf-8"></script> 
<script language="javascript">
$.fn.tagcloud.defaults = {
    size: {start: 1, end: 1, unit: 'em'},
      color: {start: '#f8e0e6', end: '#ff3333'}
};

$(function () {
    $('#tag_cloud a').tagcloud();
});
</script> -->

