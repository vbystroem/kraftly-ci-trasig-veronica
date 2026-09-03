## Fel 1

**Symptom:**

> Invalid workflow file: .github/workflows/ci.yml#L1
> (Line: 5, Col: 12): Unexpected value 'pull-request'

**Orsak:** pull-request är fel syntax, det ska följa yaml-trädet, [square brackets] är fel
**Fix:** bytte till:

```
on:
  push:
    branches:
      - main
  pull-request:
    branches:
      - main
```

**Hade upptäckts tidigare av:** är nog bara ett slarvfel, men gör man det felet en gång gör man inte det igen.
