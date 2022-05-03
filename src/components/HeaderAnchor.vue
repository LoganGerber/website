<script setup lang="ts">
import HeaderIcon from '@/components/HeaderIcon.vue';

defineProps({
	href: {
		type: String,
		required: true
	},
	target: {
		type: String,
		default: "_blank"
	},
	icon: {
		type: [String, Array],
		required: true
	},
	title: String,
	iconSize: {
		type: Number,
		default: 28
	},
	captionSize: {
		type: Number,
		default: 15
	}
});
</script>

<template>
	<a :href="href" :target="target">
		<HeaderIcon :icon="icon" :title="title" :iconSize="iconSize" :captionSize="captionSize">
			<slot></slot>
		</HeaderIcon>
	</a>
</template>
