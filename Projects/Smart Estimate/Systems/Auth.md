# Overview

Clients will me managed by Dealer Users. Dealer Users will be managed by Smart Users. It will be invite only by email and will not have public registration. Each Dealer User needs to be associated with a Dealer.
# User Types

- Smart Admin
- Smart User
- Dealer Admin
- Dealer User
# User Stories

As a User, I want to reset my password
As a User, I want to able to change my email (?)
As a User, I want to log in to the SmartOrder app

As a Smart Admin, I want to be able to add Smart Admins and Smart Users
As a Smart Admin, I want to be able to create a new Dealer
As a Smart Admin, I want to be able to add Dealer Users and Admins to a Dealer

As a Dealer User, I want to manage all my Quotes
As a Dealer Admin, I want to be able to manage all the Quotes in my Dealership

# Metadata

### User 
- username
- email
- factoryLinkId (Dealer's Id)
	- or maybe this will be the primary index of a dealer record of some kind?

#### Dealer 

- Dealer Name
- factoryLinkId

# Smart Data Collections

Everything in SmartOrder assumes that a user will only be associated to one Library at a time. I think then that Smart Users will only be able to manage other users, and not be able to load any Quotes.

#### Client Connection Requirements

- User Name
- Dealer Name
- Factory LinkID

Dealer
	-> Factory
		-> Library
			-> Projects (Quotes)
			-> Products
			-> etc.