# Project Requirements

To complete this project,

1. Implement as many of the Feature Requirements (details below) as possible
1. Conform to the Front-end Layer Requirements and Back-end Layer Requirements (details below)
1. Include two [additional features](./additional-features.md):
    - One front-end layer feature
    - One back-end layer feature

## Front-end Layer Requirements

Your front-end layer must use:

- React
- vite
- axios

Please avoid using additional packages if possible. (But please install any packages needed for your project to run!)

### Deployment

The front-end layer must be deployed on Render. This requires independent research starting with the search query "react render deploy."

## Back-end Layer Requirements

Your back-end layer must use:

- Flask
- PostgreSQL
- SQLAlchemy (including Migrate and Alembic)
- venv
- python-dotenv
- gunicorn
- pytest
- flask_cors

Please avoid using additional packages if possible. (But please install any packages needed for your project to run!)

### Deployment

The back-end API must be deployed on Render.

## Feature Requirements

Aim to complete all of these features. You and your team should feel *empowered* to:

- Interpret the features however you'd like
- Style the web app however you'd like, as long as it's usable
- Prioritize which features come first

It's recommended to prioritize creating and reading Boards and Cards.

### Create & Read Boards

**As a user, I want to be able to...**

#### Create

- Create a new board, by filling out a form. The form includes "title" and "owner" name of the board.
- See an error message if I try to make a new board with an empty/blank/invalid/missing "title" or "owner" input.
    - All error messages can look like a new section on the screen, a red outline around the input field, and/or disabling the input, as long as it's visible
- Hide the "New Board" form, so I don't have to see the "New Board" form all the time when I'm looking at cards.

#### Read

- View a list of all boards.
- Select a board.

### Create, Read, and Delete Cards

**As a user, I want to be able to...**

#### Create

- Create a new card _for the selected board_, by filling out a form and filling out a "message."
- See an error message if I try to make the card's "message" more than 40 characters.
    - All error messages can look like a new section on the screen, a red outline around the input field, and/or disabling the input, as long as it's visible
- See an error message if I try to make a new card with an empty/blank/invalid/missing "message."

#### Read

- View a list of cards that belong to the selected board.

#### Delete

- Delete an existing card.

### +1 Feature

**As a user, I want to be able to...**

- Press a "+1" icon on a single card, to indicate that I agree with it.
- See the number of "+1"s on a single card. Every card starts with zero "+1"s.
