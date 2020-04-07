<template lang="html">
	<section>
		<div class="col">
		<article>
			<h2>{{title}}</h2>
			<slot></slot>
		</article>
		</div>
	</section>    
</template>

<script>
export default {
	name: "Article",
	props: ["title"]
};
</script>

<style lang="css" scoped>
section {
	margin: 1em 0;
}
article > p {
	text-align: justify;
	text-justify: inter-word;
}
</style>

