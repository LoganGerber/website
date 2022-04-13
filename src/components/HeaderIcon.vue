<script setup lang="ts">
import { ref } from 'vue';

defineProps({
	href: {
		type: String,
		required: true
	},
	target: {
		type: String,
		default: '_blank'
	},
	icon: {
		type: [String, Array],
		required: true
	},
	title: String,
	iconSize: {
		type: Number,
		default: 12
	},
	captionSize: {
		type: Number,
		default: 12
	}
});

let isHovered = ref(false);
</script>

<template>
	<a
		:href="href"
		:target="target"
		class="headerIcon"
		@mouseover="isHovered = true"
		@mouseout="isHovered = false"
	>
		<font-awesome-icon :icon="icon" inverse :title="title" :style="{ 'fontSize': iconSize + 'pt' }" />
		<span
			class="iconCaption"
			:style="{ 'fontSize': captionSize + 'pt', 'display': isHovered ? 'contents' : 'none' }"
		>
			<slot></slot>
		</span>
	</a>
</template>

<style scoped>
.headerIcon {
	display: flex;
	flex-direction: column;
	justify-content: center;

	text-decoration: none;
}

.iconCaption {
	color: white;
	font-weight: bold;
}
</style>
