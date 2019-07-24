<svelte:head>
	<title>Studio Sloth</title>
</svelte:head>

<svelte:window bind:scrollY={y} />

<style>
	.heading {
		min-height: 95vh;
		display: flex;
		align-items: center;
		justify-content: center;
		flex-direction: column;
	}
	.content-section {
		min-height: 95vh;
	}

	.content-section img {
		max-width: 100%;
	}
</style>

<script>
	let y;

	let sections = [{
		id: "34as",
		title: "34AS",
		subtitle: "yet another Tetris game, with a twist",
		href: "/34as",
		caption: "34AS is the Metrobus line that people living \
			in Istanbul use daily to start and finish their \
			office days between two sides of the city. It's \
			hard to fit in and to keep yourself in morph.",
		image: "img/34as/34as-preview.gif",
	}]
</script>

<div class="container">
	<div class="row center heading">
		<div class="col s12 m12">
			<h1 class="header">Studio Sloth</h1>
		</div>
		<div class="col s12 m12">
			<h4 class="light">Studio Sloth is a group of indie designers and developers trying out ideas and projects, currently based in Istanbul, Turkiye.</h4>
		</div>
	</div>
	<br>
	{#each sections as s}
	<div class="row center content-section" id="{s.id}">
		<h3 class="light header">{s.title}</h3>
		<h4 class="light header">{s.subtitle}</h4>
		{#if s.caption}
		<p class="col s12 m8 offset-m2 caption">{s.caption}</p>
		{/if}
		{#if s.image}
		<img src={s.image} alt={s.title}/>
		{/if}
		<a href="{s.href}" class="col s12 m4 offset-m4 btn-large waves-effect waves-light">Go</a>
	</div>
	<br>
	{/each}
</div>

