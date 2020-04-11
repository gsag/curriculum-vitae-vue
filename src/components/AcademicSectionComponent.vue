</<template>
	<Article title="Formação Acadêmica">
		<ul class="list-unstyled">
			<li class="media">
				<ArticleTopic
					title="Mestre em Ciência da Computação (Interação Humano-Computador)"
					subTitle="Universidade Federal Fluminense"
					aside="2016 ~ 2018"
					class="row"
				/>
			</li>
			<li class="media">
				<ArticleTopic
					title="Bacharel em Sistemas de Informação"
					subTitle="Universidade Federal Fluminense"
					aside="2011 ~ 2015"
					class="row"
				/>
			</li>
		</ul>
	</Article>
</template>

<script>
import Article from "@/components/ArticleComponent";
import ArticleTopic from "@/components/ArticleTopicComponent";
export default {
	name: "AcademicSection",
	components: {
		Article,
		ArticleTopic
	}
};
</script>

<style scoped>
</style>
