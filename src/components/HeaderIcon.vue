<script setup lang="ts">
import { FontAwesomeIcon } from '@fortawesome/vue-fontawesome';
import { ref, computed, onMounted, onUpdated } from 'vue';

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
		default: 28
	},
	captionSize: {
		type: Number,
		default: 15
	}
});

let isHovered = ref(false);
const caption = ref<HTMLSpanElement | null>(null);
const parent = ref<HTMLAnchorElement | null>(null);

const captionOpacity = computed(() => {
	return isHovered.value ? '1' : '0';
});

onMounted(() => { updateCaptionOffset() });
onUpdated(() => { updateCaptionOffset() });

function updateCaptionOffset() {
	let parentWidth = parent.value?.clientWidth;
	let captionWidth = caption.value?.clientWidth;

	if (parentWidth === undefined || captionWidth === undefined) {
		return;
	}

	let marginLeft = -1 * (captionWidth - parentWidth) / 2;

	console.log(marginLeft);
	(caption.value as HTMLSpanElement).style.marginLeft = marginLeft.toString() + 'px';
}

</script>

<template>
	<a :href="href" :target="target" class="headerIcon" @mouseover="isHovered = true" @mouseout="isHovered = false"
		ref="parent">
		<font-awesome-icon :icon="icon" inverse :title="title" :style="{ 'fontSize': iconSize + 'pt' }" />
		<span class="iconCaption" :style="{
			'fontSize': captionSize + 'pt', 'opacity': captionOpacity
		}" ref="caption">
			<slot></slot>
		</span>
	</a>
</template>

<style scoped>
.headerIcon {
	position: relative;

	display: flex;
	flex-direction: column;
	justify-content: center;

	text-decoration: none;
}

.iconCaption {
	color: white;
	font-weight: bold;
	position: absolute;

	top: calc(100% + 10px);
}
</style>
