+++
slug = "making-my-site-more-accessible"
title = "Making My Site More Accessible"
date = "2019-08-31T18:20:53-04:00"
description = "How I made my site meet standards for accessibility."
author = "Noah Kernis"
tags = ["itp", "accessibility"]
showFullContent = false
+++
asd
1. Made sure list, figures (do this still), and images all have alt text
```go
    {{ if .Params.Cover}}
    <img src="{{ .Params.Cover | absURL }}" alt="{{ .Params.Alt }}" class="post-cover" />
	{{ end }}
```
2. Color Testing
	- not pretty change to inline to overrride issues
	- style="color:#FF79C6 !important; opacity: 1 !important; text-decoration: underline">

3. Screen Readers

use screen grabs from the demo site for terminal theme to show contrast issues and code without alt text, etc.

---

```
.post-tags {
	display: block;
	margin-bottom: 20px;
	font-size: 1rem;
	opacity: .5 <-- remove
}

:root {
	--accent: #FF79C6;
	--phoneWidth: (max-width:684px);
	--tabletWidth: (max-width:900px);
	--accent: #FF79C6;
	--background: #282A36;
	--color: #fff;
	--border-color: #FF79C6; <-- changhe to this
}
```