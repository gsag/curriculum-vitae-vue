<template>
	<main id="app" class="container">
	<Header class="row"/>
	<ResumeeSection class="row"/>
	<ExperienceSection class="row"/>
	<AcademicSection class="row"/>
		<SkillsSection class="row"/>
		<ExtraInfoSection class="row"/>
  </main>
</template>

<script>
import Header from "@/components/HeaderComponent";
import ResumeeSection from "@/components/ResumeeSectionComponent";
import ExperienceSection from "@/components/ExperienceSectionComponent";
import AcademicSection from "@/components/AcademicSectionComponent";
import SkillsSection from "@/components/SkillsSectionComponent";
import ExtraInfoSection from "@/components/ExtraInfoSectionComponent";

export default {
	name: "App",
	components: {
		Header,
		ResumeeSection,
		ExperienceSection,
		AcademicSection,
		SkillsSection,
		ExtraInfoSection,
	}
};
</script>

<style lang="css">
:root {
	--main-text-color: #343a40;
	--main-bg-color: #ededed;
	--container-bg-color: #fff;
	--grey-scale-100: #F5F5F5;
	--grey-scale-300: #E0E0E0;
	--grey-scale-500: #9E9E9E;
}
html,
body {
	background-color: var(--main-bg-color);
	height: 100%;
}
#app {
	font-family: "Roboto", Arial, sans-serif;
	-webkit-font-smoothing: antialiased;
	-moz-osx-font-smoothing: grayscale;
	padding-top: 3em;
	width: 100%;
	color: var(--main-text-color);
	background-color: var(--container-bg-color);
	box-shadow: 0 4px 8px 0 rgba(0, 0, 0, 0.2), 0 6px 20px 0 rgba(0, 0, 0, 0.19);
}
@media only screen and (min-width: 800px) {
	#app {
		padding: 3em 3em;
	}
}

@media only print {
	html,
	body{
		background-color: var(--container-bg-color);
		font-size: 100%;
	}
	#app {
		padding: 1em 0;
		box-shadow: none;
	}
}
</style>
