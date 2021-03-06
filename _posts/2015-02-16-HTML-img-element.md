---
title: Web图像
time: 2015.02.16 
layout: post
tags:
- HTML
- 笔记
excerpt: 本文主要记录了三种常用的图像格式JPEG、PNG、GIF。
---
#浏览器如何处理图像
HTML是纯文本，图像绝对无法作为页面的一部分，图像是单独存在的。浏览器是在下载了HTML文件并开始显示页面后，才向WEB服务器同时请求多个图像，然后逐个获取图像，每得到一个图像并显示完图像后，再转向下一个图像，重复这个过程。

#`<img>`元素
`<img>`：内联元素、void元素，常与`src`属性一起使用，指定标记显示的图像的文件名。如`<img src="photo.gif">`。

`alt`属性：在图像服务器宕机或者连接速度太慢，导致浏览器无法显示图像时，可能会显示描述这个图像的一些文本。

`width`&`height`属性：提前告诉浏览器页面中图像的大小，帮助浏览器确定要为图像预留多大的空间。如`<img src="drinks.gif" width="48" height="100">`

浏览器宽度通常设置为800-1280像素之间，LOGO宽度在100-200像素之间。



<table>
   <tr>
      <th>JPEG</th>
	  <th>PNG</th>
	  <th>GIF</th>
   </tr>
   <tr>
      <td>最适合连续色调图像，如照片和复杂图像</td>
	  <td>最适合单色图像和线条构成的图像，如单色图像、LOGO和几何图形</td>
	  <td>类似于PNG，最适合单色图像和线条构成的图像，如单色图像、LOGO和几何图形</td>
   </tr>
   <tr>
      <td>表示包含1600多万种不同颜色的图像</td>
	  <td>表示包含上百万种不同颜色的图像。PNG-8(支持数百万种颜色)、PNG-24(支持数千种颜色)、PNG-32(支持256种颜色)</td>
	  <td>表示最多256种不同颜色的图像</td>
   </tr>
   <tr>
      <td>“有损”格式，缩小文件大小时会丢失图像的一些信息</td>
	  <td>“无损”格式，缩小文件大小时不会丢失信息</td>
	  <td>“无损”格式</td>
   </tr>
   <tr>
      <td>不支持透明度</td>
	  <td>允许将颜色设为"透明"，使图像下面的内容可以显示出来</td>
	  <td>支持透明度，但只允许一种颜色设为透明。如果希望图像有无锯齿透明区，就不能只设置一种颜色透明</td>
   </tr>
   <tr>
      <td>文件比较小，以便WEB页面更高效显示。</td>
	  <td>与相应的JPEG文件比，PNG文件更大；与相应的GIF比，取决于使用的颜色数，可能小也可以大</td>
	  <td>往往比相应的JPEG文件大</td>
   </tr>
   <tr>
      <td>不支持支动画</td>
	  <td>不支持动画</td>
	  <td>支持动画</td>
   </tr>   
</table>