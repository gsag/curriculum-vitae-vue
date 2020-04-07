<template lang="html">
	<section>
		<div class="col-12 col-md-8">
			<h3 v-if="title">
				{{title}}
			</h3>
			<h4 class="text-muted">
				{{subTitle}}
				<small class="show-on-print">({{aside}})</small>
			</h4>
			<slot></slot>
		</div>
		<div class="col-12 col-md-4 d-flex flex-column align-items-start align-items-sm-start align-items-md-end justify-content-start">
			<span class="hide-on-print">{{aside}}</span>
		</div>
	</section>
</template>

<script>
export default {
	name: "ArticleTopic",
	props: ["title", "subTitle", "aside"]
};
</script>

<style lang="css" scoped>
.text-muted {
	color: #6c757d;
}
@media screen {
	.show-on-print {
		display: none;
	}
	.hide-on-print {
		display: inline-flex;
	}
}
@media only print {
	.show-on-print {
		display: inline-flex;
	}
	.hide-on-print {
		display: none;
	}
}
</style>

