<template>
  <Article class="row" title="Experiência">
    <ul class="list-unstyled">
      <li class="media">
        <ArticleTopic
          title="Superintendência de Tecnologia da Informação - UFF"
          subTitle="Desenvolvedor Web Java"
          class="row"
        >
          <ul>
            <li class="text-justify">
              Desenvolvimento, manutenção e suporte de sistemas Web, utilizando
              tecnologias como Java, Spring Framework, Hibernate, JUnit, Oracle, HTML,
              CSS e Javascript.
            </li>
            <li class="text-justify">
              Agosto de 2017 - Atuação como líder técnico Java no desenvolvimento,
              manutenção, suporte de projetos acadêmicos e na participação e criação
              de treinamentos para as equipes.
            </li>
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
}
</script>

<style scoped>
</style>

