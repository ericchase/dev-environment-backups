The `JavaScript and TypeScript Nightly` `v5.7.20240911` update broke some part of the `Add all missing imports` source action. Ever since then, some imports would be incorrectly imported with the `type` only attribute; i.e.

```ts
import type {} from "";
```

instead of

```ts
import {} from "";
```

for situations where type only imports are not correct.

`JavaScript and TypeScript Nightly` `v5.7.20240904` works as expected, as far as I can tell.
