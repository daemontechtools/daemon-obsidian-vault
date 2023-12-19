##### Dynamically render absolute child element on top of it's parent

^f668cd

If you want to dynamically render a child element based on the `click` or `focus` events of the parent, keep in mind that the child will not be there to receive click events when it is clicked because you'll have fired the `onblur` event of the parent and removing the element from the DOM before it's able to receive an `click` events.
	Possible Solution?
	Try to do this without needing Javascript  by using the onfocusout event of the parent. This fires when the parent is *about* to lose focus. Didn't work

	Second Solution
	make absolute div

