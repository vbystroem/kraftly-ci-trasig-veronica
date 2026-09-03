## Fel 1

**Symptom:**

> Invalid workflow file: .github/workflows/ci.yml#L1
> (Line: 5, Col: 12): Unexpected value 'pull-request'

**Orsak:** pull-request är fel syntax, det ska vara 'pull-requests'
**Fix:** bytte till pull-requests
**Hade upptäckts tidigare av:** är nog bara ett slarvfel, men gör man det felet en gång gör man inte det igen.
