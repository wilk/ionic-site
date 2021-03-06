---
layout: "v2_fluid/docs_base"
version: "3.1.1"
versionHref: "/docs/v2/native"
path: ""
category: native
id: "app-availability"
title: "App Availability"
header_sub_title: "Class in module "
doc: "App Availability"
docType: "class"
---







<h1 class="api-title">
  
  App Availability
  

  

  </h1>

<a class="improve-v2-docs" href="http://github.com/driftyco/ionic-native/edit/master/src/@ionic-native/plugins/app-availability/index.ts#L1">
  Improve this doc
</a>



<!-- decorators -->





<pre><code>$ ionic plugin add cordova-plugin-appavailability
$ npm install --save @ionic-native/app-availability
</code></pre>
<p>Repo:
  <a href="https://github.com/ohh2ahh/AppAvailability">
    https://github.com/ohh2ahh/AppAvailability
  </a>
</p>

<!-- description -->

<p>This plugin allows you to check if an app is installed on the user&#39;s device. It requires an URI Scheme (e.g. twitter://) on iOS or a Package Name (e.g com.twitter.android) on Android.</p>
<p>Requires Cordova plugin: cordova-plugin-appavailability. For more info, please see the <a href="https://github.com/ohh2ahh/AppAvailability">AppAvailability plugin docs</a>.</p>


<!-- @platforms tag -->
<h2>Supported platforms</h2>

<ul>
  <li>Android</li><li>iOS</li>
</ul>

<!-- @platforms tag end -->


<!-- if doc.decorators -->

<!-- @usage tag -->

<h2>Usage</h2>

<pre><code class="lang-typescript">import { AppAvailability } from &#39;@ionic-native/app-availability&#39;;
import { Platform } from &#39;ionic-angular&#39;;

constructor(private appAvailability: AppAvailability, private platform: Platform) { }

...

let app;

if (this.platform.is(&#39;ios&#39;)) {
  app = &#39;twitter://&#39;;
} else if (this.platform.is(&#39;android&#39;)) {
  app = &#39;com.twitter.android&#39;;
}

this.appAvailability.check(app)
  .then(
    (yes: string) =&gt; console.log(app + &#39; is available&#39;),
    (no: string) =&gt; console.log(app + &#39; is NOT available&#39;)
  );
</code></pre>




<!-- @property tags -->




<!-- methods on the class -->

<h2>Instance Members</h2>
<div id="check"></div>
<h3>
  <code>check(app)</code>
  

</h3>
Checks if an app is available on device
<table class="table param-table" style="margin:0;">
  <thead>
  <tr>
    <th>Param</th>
    <th>Type</th>
    <th>Details</th>
  </tr>
  </thead>
  <tbody>
  
  <tr>
    <td>
      app
      
    </td>
    <td>
      
<code>string</code>
    </td>
    <td>
      <p>Package name on android, or URI scheme on iOS</p>

      
      
    </td>
  </tr>
  
  </tbody>
</table>

<div class="return-value" markdown="1">
  <i class="icon ion-arrow-return-left"></i>
  <b>Returns:</b> 
<code>Promise&lt;boolean&gt;</code> 
</div>



<!-- other classes -->

<!-- end other classes -->

<!-- interfaces -->

<!-- end interfaces -->

<!-- related link --><!-- end content block -->


<!-- end body block -->

