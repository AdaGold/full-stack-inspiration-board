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
1. `Board`
1. `NewBoardForm`
1. `CardList`
1. `NewCardForm`
1. `Card`

Note: Why isn't there a `BoardList` component? There's not really a good reason, besides a weird decision. Not every design turns out perfectly! Many designs evolve over time.

</details>

## Hint #3: Props and State in "Board"-related Component

Don't forget that these are here to inspire your solution. They are not requirements!

<details>

<summary>The example implementation uses these props and state in the board-related components.</summary>

Feel free to inspect the example implementation using React Dev Tools for more inspiration.

### In the container component that holds data about boards

State:

- `boardsData`
- `selectedBoard`
- `isBoardFormVisible`

### `Board`

Props:

- `board`
- `onBoardSelect`

### `NewBoardForm`

Props:

- `createNewBoard`

State:

- `title`
- `owner`

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

## Hint #5: Requests to the API

Don't forget that these are here to inspire your solution. They are not requirements!

<details>

<summary>In the example implementation, the front-end layer sends these request bodies to the back-end API.</summary>

<br/>

Every time the front-end sends a request to the back-end, and the request needs to send data about a board, the HTTP request includes these key-value pairs:

```json
{
    "title": ...,
    "owner": ...
}
```

Every time the front-end sends a request to the back-end, and the request needs to send data about a card, the HTTP request includes these key-value pairs:

```json
{
    "message": ...,
    "likes_count": 0,
    "board_id": ...
}
```


</details>

## Hint #6: Responses from the API

Don't forget that these are here to inspire your solution. They are not requirements!

<details>

<summary>In the example implementation, the back-end API sends back these responses to the front-end layer.</summary>

<br/>

Every time the API sends back data about a board, the HTTP response includes these key-value pairs:

```json
{
    "board_id": ...,
    "title": ...,
    "owner": ...
}
```

When the API sends back a list of boards, the HTTP response looks like:

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

When the API sends back a card, the HTTP response looks like:

```json
{
    "card_id": ...,
    "message": ...,
    "likes_count": ...,
    "board_id": ...
}
```

Lists of cards are in an array:

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
