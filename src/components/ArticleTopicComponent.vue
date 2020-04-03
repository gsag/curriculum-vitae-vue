<template lang="html">
	<section>
		<div class="col-12 col-md-8">
			<h3>{{title}}</h3>
			<h4 class="text-muted">{{subTitle}}</h4>
			<slot></slot>
		</div>
		<div class="col-12 col-md-4 d-flex flex-column align-items-start align-items-sm-start align-items-md-end justify-content-start">
			Ago. 2015 ~ Abr. 2019
		</div>
	</section>
</template>

<script>
export default {
	name: "ArticleTopic",
	props: ["title", "subTitle"]
};
</script>

<style lang="css" scoped>
.text-muted {
	color: #6c757d;
}
</style>

