<script setup lang="ts">
import HeaderIcon from '@/components/HeaderIcon.vue';

defineProps({
	to: {
		type: String,
		required: true
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
	<RouterLink :to="to">
		<HeaderIcon :icon="icon" :title="title" :iconSize="iconSize" :captionSize="captionSize">
			<slot></slot>
		</HeaderIcon>
	</RouterLink>
</template>
