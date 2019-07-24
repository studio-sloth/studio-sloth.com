<script>
	export let segment;
</script>

<style>
	
</style>

<nav>
	<ul id="nav" class="sidenav sidenav-fixed" style="transform: translateX(0px);">
		
		<li class="bold"><a class='waves-effect waves-teal {segment === undefined ? "selected" : ""}' href='.'>home</a></li>
		<li class="bold"><a class='waves-effect waves-teal {segment === "about" ? "selected" : ""}' href='about'>about</a></li>
		<li class="bold"><a class='waves-effect waves-teal {segment === "contact" ? "selected" : ""}' href='contact'>contact</a></li>

		<!-- for the blog link, we're using rel=prefetch so that Sapper prefetches
		     the blog data when we hover over the link or tap it on a touchscreen -->
		<li class="bold"><a rel=prefetch class='{segment === "blog" ? "selected" : ""}' href='blog'>blog</a></li>
	</ul>
</nav>
