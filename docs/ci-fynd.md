## Fel 1

**Symptom:**

> Invalid workflow file: .github/workflows/ci.yml#L1
> (Line: 9, Col: 12): Unexpected value 'pull-request'

**Orsak:** pull-request är fel syntax, det ska vara pull_request
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
