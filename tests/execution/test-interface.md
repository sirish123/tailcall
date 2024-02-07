# test-interface

###### check identity

#### server:

```graphql
schema @server @upstream(baseURL: "http://jsonplacheholder.typicode.com") {
  query: Query
}

interface IA {
  a: String
}

type B implements IA {
  a: String
  b: String
}

type Query {
  bar: B @http(path: "/user")
}
```