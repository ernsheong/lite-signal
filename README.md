
<!-- [![Build status](https://travis-ci.org/PolymerElements/lite-signal.svg?branch=master)](https://travis-ci.org/PolymerElements/lite-signal) -->

<!-- _[Demo and API docs](https://elements.polymer-project.org/elements/lite-signal)_ -->


##&lt;lite-signal&gt;

`lite-signal` provides basic publish-subscribe functionality.

Note: avoid using `lite-signal` whenever you can use
a controller (parent element) to mediate communication
instead.

To send a signal, fire a custom event of type `lite-signal`, with
a detail object containing `name` and `data` fields.

```javascript
this.fire('lite-signal', {name: 'hello', data: null});
```

To receive a signal, listen for `lite-signal-<name>` event on a
`lite-signal` element.

  <lite-signal on-lite-signal-hello="{{helloSignal}}">

You can fire a signal event from anywhere, and all
`lite-signal` elements will receive the event, regardless
of where they are in DOM.
