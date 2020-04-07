<template lang="html">
	<header>
		<div class="header-main-info col-9 col-xs-10 col-sm-12 col-md-8 d-flex flex-column align-items-start">
			<h1>{{headerTitle}}</h1>
			<h2 class="d-flex flex-xs-row flex-sm-column flex-md-row">
		<span v-for="subtitle in headerSubTitles"
			v-bind:key="subtitle">
			{{subtitle}}
		</span>
		</h2>
		</div>
		<div class="header-side-info col-3 col-sm-12 col-md-4 d-flex flex-column align-items-end align-items-xs-end align-items-sm-start align-items-md-end justify-content-center">
			<span class="header-side-info__email">
				{{headerEmail}}
			</span>
			<span class="header-side-info__phone">
				{{formatPhone(headerPhone)}}
			</span>
			<span class="header-side-info__city">
				{{headerCity}}
			</span>
		</div>
	</header>
</template>

<script>
export default {
	name: "Header",
	data: () => {
		return {
			headerTitle: "Guilherme da Silva Alves Gonçalves",
			headerSubTitles: ["Líder de Projetos", "Desenvolvedor Web"],
			headerEmail: "gsag.dh@gmail.com",
			headerPhone: 21996760304,
			headerCity: "Niterói / RJ"
		};
	},
	methods: {
		formatPhone: phoneNumber => {
			let stringPhoneNumber = phoneNumber.toString();
			let formatedPhone = stringPhoneNumber.replace(
				/^(?:(\d{2})(\d{1})?(\d{4})(\d{4}))$/g,
				"($1) $2 $3-$4"
			);
			return formatedPhone;
		}
	}
};
</script>

<style lang="css" scoped>
h1 {
	font-weight: bold;
}
h2,
span {
	font-weight: 300;
}
header {
	padding: 0 1em;
}
header::after {
	content: "";
	height: 2px;
	background-color: var(--main-text-color);
	width: 100%;
	margin: 0.5em 1em;
}
@media only screen and (min-width: 800px) {
	h2 > span:not(:first-child)::before {
		content: "|";
		margin: 0 0.25em 0 0.5em;
	}
}
@media print and (max-width: 600px) {
	h2 > span:not(:first-child)::before {
		content: "|";
		margin: 0 0.25em 0 0.5em;
	}
}
</style>
