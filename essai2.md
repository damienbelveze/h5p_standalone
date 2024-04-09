---
title: essai2
author: Damien Belvèze
---


<div id="h5p-container-8"></div> // YOUR H5P FILE (THIS IS A FOLDER PATH)
<script>
  (function() {
    let h5pContainer = document.getElementById("h5p-container-8"); // div tag ID
    let h5pJsonPath = 'H5P/consequences'; // YOUR H5P FILE (THIS IS A FOLDER PATH)

    if (!document.getElementById('h5p-bundle-js')) {
      let script = document.createElement('script');
      script.id = 'h5p-bundle-js';
      script.src = 'libs/h5p/main.bundle.js';
      h5pContainer.parentNode.insertBefore(script, h5pContainer.nextSibling);
    }

    window.addEventListener("load", function() {
      const options = {
        h5pJsonPath: h5pJsonPath,
        frameJs: 'libs/h5p/frame.bundle.js',
        frameCss: 'libs/h5p/styles/h5p.css',
      }
      new H5PStandalone.H5P(h5pContainer, options);
    });
  }) ();
</script>