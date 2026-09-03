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

## Fel 2

**Symptom:**

kunde inte hitta package.json

**Orsak:** pipelinen körde inte checkout
**Fix:** bytte till:

lade till checkout

**Hade upptäckts tidigare av:** att man höll bättre koll på dokumentationen

## Fel 3

**Symptom**

Fanns inget tests script

**Orsak**

Hade skrivit fel, det är test eller test:run

**Fix**: ändrade till test:run

## Fel 4

**Symptom**

Warning: No files were found with the provided path: build. No artifacts will be uploaded.

**Orsak**

artefacten heter "dist" inte "build"

**Fix**
byt path: build till path: dist
