---
title: posts目录
layout: page
---


<ul>
  {% for post in site.posts %}
    <li>
      <a href="{{ post.url }}">{{ post.title }}</a>
    </li>
  {% endfor %}
</ul>



{% for page in site.posts %}
<table>

    <tr>
      <td class="td_key">id</td>
      <td class="td_key">id</td>
      <td class="td_val">{{ page.id }}</td>
    </tr>

    <tr>
      <td class="td_key">标题</td>
      <td class="td_key">title</td>
      <td class="td_val"><a href="{{ page.url }}"> {{ page.title }} </a></td>
    </tr>

    <tr>
      <td class="td_key">相对路径</td>
      <td class="td_key">url</td>
      <td class="td_val"><a href="{{ page.url }}"> {{ page.url }} </a></td>
    </tr>
    
    <tr>
      <td class="td_key">源文件地址</td>
      <td class="td_key">path</td>
      <td class="td_val">{{ page.path }} </td>
    </tr>
    
    <tr>
      <td class="td_key">日期</td>
      <td class="td_key">date</td>
      <td class="td_val">{{ page.date }} </td>
    </tr>
    
    <tr>
      <td class="td_key">分类</td>
      <td class="td_key">categories</td>
      <td class="td_val">{{ page.categories }} </td>
    </tr>
    
    <tr>
      <td class="td_key">标签</td>
      <td class="td_key">tags</td>
      <td class="td_val">{{ page.tags }} </td>
    </tr>
    
    <tr>
      <td class="td_key">摘要</td>
      <td class="td_key">excerpt</td>
      <td class="td_val">{{ page.excerpt }}</td>
    </tr>
    
    {% if page.previous %} 
    <tr>
      <td class="td_key">上一篇</td>
      <td class="td_key">previous</td>
      <td class="td_val">{{ page.previous.title }} </td>
    </tr>
    {% endif %}

    {% if page.next %}
    <tr>
      <td class="td_key">下一篇</td>
      <td class="td_key">next</td>
      <td class="td_val">{{ page.next }} </td>
    </tr>
    {% endif %} 
</table>
{% endfor %}
