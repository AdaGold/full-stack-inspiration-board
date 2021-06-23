# Project Requirements

To complete this project,

1. Implement as many of the Feature Requirements (details below) as possible
1. Conform to the Front-end Layer Requirements and Back-end Layer Requirements (details below)
1. Include two [stretch goals](./stretch-goals.md):
    - One front-end layer stretch goal
    - One back-end layer stretch goal

## Front-end Layer Requirements

Your front-end layer must use:

- React
- create-react-app
- axios

Please avoid using additional packages if possible. (But please install any packages needed for your project to run!)

### Deployment

The front-end layer must be deployed on Heroku. This requires independent research starting with the search query "react heroku deploy."

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

The back-end API must be deployed on Heroku.

Note: If your project changes the directory name `app` to something else, or renames the function `create_app()` inside `src/__init__.py`, you may need to change the command from `web: gunicorn 'app:create_app()'`.

## Feature Requirements

### Create & Read Boards

**As a user, I want to be able to...**

#### Create

- Create a new board, by filling out a form and filling out the "title" and "owner" name.
- See an error message if I try to make a new board with an empty/blank/invalid "title" or "owner" input.
    - All error messages can look like a new section on the screen, a red outline around the input field, and/or disabling the input, as long as it's visible
- Hide the "New Board" form, so I don't have to see the "New Board" form all the time when I'm looking at cards.

#### Read

- View a list of all boards.
- Hide the list of boards.
- Select a board.

<!-- #### Update

- Edit the "title" and "owner" of an existing board, using a form.
- See an error message if I try to edit a new board with an empty/blank/invalid "title" or "owner" input. -->

<!-- #### Delete

- Delete an existing board, which should delete all associated cards. -->

### Create, Read, Delete, and +1 Cards

**As a user, I want to be able to...**

#### Create

- Create a new card _for the selected board_, by filling out a form and filling out the "message."
- See an error message if I try to make the card's "message" more than 40 characters.
    - All error messages can look like a new section on the screen, a red outline around the input field, and/or disabling the input, as long as it's visible
- See an error message if I try to make a new card with an empty/blank/invalid "message."

#### Read

- View a list of cards that belong to the selected board.

#### Delete

- Delete an existing card.

### +1 Feature

**As a user, I want to be able to...**

- Press a "+1" icon on a single card, to indicate that I agree with it.
- See the number of "+1"s on a single card. Every card starts with zero "+1"s.
