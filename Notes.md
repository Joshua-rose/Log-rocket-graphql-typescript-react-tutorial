graphql query for github issues https://developer.github.com/v4/explorer/
```graphql
{
  viewer {
    login
  }
  repository(name: "JobApplications", owner: "jrgiant") {
    issues(first: 100, orderBy: {field: CREATED_AT, direction: ASC}) {
      nodes {
        id
        number
        updatedAt
        url
        title
        labels(first: 100) {
          nodes {
            description
            name
          }
        }
        createdAt
      }
      pageInfo {
        hasNextPage
        hasPreviousPage
        startCursor
      }
      totalCount
    }
  }
}
```

https://blog.logrocket.com/build-a-graphql-react-app-with-typescript/

start at Adding user interaction