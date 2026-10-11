# Scott Swarm — Synthetic Approval Verification

Standalone synthetic security verification package.

## Requirements

Windows and Python 3.12. No third-party Python libraries.

## Running the tests

Download and extract:

`releases/scott-swarm-f7y-synthetic-verifier.zip`

Run:

```powershell
python -I -B test_suite.py
```

The 16 local tests examine ECDSA P-256 signatures, canonicalization,
negative mutations, persistent replay prevention, and a two-process
SQLite concurrency race.

## Security limitations

- Synthetic approval authority only
- No independent real-world signing-key custody
- No verified human operator consent
- No real enrollment
- No production or mainnet authority
- No anti-rollback certification
- No independent third-party reproduction yet
- Test author and verifier author are not independent

Passing these tests does not certify production security.

Discussion and adversarial review:
https://tantive.space/t/2340