reveal.js ACE Editor plugin
===========================

reveal.js-ace is a reveal.js plugin that allows to embed ACE editors in a
reveal.js presentation.

Installation
------------

Download and install the package in your project:

bower install Gottox/reveal.js-ace

Add the plugin to the dependencies in your presentation, as below.

```
Reveal.initialize({
	// ...
	dependencies: [
	// ... 
		{ src: 'bower_components/reveal.js-ace/ace.js' }
	]
});
```

And embed the editor

```
<iframe class="ace" width=600 height=500 data-onchange="console.log(editor.getValue())">
Hello World!
</iframe>
```

Configuration
-------------

You can configure the editor for your presentation by providing a ```ace``` option in
the reveal.js initialization options. Note that all config values are optional
and will default as specified below.

```
Reveal.initialize({
	// ...

	ace: {
		// Event is triggered when a new editor is created.
		oninit: function(editor) {

		},
		// Event is triggered when the text of an editor has changed
		onchange: function(event, editor) {

		},
		// Automatically focus an editor when it is displayed
		autoFocus: false,

		// defines a css class name for the ace editors
		className: "ace"
	}
});
```
