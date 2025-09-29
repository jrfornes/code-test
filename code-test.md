# Angular Developer Code Test - User Activity Dashboard

## Objective

Build an Angular application that demonstrates your ability to handle dependent API calls and data aggregation. You'll fetch user data from one endpoint, then use that data to fetch additional information from other endpoints.

## Requirements

### Phase 1: Basic Implementation

Create an Angular application that:

1. **Fetches Users**: Get a list of users from `https://jsonplaceholder.typicode.com/users`
2. **Fetches User Posts**: For each user, fetch their posts from `https://jsonplaceholder.typicode.com/posts?userId={userId}`
3. **Fetches Post Comments**: For each post, fetch the comments from `https://jsonplaceholder.typicode.com/comments?postId={postId}`
4. **Aggregates Data**: Calculate the total number of posts and comments per user
5. **Displays Results**: Show users in a table with columns: Name, Email, Total Posts, Total Comments, Activity Score

### Phase 2: Advanced Features

If you complete Phase 1, implement:

1. **Error Handling**: Handle API failures gracefully with user-friendly error messages
2. **Loading States**: Show loading indicators while fetching data
3. **Sorting**: Allow users to sort by any column
4. **Filtering**: Add a search box to filter users by name or email

## API Endpoints

- Users: `https://jsonplaceholder.typicode.com/users`
- Posts: `https://jsonplaceholder.typicode.com/posts?userId={userId}`
- Comments: `https://jsonplaceholder.typicode.com/comments?postId={postId}`

## Data Models

```typescript
interface User {
  id: number;
  name: string;
  email: string;
  // ... other fields from the API
}

interface Post {
  id: number;
  userId: number;
  title: string;
  body: string;
}

interface Comment {
  id: number;
  postId: number;
  name: string;
  email: string;
  body: string;
}
```
