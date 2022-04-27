<script setup lang="ts">
import { RouterLink } from 'vue-router';
import HeaderIcon from '@/components/HeaderIcon.vue';
</script>

<template>
	<nav id="pageHeader">
		<RouterLink to="/" id="homeLink">Logan Gerber</RouterLink>
		<div id="spacer"></div>
		<HeaderIcon id="resumeLink" href="public/Resume.pdf" :icon="'file'" title="Resume">Resumé
		</HeaderIcon>
		<HeaderIcon id="githubLink" href="https://github.com/LoganGerber" :icon="['fab', 'github-square']"
			title="Github">Github</HeaderIcon>
		<HeaderIcon id="emailLink" href="mailto:logangerber@protonmail.com" :icon="'envelope'" title="Email">Email
		</HeaderIcon>
		<!-- <RouterLink to="/blog" id="blogLink"></RouterLink> -->
	</nav>
</template>

<style scoped>
#pageHeader {
	display: flex;
	flex-direction: row;

	justify-content: flex-start;
	flex-wrap: nowrap;
	align-items: flex-end;

	/* padding-bottom: 10px; */

	background: var(--color-header-background);

	/* border: 1px solid white; */
	height: 64px;
}

#homeLink {
	color: white;
	text-decoration: none;
	font-size: 30pt;
	font-weight: 700;
	padding-left: 10px;
}

#resumeLink {
	margin-left: auto;
}

#githubLink {
	margin-left: 10px;
}

#emailLink {
	margin-left: 10px;
	margin-right: 10px;
}

#blogLink {}

#hamburgerMenu {}
</style>
