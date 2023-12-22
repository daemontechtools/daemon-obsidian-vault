## ComboBox

^b731ba
^b49151
- [x] Accept a string as an initial value as well as options of type DmnSelectOption
- [x] Use the same technique used in DmnInputText to inherit from InputText
- [x] Provide a Class Property for overriding top level styles
- [x] Hide/Show options on `input` element `focus`/`blur`
- [x] On option click, set the input's current value
	- z fighting never gets old. I think label elements hijack an associated input's `click` and `focus` events. I need to stop using the label as the parent element for the ComboBox.
	- Still can't figure it out. spent almost all morning on this...I think what might be happening is that the `ul` element might be removed from the ui from the `onblur` event **before** the `onclick` has had a chance to fire? **Yes that was it**. Recorded in [[Gotchas#^f668cd| Web Browser Gotchas]].
- [x] Render the option list
- [ ] Support 2 levels of grouping. Display options in relation to their groups.
- [x] Filter the options based on the value of the input
- [x] Create a state for no results
- [ ] Allow ComboBox to show errors for any field on a model with a `ValueExpression`

#### Overriding Input Text Behaviour

- The value of our underlying `InputText` is not the value the Consumer cares about. It represents the query that we're using find a Value, it's that Value that is bound to by the Consumer

#### Should have based inherited from `InputSelect` instead of TextInput

Nope. Needed to go lower. `InputBase<T>`

#### The final solution

- Create a custom Input component with `InputBase<T>`. This allows the `Value` to be generic but requires far more setup which includes a Razor component [code behind](https://learn.microsoft.com/en-us/aspnet/core/blazor/components/?view=aspnetcore-8.0#partial-class-support)
- Data doesn't need to be marshalled into a custom object with `Label` and `Value` before it can be used in the ComboBox
- You can provide a custom list of objects, and on select you will get the instance of the selected custom object back.


**Let's try NOT doing this for now...**
- [ ] Figure out how many options can currently be displayed depending on the height of the current viewport.
	- [ ] Figure out how to get browser resizing events in Blazor Server.
- [ ] Load/Unload options from a virtual list of all options depending on the current location of the selection list.



##### DmnSelectOption
- Value: string
	- All values in html should boil down to strings. Not sure if I can use other types but for now this works as all I want is a UID from the selection as the value.
- Label: string
	- What shows up in the rendered list.
- Group: string?
	- Optional tag for sorting options into groups
- Group2: string?
	- Another tag for one more level of group
- ![[Pasted image 20231221091411.png]]
- 