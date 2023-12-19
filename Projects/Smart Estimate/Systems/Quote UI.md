#### ComboBox

^b731ba
^b49151
- [x] Accept a string as an initial value as well as options of type DmnSelectOption
- [x] Use the same technique used in DmnInputText to inherit from InputText
- [x] Provide a Class Property for overriding top level styles
- [x] Hide/Show options on `input` element `focus`/`blur`
- [ ] On option click, set the input's current value
- [x] Render the option list
- [ ] Support 2 levels of grouping. Display options in relation to their groups.
- [ ] Figure out how many options can currently be displayed depending on the height of the current viewport.
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