<template lang="html">
  	<header>
		<div class="header-main-info col-8 d-flex flex-column align-items-start">
			<h1>{{headerTitle}}</h1>
			<h2>{{headerSubTitle}}</h2>
		</div>
		<div class="header-side-info col-4 d-flex flex-column align-items-end">
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
import * as VMasker from "@/assets/libs/vanilla-masker.min.js";

export default {
  name: "Header",
  data: () => {
    return {
      headerTitle: "Guilherme da Silva Alves Gonçalves",
      headerSubTitle: ["Líder de Projetos", "Desenvolvedor Web"],
      headerEmail: "gsag.dh@gmail.com",
      headerPhone: 21996760304,
      headerCity: "Niterói / RJ"
    };
  },
  methods: {
    formatPhone: phoneNumber => {
      return VMasker.toPattern(phoneNumber, "(99) 9 9999-9999");
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
</style>
