---
layout: "v2_fluid/docs_base"
version: "3.1.1"
versionHref: "/docs/v2/native"
path: ""
category: native
id: "network"
title: "Network"
header_sub_title: "Class in module "
doc: "Network"
docType: "class"
---







<h1 class="api-title">
  
  Network
  

  

  </h1>

<a class="improve-v2-docs" href="http://github.com/driftyco/ionic-native/edit/master/src/@ionic-native/plugins/network/index.ts#L5">
  Improve this doc
</a>



<!-- decorators -->





<pre><code>$ ionic plugin add cordova-plugin-network-information
$ npm install --save @ionic-native/network
</code></pre>
<p>Repo:
  <a href="https://github.com/apache/cordova-plugin-network-information">
    https://github.com/apache/cordova-plugin-network-information
  </a>
</p>

<!-- description -->

<p>Requires Cordova plugin: cordova-plugin-network-information. For more info, please see the <a href="https://github.com/apache/cordova-plugin-network-information">Network plugin docs</a>.</p>


<!-- @platforms tag -->
<h2>Supported platforms</h2>

<ul>
  <li>Amazon Fire OS</li><li>iOS</li><li>Android</li><li>BlackBerry 10</li><li>Windows Phone 7</li><li>Windows Phone 8</li><li>Windows</li><li>Firefox OS</li><li>Browser</li>
</ul>

<!-- @platforms tag end -->


<!-- if doc.decorators -->

<!-- @usage tag -->

<h2>Usage</h2>

<pre><code class="lang-typescript">import { Network } from &#39;@ionic-native/network&#39;;

constructor(private network: Network) { }

...

// watch network for a disconnect
let disconnectSubscription = this.network.onDisconnect().subscribe(() =&gt; {
  console.log(&#39;network was disconnected :-(&#39;);
});

// stop disconnect watch
disconnectSubscription.unsubscribe();


// watch network for a connection
let connectSubscription = this.network.onConnect().subscribe(() =&gt; {
  console.log(&#39;network connected!&#39;); 
  // We just got a connection but we need to wait briefly
   // before we determine the connection type.  Might need to wait 
  // prior to doing any api requests as well.
  setTimeout(() =&gt; {
    if (Network.type === &#39;wifi&#39;) {
      console.log(&#39;we got a wifi connection, woohoo!&#39;);
    }
  }, 3000);
});

// stop connect watch
connectSubscription.unsubscribe();
</code></pre>




<!-- @property tags -->




<!-- methods on the class -->

<h2>Instance Members</h2>
<div id="type"></div>
<h3>
  <code>type</code>
  

</h3>
Connection type


<div class="return-value" markdown="1">
  <i class="icon ion-arrow-return-left"></i>
  <b>Returns:</b> 
<code>string</code> 
</div><div id="downlinkMax"></div>
<h3>
  <code>downlinkMax</code>
  

</h3>
Downlink Max Speed


<div class="return-value" markdown="1">
  <i class="icon ion-arrow-return-left"></i>
  <b>Returns:</b> 
<code>string</code> 
</div><div id="onchange"></div>
<h3>
  <code>onchange()</code>
  

</h3>
Returns an observable to watch connection changes


<div class="return-value" markdown="1">
  <i class="icon ion-arrow-return-left"></i>
  <b>Returns:</b> 
<code>Observable&lt;any&gt;</code> 
</div><div id="ontypechange"></div>
<h3>
  <code>ontypechange()</code>
  

</h3>
Returns an observable to watch connection type changes


<div class="return-value" markdown="1">
  <i class="icon ion-arrow-return-left"></i>
  <b>Returns:</b> 
<code>Observable&lt;any&gt;</code> 
</div><div id="onDisconnect"></div>
<h3>
  <code>onDisconnect()</code>
  

</h3>
Get notified when the device goes offline


<div class="return-value" markdown="1">
  <i class="icon ion-arrow-return-left"></i>
  <b>Returns:</b> 
<code>Observable&lt;any&gt;</code> Returns an observable.
</div><div id="onConnect"></div>
<h3>
  <code>onConnect()</code>
  

</h3>
Get notified when the device goes online


<div class="return-value" markdown="1">
  <i class="icon ion-arrow-return-left"></i>
  <b>Returns:</b> 
<code>Observable&lt;any&gt;</code> Returns an observable.
</div>

<h2><a class="anchor" name="advanced" href="#advanced"></a>Advanced</h2>
<p>The <code>type</code> property will return one of the following connection types: <code>unknown</code>, <code>ethernet</code>, <code>wifi</code>, <code>2g</code>, <code>3g</code>, <code>4g</code>, <code>cellular</code>, <code>none</code></p>


<!-- other classes -->

<!-- end other classes -->

<!-- interfaces -->

<!-- end interfaces -->

<!-- related link --><!-- end content block -->


<!-- end body block -->

