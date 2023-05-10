---
title: 静态文件列表
layout: page
---


<table>
  <thead>
    <tr>
      <th>路径</th>
      <th>修改时间</th>
      <th>文件名称（带扩展名）</th>
      <th>文件名称（不带扩展名）</th>
      <th>扩展名</th>
    </tr>
    
  </thead>
  
  <tbody>
    <tr>
      <th>path</th>
      <th>modified_time</th>
      <th>name</th>
      <th>basename</th>
      <th>extname</th>
    </tr>

    {% for file in site.static_files %}

    <tr>
        <td><a href="{{ file.path }}" target="_blank">{{ file.path }} </a></td>
        <td> {{ file.modified_time }} </td>
        <td> {{ file.basename }} </td>
        <td> {{ file.extname }} </td>
    </tr>

    {% endfor %}
  </tbody>
</table>

