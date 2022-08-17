# Feathers-Pinia TypeScript Example

```

export class User extends BaseModel {
  id: Id;
  name: string;
  age: number;
  type: string;
  class: string;
}

----------------

<template>
  <tr>
    <td>{{ user.name }}</td>
    <td>{{ user.age }}</td>
    <td>{{ user.class }}</td>
  </tr>
</template>
<script setup lang="ts">
import { User } from "./../stores/user";
defineProps({
  user: { type: User, required: true },
});
</script>
```

This example is based on [Feathers-Pinia Pagination
Example](https://github.com/marshallswain/vitesse-feathers-pinia-example)

## TypeScript features

* `src/stores/user.ts` shows how to define class properties
* `src/components/UserRow.vue` uses the defined properties
* `src/pages/index.vue` shows how to type returned values from `useFind` :

```
const { items: users, latestQuery }: { items: ComputedRef<User[]>; latestQuery: null | object } = useFind({ model: User, params });
```

## Setup

1. Clone and run `pnpm i`
2. Run the app with `pnpm dev`
3. Open your browser to http://localhost:3333

If everything went well, you'll see the app, above.

Learn more about Feathers-Pinia at [https://feathers-pinia.pages.dev](https://feathers-pinia.pages.dev)

<img src="https://feathers-pinia.pages.dev/feathers-pinia.png" height="360" style="object-fit: scale-down;"/>
