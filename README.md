# SSR with Amplify DataStore and Next.js

## Steps to run:
- `amplify init`
- `amplify add api`
- Use the schema below
- `amplify update api` - enable conflict resolution
- `amplify push`
## Schema:

```graphql
type Post
  @model
  @auth(rules: [{ allow: owner }, { allow: public, operations: [read] }]) {
  id: ID!
  title: String!
  content: String!
}
```
