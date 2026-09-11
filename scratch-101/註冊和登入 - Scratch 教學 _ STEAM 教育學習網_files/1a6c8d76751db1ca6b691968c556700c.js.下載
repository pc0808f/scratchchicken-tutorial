(function(){'use strict';var d=class{constructor(a){this.body=a}dispatchEvent(a,b){this.body.dispatchEvent(new CustomEvent(a,{detail:b}))}};function e(a){if(a.l.offsetWidth<=1||a.l.offsetHeight<=1)return!1;a.i.remove();a.context.dispatchEvent("spanReady");return!0}
var k=class{constructor(a){this.context=a;this.config={v:!1,u:100};this.l=document.createElement("span");this.i=document.createElement("div");this.l.style.fontSize="6px";this.l.textContent="go";this.i.style.position="absolute";this.i.style.top="100%";this.i.style.left="100%";this.i.style.width="1px";this.i.style.height="0";this.i.style.overflow="hidden";this.i.style.visibility="hidden";this.i.appendChild(this.l)}wait(){if(!this.config.v&&(this.context.dispatchEvent("spanStart"),this.context.body.appendChild(this.i),
!e(this)))return new Promise(a=>{var b=setInterval(()=>{e(this)&&(clearInterval(b),a())},this.config.u)})}};/*

 Copyright The Closure Library Authors.
 SPDX-License-Identifier: Apache-2.0
*/
function l(a,b){if(a.m===1){a.dispatchEvent("overallStart");var c;let h;(c=a.o)==null||(h=c.b0)==null||h.call(c)}c=(new k(a.context)).wait();a.dispatchEvent("browserStart");var f,g;(f=a.o)==null||(g=f.b1)==null||g.call(f);a.dispatchEvent("browserStartEnd");c?c.then(()=>{m(a,b)}):m(a,b)}
function m(a,b){if(a.m===b){a.dispatchEvent("browserReady");var c,f;(c=a.o)==null||(f=c.b2)==null||f.call(c);a.dispatchEvent("browserReadyEnd");a.dispatchEvent("overallReady");a.dispatchEvent("browserQuiet");var g,h;(g=a.o)==null||(h=g.b3)==null||h.call(g);a.dispatchEvent("browserQuietEnd");a.m===1&&a.dispatchEvent("overallQuiet")}}
for(var n=class{constructor(a,b){this.body=b;this.m=0;this.context=new d(b)}r(a){this.o=a;this.body.addEventListener("browserRender",()=>{++this.m;l(this,this.m)})}dispatchEvent(a){this.body.dispatchEvent(new CustomEvent(a))}},p=["mys","Engine"],q=this||self,r;p.length&&(r=p.shift());)p.length||n===void 0?q[r]&&q[r]!==Object.prototype[r]?q=q[r]:q=q[r]={}:q[r]=n;}).call(this);
