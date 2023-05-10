---
title: 目录
layout: page
---


<ul>
  {% for post in site.posts %}
    <li>
      <a href="{{ post.url }}">{{ post.title }}</a>
    </li>
  {% endfor %}
</ul>




{% for post in paginator.posts %}



<article class="post_box" >
    <div class="c-top" >
            <div class="datetime">{{ post.date | date:"%Y" }}<br />{{ post.date | date:"%m-%d" }}</div> 

            <header class="tit">
                <h2 class="h1">
                  <a href="{{ post.url }}#content" title="{{ post.title }}" rel="bookmark">{{ post.title }}</a>
                </h2>

                <aside class="iititle">
                    <span><i class="icon-user icon-large"></i>发布:<a href="tencent://message/?uin={{ post.authorQQ }}" title="发布:{{ post.author }} QQ:{{ post.authorQQ }} Email:{{ post.authorEmail }}" rel="author">{{ post.author }}</a></span>

                    <span><i class="icon-folder-open icon-large"></i>分类:<a href="/categories/#{{ post.categories }}" rel="category tag">{{ post.categories }}</a></span>

                </aside>

            </header>
    </div>



    <div class="c-con" >  
          {% if post.thumbnail %}
          <a href="{{ post.url }}#content" class="disp_a" rel="bookmark" title="">  
              <img src="{{ post.thumbnail }}" alt="{{ post.title }}" />  
          </a>
          {% endif %}

          {{ post.excerpt | remove: '<p>' | remove: '</p>' }} &raquo;
          <a href="{{ post.url }}#content" class="more-link">Read More ></a><div class="cls"></div>
    </div>


    <div class="c-bot">
            <div class="cls"></div>
    </div>
</article>
{% endfor %}
