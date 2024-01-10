- [ ] Revert to a Mongoose version that supports stripping out undefined keys in findOneAndUpdate
	- [ ] Mongoose 5 was the last version to support `omitUndefined` in update functions
		- Although the wording in the migration documentation suggests that you can get the same behaviour by not needing the option at all, it actually removes `undefined` properties instead of omitting them from the update query.
	- [ ] Need to make sure I'm using the same Mongoose connection options
	- [x] Fix createLocalizedSchema
	- [ ] Fix Model.countDocuments
	- [ ] Fix res.acknowledged and res.modifiedCount
	- [ ] Fix Model.exists
		- had to use ts-ignore
	- [ ] Update Nx Version
	- [ ] Add`omitUndefined`

update count to count documents


Document NX build, serve and deploy
Dotenv vault