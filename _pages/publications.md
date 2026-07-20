---
layout: page
permalink: /publications/
title: Publications
description: 
nav: true
nav_order: 2
---
<style>
.post-title, .page-title, h2.bibliography { font-weight: 700 !important; }
</style>
Please check the up-to-date list on <a href='https://scholar.google.com.hk/citations?user=C2yZktgAAAAJ&hl=en' style="color:#36AE7C;" >Google Scholar</a>.
<!-- _pages/publications.md -->
<div class="publications">
This Software was developed under Research Sponsored by:
<br>
National Science Foundation (NSF)
<br>
Army Research Office (ARO)
<br>
Office of Naval Research (ONR)
<br>
<br>
Note: Only a few example papers come with code. If you have trouble making it work, please figure it out yourself.  The methods are explained in the papers.

<br>
<br>

Note: Publications are listed by their publication dates unless they have not yet been published.

<br>
<br>


<h2 class="bibliography">Books</h2>
{% bibliography --query @book %}
<h2 class="bibliography">Book Chapters</h2>
{% bibliography --query @incollection %}
<h2 class="bibliography">Journal & Conference Publications</h2>
{% bibliography --query @article, @inproceedings %}
</div>


Copyright © 2026 Bosen Lian. All rights reserved.