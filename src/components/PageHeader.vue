<script setup lang="ts">
import { RouterLink } from 'vue-router';
</script>

<template>
	<nav id="pageHeader">
		<RouterLink to="/" id="homeLink">Logan Gerber</RouterLink>
		<!-- <RouterLink to="/resume" id="resumeLink"></RouterLink> -->
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
#pageHeader {
	display: flex;
	flex-direction: row;

	justify-content: flex-start;
	flex-wrap: nowrap;
	align-items: center;

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

/* #resumeLink {
} */

#githubLink {
}

#emailLink {
}

#blogLink {
}

#hamburgerMenu {
}
</style>
