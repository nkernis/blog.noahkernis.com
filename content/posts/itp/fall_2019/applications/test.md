+++
slug = "test"
title = "test"
date = "2019-09-01T14:42:22-04:00"
author = "Noah Kernis"
tags = ["itp", "applications"]
description = "Proof Sections Works"
showFullContent = false
+++

This is proof this section works.

Post will be removed when I have real first post...

```js

  var taglines = "words"

  function randInt(max) {
    return Math.floor(Math.random() * Math.floor(max));
  };

  var oldTxt = document.getElementById("tagline").innerHTML;
  var newTxt = oldTxt.replace(/&nbsp;/g, taglines[randInt(taglines.length)]);
  document.getElementById("tagline").innerHTML = newTxt;

```