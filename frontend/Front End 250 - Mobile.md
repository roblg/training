# Front End 250: Mobile all the Things


## what the what

1. terms to know:
	* viewport (the size of the browser window)
	* **TODO** ADD MORE?
2. types of layout:
	* fixed: pixel-based; like it sounds. never changes.
	* fluid: percentage-based; proportional layout changes with viewport
	* adaptive: uses media queries to implement multiple fixed layouts
	* responsive: uses media queries to implement multiple fluid layouts


## media queries

1. what is a media query? 
2. state of the internet
	* browser support: no IE8
	* redfin support: no IE <10 unless otherwise specified
3. breakpoints
4. syntax / convention at Redfin
	* Media Query mixin that builds for IE8+


## javascript PE / degradation

Ideally, pages viewed on mobile devices should be as lightweight as possible. This includes javascript. Most mobile browsers block page rendering or interaction while javascript runs, as they currently have performance limitations compared to even the slowest desktops. [Read More][sencha-perf]

> "Mobile JavaScript + mobile DOM access is getting progressively faster, but you should still treat the iPhone 5 as if it’s a Chrome 1.0 browser on a 2008-era desktop (aka 5–10x faster than desktop IE8)." – [Sencha][sencha-perf]

[100,000 words on why web apps are slow][sealed]

* has.js


## mobile web at Redfin

We have two main ways to handle the construction of mobile web pages and apps:

1. Mobile First
	* Build the minimum viable product first
	* Build it on mobile
	* Use PE to improve the experience for tablet and desktop
2. Mobile Last
	* Build a desktop page
	* Shoehorn in some CSS to make it look right
	* Attempt to use has.js after the fact to trim out the bits that perform poorly

From a performance standpoint, Mobile First is the preferable approach. It's only really practical on a clean-sheet design, though.




 [sencha-perf]: http://www.sencha.com/blog/5-myths-about-mobile-web-performance/
 [sealed]: http://sealedabstract.com/rants/why-mobile-web-apps-are-slow/