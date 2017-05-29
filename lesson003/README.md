

To two-way bind to native elements or non-Polymer elements that don't follow this event naming convention, 
you can specify a custom change event name in the annotation using the following syntax:

target-prop="{{hostProp::target-change-event}}"

Example:

<!-- Listens for `input` event and sets hostValue to <input>.value -->
<input value="{{hostValue::input}}">

<!-- Listens for `change` event and sets hostChecked to <input>.checked -->
<input type="checkbox" checked="{{hostChecked::change}}">

<!-- Listens for `timeupdate ` event and sets hostTime to <video>.currentTime -->
<video url="..." current-time="{{hostTime::timeupdate}}">
