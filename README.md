# Card Deck Slideshow #

*Description:*  This content slideshow script utilizes CSS3 transform to rotate and "unhinge" each slide to show the next, similar to a stacked pile of cards. At the heart of it all, however, is a versatile slideshow that supports both auto and manual mode, persistence of the last viewed slide, inline or ajax content, and more. The "unhinge" effect works in all browsers that support CSS3 transform, namely, IE10, all modern versions of FF, Chrome, and Safari, including their mobile versions. In non supporting browsers (such as IE9), a standard slide down effect is employed instead.

## Directions ##

*Step 1:* This script uses the following external files:

+ jQuery 1.7 or above (served via Google CDN)
+ carddeckslideshow.js
+ carddeckslideshow.css

*Step 2:* Add the below code to the HEAD section of your page:

	<link rel="stylesheet" href="carddeckslideshow.css" />
	
	<style>
	
	.stackcontainer{
	margin: 100px 0 10px 0;
	}
	
	#demo1{
	width: 250px; 
	height: 200px;
	margin-left: 100px;
	}
	
	#demo2{
	width: 350px;
	height: 200px;
	}
	
	
	#demo3 > div.inner{
	background: lightyellow;
	}
	
	#demo1 h4, #demo3 h4{
	margin: 0;
	}
	
	
	</style>
	
	<script type="text/javascript" src="http://ajax.googleapis.com/ajax/libs/jquery/1.8/jquery.min.js"></script>
	
	<script src="carddeckslideshow.js">
	
	/*
	* Card Deck Slideshow (c) Dynamic Drive (www.dynamicdrive.com)
	* Last updated: May 2nd, 13'
	* Visit http://www.dynamicdrive.com/ for this script and 100s more.
	*/
	
	</script>
	
	<script>
	
	var demo1 = new carddeckslideshow({
		id: 'demo1',
		autoplay: true,
		cycles: 2,
		persist: false
	})
	
	var demo2 = new carddeckslideshow({
		id: 'demo2',
		hingepoint: 'top right',
		fxduration: 1000
	})
	
	var demo3 = new carddeckslideshow({
		id: 'demo3',
		hingepoint: '50% 60%',
		source: 'stackedcontents.txt',
		fxduration: 2000,
		pause: 1000
	})
	
	</script>


*Step 3:* Then, add the below sample markup to your page:

	<div id="demo1" class="stackcontainer">
	
		<div class="inner">
			<div>
			 <b>Coconuts</b> are different from any other fruits because they contain a large quantity of "water" and when immature they are known as tender-nuts or jelly-nuts and may be harvested for drinking. The clear liquid coconut water within is a refreshing drink.
			</div>
		</div>
		
		<div class="inner">
			<img src="coconut.jpg" />
		</div>
		
		<div class="inner">
			<div>
			<b>Woodland</b> is a low-density forest forming open habitats with plenty of sunlight and limited shade. Woodlands may support an understory of shrubs and herbaceous plants including grasses. Woodland may form a transition to shrubland under drier conditions.
			</div>
		</div>
		
		<div class="inner">
			<img src="forest.jpg" />
		</div>
		
		<div class="inner">
			<div>
			Ontario is a province located in the central part of Canada, the largest by population and second largest, after Quebec in total area. Toronto, the capital of Ontario, is the centre of Canada's financial services and banking industry.
			</div>
		</div>
	
	</div>
	
	<div style="margin-top:1em; margin-left:100px">
	<a href="javascript:demo1.navigate('prev')">Previous Slide</a> / <a href="javascript:demo1.navigate('next')">Next Slide</a> / <a href="javascript:demo1.getajaxcontent('stackedcontents.txt')">Load Ajax Contents</a>
	</div>
	
	
	<div id="demo2" class="stackcontainer">
	
		<div class="inner">
			<img src="river.jpg" />
		</div>
	
		<div class="inner">
			<img src="whitechairs.jpg" />
		</div>
	
		<div class="inner">
			<img src="sunnypath.jpg" />
		</div>
	
		<div class="inner">
			<img src="mushroom.jpg" />
		</div>
	
	</div>
	
	<div style="margin-top:1em">
	<a href="javascript: demo2.navigate('prev')">Previous Slide</a> | <a href="javascript: demo2.navigate('next')">Next Slide</a> / <a href="javascript: demo2.userplay()">Play Slideshow</a> / <a href="javascript: demo2.userpause()">Stop</a>
	</div>
	
	
	
	<div id="demo3" class="stackcontainer">
	
		<div class="inner">
			<img src="river.jpg" />
		</div>
	
		<div class="inner">
			<img src="whitechairs.jpg" />
		</div>
	
		<div class="inner">
			<img src="sunnypath.jpg" />
		</div>
	
		<div class="inner">
			<img src="mushroom.jpg" />
		</div>
	
	</div>
	
	
	<div style="margin-top:1em">
	<a href="javascript: demo3.navigate('prev')">Previous Slide</a> / <a href="javascript: demo3.navigate('next')">Next Slide</a>
	</div>

## Card Deck Slideshow set up ##

See script project page for additional details on setup and documentation: <http://www.dynamicdrive.com/dynamicindex17/carddeckslideshow.htm>
