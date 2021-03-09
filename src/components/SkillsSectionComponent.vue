<template>
	<section>
		<Article title="Especialidades" class="col-12">
			<p>
				Desenvolvimento Web, Desenvolvimento de software, Design
				de interfaces front-end responsivas, Desenvolvimento de websites, Avaliação de
				Usabilidade e Acessibilidade.
			</p>
		</Article>

		<Article title="Competências" class="col-12">
			<p>Fluência linguística: Inglês Intermediário, Italiano Básico, Português Nativo.</p>
			<section class="row d-flex flex-row">
				<div class="col text-center skill-box skill-box__basic">Básico</div>
				<div class="col text-center skill-box skill-box__intermed">Intermediário</div>
				<div class="col text-center skill-box skill-box__advanced">Avançado</div>
			</section>

			<ArticleTopic title="Desenvolvimento Front-end" class="row row-fix">
				<section class="d-flex flex-row flex-wrap">
					<div
						v-for="skill in frontendSkills"
						v-bind:key="skill.name"
						class="col-2 text-center"
						:class="addSkillLevelStyle(skill.level)"
					>{{skill.name}}</div>
				</section>
			</ArticleTopic>

			<ArticleTopic title="Desenvolvimento Back-end" class="row row-fix">
				<section class="d-flex flex-row flex-wrap">
					<div
						v-for="skill in backendSkills"
						v-bind:key="skill.name"
						class="col-2 text-center"
						:class="addSkillLevelStyle(skill.level)"
					>{{skill.name}}</div>
				</section>
			</ArticleTopic>

			<ArticleTopic title="Outros" class="row row-fix">
				<section class="d-flex flex-row flex-wrap">
					<div
						v-for="skill in otherSkills"
						v-bind:key="skill.name"
						class="col-2 text-center"
						:class="addSkillLevelStyle(skill.level)"
					>{{skill.name}}</div>
				</section>
			</ArticleTopic>
		</Article>
	</section>
</template>

<script>
import Article from "@/components/ArticleComponent";
import ArticleTopic from "@/components/ArticleTopicComponent";
export default {
	name: "SkillsSection",
	components: {
		Article,
		ArticleTopic
	},
	data: () => {
		return {
			frontendSkills: [
				{
					name: "HTML",
					level: "advanced"
				},
				{
					name: "CSS",
					level: "advanced"
				},
				{
					name: "WCAG/ARIA",
					level: "intermed"
				},
				{
					name: "Javascript",
					level: "intermed"
				},
				{
					name: "ES6+",
					level: "intermed"
				},
				{
					name: "Typescript",
					level: "intermed"
				},
				{
					name: "Bootstrap",
					level: "advanced"
				},
				{
					name: "JQuery",
					level: "intermed"
				},
				{
					name: "SASS/SCSS",
					level: "intermed"
				},
				{
					name: "AngularJs",
					level: "basic"
				},
				{
					name: "Angular",
					level: "intermed"
				},
				{
					name: "VueJS",
					level: "basic"
				},
				{
					name: "NPM",
					level: "basic"
				},
				{
					name: "Webpack",
					level: "basic"
				},
				{
					name: "Jasmine",
					level: "basic"
				},
				{
					name: "Karma",
					level: "basic"
				},
				{
					name: "Jest",
					level: "basic"
				},
				{
					name: "Websockets",
					level: "basic"
				}
			],
			backendSkills: [
				{
					name: "C#",
					level: "intermed"
				},
				{
					name: ".NET Core",
					level: "intermed"
				},
				{
					name: ".NET Framework",
					level: "intermed"
				},
				{
					name: "Java",
					level: "intermed"
				},
				{
					name: "Spring Framework",
					level: "intermed"
				},
				{
					name: "Node JS",
					level: "basic"
				},
				{
					name: "SQL Server DB",
					level: "intermed"
				},
				{
					name: "Oracle DB",
					level: "intermed"
				},
				{
					name: "Azure Services",
					level: "basic"
				}
			],
			otherSkills: [
				{
					name: "Git",
					level: "intermed"
				},
				{
					name: "Mercurial",
					level: "intermed"
				},
				{
					name: "Linux",
					level: "intermed"
				},
				{
					name: "Docker",
					level: "basic"
				},
				{
					name: "RabbitMQ",
					level: "basic"
				},
				{
					name: "Dart / Flutter",
					level: "basic"
				},
			]
		};
	},
	methods: {
		addSkillLevelStyle: level => {
			return "skill-box skill-box__" + level;
		}
	}
};
</script>

<style scoped>
.text-center {
	text-align: center;
}
.skill-box {
	border: 1px solid var(--main-text-color);
}
.skill-box__basic {
	background-color: var(--grey-scale-100);
}
.skill-box__intermed {
	background-color: var(--grey-scale-300);
}
.skill-box__advanced {
	background-color: var(--grey-scale-500);
}
.row-fix{
	margin-left: -15px;
	margin-right: -15px;
}
</style>
