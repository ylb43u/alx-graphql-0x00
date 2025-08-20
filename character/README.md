# Rick and Morty GraphQL Queries

This project demonstrates how to use GraphQL queries with the [Rick and Morty API](https://rickandmortyapi.com/graphql). The API provides data about characters, episodes, and locations from the Rick and Morty universe.

## Example Queries

### 1. Fetch All Characters

```graphql
query {
    characters {
        results {
            id
            name
            status
            species
            gender
            image
        }
    }
}
```

### 2. Get Character by ID

```graphql
query {
    character(id: 1) {
        id
        name
        origin {
            name
        }
        episode {
            name
            episode
        }
    }
}
```

### 3. Search Characters by Name

```graphql
query {
    characters(filter: { name: "Rick" }) {
        results {
            id
            name
            status
        }
    }
}
```

## Usage

- Use any GraphQL client (e.g., Apollo, Insomnia, Postman) to send queries to `https://rickandmortyapi.com/graphql`.
- Explore more queries and schema details at the [API documentation](https://rickandmortyapi.com/documentation/#graphql).