---
layout:  page
title: Einstein's Geometric Theory of Gravity
published: true 
---
# {{page.title}}
<hr>

<script>
function show_pdf(mat_date){
	mats=mat_date.firstElementChild
	if (mats.style.display=="block"){
		mats.style.display="none";
		}	
	else{
		mats.style.display="block";
		}
	}
</script>

<section>
<h2>课程资料：</h2>
点击相应上课时间，查看及下载课件资料。
<ol id="materials-all" >
	<li onclick="show_pdf(this)">
		{% assign dir_date = '' %}
		{% for file in site.static_files %}
			{% if file.path contains '/gr/' %}
				{% capture file_date %}
					{{file.path | slice: 4, 4}} 
				{% endcapture %}
				{% if file_date != dir_date %}	
					{% if dir_date != '' %}	
							</ul>
						</li>
			    		<li onclick="show_pdf(this)">	
					{% endif %}
					{% assign dir_date = file_date %}
			    	{{dir_date}}
						<ul class="materials-day">
				{% endif %}
				<li><a href='{{file.path}}' target='_blank'>{{file.name}}</a></li>
			{% endif %}
		{% endfor %}
		</ul>	
	</li>
</ol>
</section>

## 课程通知：
