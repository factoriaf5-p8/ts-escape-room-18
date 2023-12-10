# Typescript Labs

## Lab 18: Typing Async Functions

file: `/src/18-function-types-with-promises.problem.ts`

Let's go deeper into function types.

Here we have a `createThenGetUser` function:

```ts
const createThenGetUser = async (
  createUser: unknown,
  getUser: unknown,
): Promise<User> => {
  const userId: string = await createUser();

  const user = await getUser(userId);

  return user;
};
```
This function takes in an asynchronous `createUser` function. It returns a promise that includes a `userId` string.

The `userId` string is then used in a call to `getUser` which would be a database call or something similar.

Challenge
Both `createUser` and `getUser` are currently typed as `unknown`.

Your challenge is to type the functions so that the errors go away.

Reference the function typing and Promise syntax that we've looked at previously for help.

