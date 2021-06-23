# Hints

## Hint #1: Database and Table Hints

<details>

<summary>The example implementation uses these tables:</summary>

**Database name: `inspiration_board_development`**

### Table name: `board`

Columns:

- `board_id`, int, primary key
- `title`, string
- `owner`, string

### **Table name: `card`**

Columns:

- `card_id`, int, primary key
- `message`, string
- `likes_count`, int
- `board_id`, int, foreign key to `board_id` in `board`

This implies that there are two models:

1. `Board`
1. `Card`

</details>

## Hint #2: Components

<details>

<summary>The example implementation uses these components.</summary>

Feel free to inspect the example implementation using React Dev Tools for more inspiration.

Components:

1. `App`
1. `BoardList`
1. `Board`
1. `NewBoardForm`
1. `CardList`
1. `NewCardForm`
1. `Card`

</details>

## Hint #3: Props and State in "Board" Component

<details>

<summary>The example implementation uses these props and state in the board-related components.</summary>

Feel free to inspect the example implementation using React Dev Tools for more inspiration.

### `App`

State:

- `boardsData`
- `selectedBoard`
- `isBoardFormVisible`

### `NewBoardForm`

State:

- `title`
- `owner`

### `CardList`

Props:

- `board`

State:

- `cardsData`

### `NewCardForm`

State:

- `message`

</details>


## Hint #4: Endpoints in the API

<details>

<summary>The example implementation defines these endpoints.</summary>

- `GET` `/boards`
- `POST` `/boards`
- `GET` `/boards/<board_id>/cards`
- `POST` `/boards/<board_id>/cards`
- `DELETE` `/cards/<card_id>`
- `PUT` `/cards/<card_id>/like`

</details>

## Hint #5: Responses from the API

<details>

<summary>The example implementation expects these responses from the API.</summary>

Every time some board data is sent, each board data is an object with these key-value pairs:

```json
{
    "board_id": ...,
    "title": ...,
    "owner": ...
}
```

Lists of boards are in an array:

```json
[
    {
        "board_id": ...,
        "title": ...,
        "owner": ...
    },
    {
        "board_id": ...,
        "title": ...,
        "owner": ...
    }
]
```

Each card data is sent with these key-value pairs:

```json
{
    "card_id": ...,
    "message": ...,
    "likes_count": ...,
    "board_id": ...
}
```

Lists of boards are in an array:

```json
[
    {
        "card_id": ...,
        "message": ...,
        "likes_count": ...,
        "board_id": ...
    },
    {
        "card_id": ...,
        "message": ...,
        "likes_count": ...,
        "board_id": ...
    }
]
```

</details>
