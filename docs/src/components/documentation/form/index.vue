<template>
	<div>
		<h1 class="title">Form</h1>
		<p class="text-large">Form components</p>

		<h3 id="input"><a href="#input">#</a> Input</h3>
		<p>
			Apply the class <code>.input</code> to format the appearance of the textfield.<br>
			Alter the size of the input by applying any of the <code class="text-info">$text-sizes</code> classes available.<br>
			Alter the appearance of the input by applying any of the modifiers present in <code class="text-info">$input-colors-classes</code> such as <code>-danger</code>
		</p>
		<label for="default-input">Input</label>
		<input class="input mb-15" id="default-input" type="text">

		<label for="large-input">Large input</label>
		<input class="input -danger text-large" id="large-input" type="text">
		<p class="text-tiny text-danger mt-5">Textfield is required.</p>

		<pretty-code :code="html.size"></pretty-code>

		<h3 id="select"><a href="#select">#</a> Select</h3>
		<p>
			Apply the class <code>.select</code> to a <strong>parent element</strong> wrapping <markup>select</markup><br>
			Alter the size of the element by applying any of the <code class="text-info">$text-sizes</code> classes available on the <markup>select</markup> element.<br>
			Alter the appearance of the select by applying any of the modifiers present in <code class="text-info">$input-colors-classes</code> such as <code>-danger</code> to the <strong>parent element</strong>.
		</p>

		<label> Select Tiny Option</label>
		<span class="select mb-15">
			<select class="text-tiny">
				<option value="1">Option 1</option>
				<option value="2">Option 2</option>
				<option value="3">Option 3</option>
			</select>
		</span>

		<label> Select Option</label>
		<span class="select -danger">
			<select>
				<option value="1">Option 1</option>
				<option value="2">Option 2</option>
				<option value="3">Option 3</option>
			</select>
		</span>
		<p class="text-tiny text-danger mt-5">Textfield is required</p>
		<pretty-code :code="html.select"></pretty-code>

		<h3 id="checkbox"><a href="#checkbox">#</a> Checkbox</h3>
		<p>
			Apply the class <code>.checkbox</code>to <markup>input type="checkbox"</markup> preceding <markup>label</markup><br>
			Alter the appearance of the checkbox by applying any of the modifiers present in <code class="text-info">$input-colors-classes</code> such as <code>-danger</code>
		</p>
		<input class="checkbox" id="checkbox-1" type="checkbox">
		<label for="checkbox-1">Checkbox 1</label>
		<input class="checkbox -danger" id="checkbox-2" type="checkbox">
		<label for="checkbox-2">Checkbox 2</label>
		<p class="text-tiny text-danger">Checkbox is required</p>

		<pretty-code :code="html.checkbox"></pretty-code>

		<p>Need extra sizes? Set values to the variable <code class="text-info">$checkbox-sizes</code>.<br>It will generate modifiers with the name you created. Those sizes will only modify the dimenstion of the checkbox itself without interfering with the label. If you wish to also change the size of the label, please apply text utilities' classes such as <code>.text-small</code> <code>.text-large</code> and others.</p>
		<pretty-code class="language-css" :code="html.checkboxSizesVariable"></pretty-code>

		<input class="checkbox -small" id="checkbox-small-1" type="checkbox">
		<label class="text-small" for="checkbox-small-1">Checkbox small 1</label>
		<input class="checkbox -small" id="checkbox-small-2" type="checkbox">
		<label class="text-small mb-15" for="checkbox-small-2">Checkbox small 2</label>
		<input class="checkbox -large" id="checkbox-large-1" type="checkbox">
		<label for="checkbox-large-1">Checkbox large 1</label>
		<input class="checkbox -large" id="checkbox-large-2" type="checkbox">
		<label for="checkbox-large-2">Checkbox large 2</label>

		<pretty-code :code="html.checkboxSizes"></pretty-code>

		<h3 id="radio"><a href="#radio">#</a> Radio</h3>
		<p>
			Apply the class <code>.radio</code>to <markup>input type="radio"</markup> preceding <markup>label</markup><br>
			Alter the appearance of the radio by applying any of the modifiers present in <code class="text-info">$input-colors-classes</code> such as <code>-danger</code>
		</p>
		<input class="radio" id="radio-1" type="radio" name="radio">
		<label for="radio-1">Radio 1</label>
		<input class="radio -danger" id="radio-2" type="radio" name="radio">
		<label for="radio-2">Radio 2</label>
		<p class="text-tiny text-danger">Radio is required</p>

		<pretty-code :code="html.radio"></pretty-code>

		<p>Need extra sizes? Set values to the variable <code class="text-info">$radio-sizes</code>.</p>
		<pretty-code class="language-css" :code="html.radioSizesVariable"></pretty-code>

		<input class="radio -medium" id="radio-medium-1" type="radio" name="radio-medium">
		<label for="radio-medium-1">Radio medium 1</label>
		<input class="radio -medium" id="radio-medium-2" type="radio" name="radio-medium">
		<label class="mb-15" for="radio-medium-2">Radio medium 2</label>

		<input class="radio -large" id="radio-large-1" type="radio" name="radio-large">
		<label class="text-large" for="radio-large-1">Radio large 1</label>
		<input class="radio -large" id="radio-large-2" type="radio" name="radio-large">
		<label class="text-large" for="radio-large-2">Radio large 2</label>

		<pretty-code :code="html.radioSizes"></pretty-code>

		<h3 id="toggle"><a href="#toggle">#</a> Toggle</h3>
		<p>Apply the class <code>.toggle</code>to <markup>input type="checkbox"</markup> preceding <markup>label</markup></p>
		<input class="toggle" id="toggle-1" type="checkbox">
		<label for="toggle-1">Toggle</label>
		<pretty-code :code="html.toggle"></pretty-code>

		<p>Need extra sizes? Set values to the variable <code class="text-info">$toggle-sizes</code>.</p>
		<pretty-code class="language-css" :code="html.toggleSizesVariable"></pretty-code>

		<input class="toggle -large" id="toggle-large" type="checkbox">
		<label class="text-large" for="toggle-large">Toggle large</label>
		<pretty-code :code="html.toggleSizes"></pretty-code>

	</div>
</template>

<script>
import prettyCode from '@/components/pretty-code'
import markup from '@/components/pretty-code/markup'

export default {
	name: 'Form',
	components: {
		prettyCode,
		markup
	},
	data: () => ({
		html: {
			size: require('./code/size.html'),
			checkbox: require('./code/checkbox.html'),
			checkboxSizesVariable: require('./code/checkbox-sizes-variable.html'),
			checkboxSizes: require('./code/checkbox-sizes.html'),
			radio: require('./code/radio.html'),
			radioSizes: require('./code/radio-sizes.html'),
			radioSizesVariable: require('./code/radio-sizes-variable.html'),
			toggle: require('./code/toggle.html'),
			toggleSizes: require('./code/toggle-sizes.html'),
			toggleSizesVariable: require('./code/toggle-sizes-variable.html'),
			select: require('./code/select.html'),
		}
	}),
	methods: {
	}
}
</script>

<style lang="scss" scoped>
</style>