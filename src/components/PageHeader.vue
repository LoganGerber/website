<script setup lang="ts">
import { RouterLink } from 'vue-router';
import HeaderIcon from '@/components/HeaderIcon.vue';
</script>

<template>
	<nav id="pageHeader">
		<RouterLink to="/" id="homeLink">Logan Gerber</RouterLink>
		<HeaderIcon
			id="newResumeLink"
			href="public/Resume.pdf"
			icon="file"
			title="Resume"
			:captionSize="12"
			:iconSize="28"
		>Resumé</HeaderIcon>
		<!-- <RouterLink to="/resume" id="resumeLink">
			<font-awesome-icon icon="file" inverse title="Resume" />
		</RouterLink>-->
		<!-- <a href="resume" id="resumeLink">
			<font-awesome-icon icon="file" inverse title="Resume" />
		</a>-->
		<HeaderIcon
			id="newGithubLink"
			href="https://github.com/LoganGerber"
			icon="['fab', 'github-square']"
			title="Github"
			:captionSize="12"
			:iconSize="32"
		>Github</HeaderIcon>
		<a href="https://github.com/LoganGerber" id="githubLink">
			<font-awesome-icon :icon="['fab', 'github-square']" inverse title="Github" />
		</a>
		<a href="mailto:logangerber@protonmail.com" id="emailLink">
			<font-awesome-icon icon="envelope" inverse title="Email" />
		</a>
		<!-- <RouterLink to="/blog" id="blogLink"></RouterLink> -->
	</nav>
</template>

<style scoped>
#newResumeLink {
	margin-left: auto;
}

#pageHeader {
	display: flex;
	flex-direction: row;

	justify-content: flex-start;
	flex-wrap: nowrap;
	align-items: flex-end;

	border: 1px solid white;
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
	margin-left: 10px;
	font-size: 28pt;
}

#githubLink {
	font-size: 32pt;
	margin-left: 10px;
}

#emailLink {
	font-size: 32pt;
	margin-left: 10px;
	margin-right: 10px;
}

#blogLink {
}

#hamburgerMenu {
}
</style>
