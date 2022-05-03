<script setup lang="ts">
import { RouterLink } from 'vue-router';
import HeaderAnchor from '@/components/HeaderAnchor.vue';
</script>

<template>
	<nav id="pageHeader">
		<RouterLink to="/" id="homeLink">Logan Gerber</RouterLink>
		<div id="spacer"></div>
		<HeaderAnchor id="resumeLink" href="public/Resume.pdf" :icon="'file'" title="Resume">Resumé
		</HeaderAnchor>
		<HeaderAnchor id="githubLink" href="https://github.com/LoganGerber" :icon="['fab', 'github-square']"
			title="Github">Github</HeaderAnchor>
		<HeaderAnchor id="emailLink" href="mailto:logangerber@protonmail.com" :icon="'envelope'" title="Email">Email
		</HeaderAnchor>
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
	gap: 20px;

	background: var(--color-header-background);

	height: 50px;

	margin-bottom: 10px;
	padding-left: 10px;
	padding-right: 10px;
}

#homeLink {
	color: white;
	text-decoration: none;
	font-size: 30pt;
	font-weight: 700;
}

#spacer {
	flex-grow: 1;
}
</style>
