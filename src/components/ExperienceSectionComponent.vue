<template>
	<Article title="Experiência">
		<ul class="list-unstyled">
			<li class="media">
				<ArticleTopic
					title="Minds at Work / BLLOG"
					subTitle="Líder de Projetos / Desenvolvedor Web"
					aside="Abr. 2019 ~ atual"
					class="row"
				>
					<ul>
						<li
							class="text-justify"
						>Jan. 2020 - Transferência da empresa Minds at Works para BLLOG com atuação e cargo mantidos.</li>
						<li
							class="text-justify"
						>Atuação em liderança de projetos de TI voltados para o setor de logística. Atuando em projetos de logística da Ambev utilizando plataforma .NET, Angular, SQL Server, linguagem C# e Typescript.</li>
					</ul>
				</ArticleTopic>
			</li>
			<li class="media">
				<ArticleTopic
					title="Superintendência de Tecnologia da Informação - UFF"
					subTitle="Desenvolvedor Web"
					aside="Ago. 2015 ~ Mar. 2019"
					class="row"
				>
					<ul>
						<li class="text-justify">
							Desenvolvimento, manutenção e suporte de sistemas Web, utilizando
							tecnologias como Java, Spring Framework, Hibernate, JUnit, Oracle, HTML,
							CSS e Javascript.
						</li>
						<li class="text-justify">
							Ago. 2017 - Atuação como líder técnico Java no desenvolvimento,
							manutenção, suporte de projetos acadêmicos e na participação e criação
							de treinamentos para as equipes.
						</li>
					</ul>
				</ArticleTopic>
			</li>
			<li class="media list-style__none">
				<ArticleTopic
					subTitle="Estagiário em Serviços Web e Front-end"
					aside="Nov. 2013 ~ Jul. 2015"
					class="row"
				>
					<ul>
						<li
							class="text-justify"
						>Criação, manutenção e suporte aos sites da universidade, que utilizam plataformas CMS (Joomla! e Wordpress). Desenvolvimento de layouts com HTML e CSS, criação de banners e materiais gŕaficos para websites.</li>
					</ul>
				</ArticleTopic>
			</li>
		</ul>
	</Article>
</template>

<script>
import Article from "@/components/ArticleComponent";
import ArticleTopic from "@/components/ArticleTopicComponent";

export default {
	name: "ExperienceSection",
	components: {
		Article,
		ArticleTopic
	}
};
</script>

<style scoped>
.list-style__none {
	list-style: none;
}
</style>

