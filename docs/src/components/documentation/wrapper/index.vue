<template>
	<div>
		<h1 class="title">Wrapper</h1>
		<p class="text-large">Wrap elements with padding around them.</p>
		<p>Use the class <code>.wrapper</code> with or without the modifiers <code>-tiny</code> <code>-small</code> <code>-large</code> matching the sizes set in the variable <code class="text-info">$wrapper-padding-sizes</code>.</p>

		<div class="wrapper -tiny bg-secondary mb-15">
			<div class="bg-primary"><br></div>
		</div>
		<div class="wrapper -small bg-secondary mb-15">
			<div class="bg-primary"><br></div>
		</div>
		<div class="wrapper bg-secondary mb-15">
			<div class="bg-primary"><br></div>
		</div>
		<div class="wrapper -large bg-secondary">
			<div class="bg-primary"><br></div>
		</div>

		<pretty-code :code="html.sizes"></pretty-code>
	</div>
</template>

<script>
import prettyCode from '@/components/pretty-code'
import markup from '@/components/pretty-code/markup'

export default {
	name: 'Utilities',
	components: {
		prettyCode,
		markup
	},
	data: () => ({
		html: {
			sizes: require('./code/sizes.html'),
		}
	}),
	methods: {
	}
}
</script>

<style lang="scss" scoped>
	@import '~loop/variables';
</style>