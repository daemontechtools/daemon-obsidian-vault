

### ShipLocationInput Component

^054d83

- Accept an initial value. Will commonly come from the parent Project object.
- While the current ShipLocation is set, display it's Address as read-only
- Provide a ComboBox for the user to select from existing ShipLocations. Upon selection, update the current Address. Emit the new value to the parent component so the parent Model can be updated as well.
- Provide an button that will expose a ShipLocation form component. When that component emits a new ShipLocation: 
	- Set the current ShipLocation to it
	- Emit the new ShipLocation to the parent component
	- Stop rendering the ShipLocation Form component

#### ShipLocation Form

- Require fields for Location Name as well as the required field for Address
- On clear, set the underlying ShipLocation Model to new(""), setting all it's properties to their default.
- On Save, validate the ShipLocation Model.
- On validation failure, update the view state to display validation errors to the user.
- On validation success, emit the created ShipLocation object to the parent.
- The parent will likely stop rendering the ShipLocation Form at this point and it will be deleted.


