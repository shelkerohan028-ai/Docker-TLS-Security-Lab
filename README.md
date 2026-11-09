# Docker TLS Security Lab

A local defensive cybersecurity lab demonstrating TLS, mutual TLS (mTLS), certificate validation, certificate revocation, and certificate rotation.

## Technologies
- Docker Desktop
- PostgreSQL 17
- Redis 7
- OpenSSL
- Ubuntu WSL 2

## PostgreSQL Security
- TLS encrypted connections
- Mutual TLS authentication
- Client certificate validation
- Wrong CA rejection
- Plaintext connection rejection
- Certificate Revocation List (CRL)
- Revoked certificate rejection

## Redis Security
- TLS-only connections
- Client certificate authentication
- Wrong CA rejection
- New CA and certificate rotation
- Old client certificate rejection
- Docker health check verification

## Test Results
- PostgreSQL TLS: PASS
- PostgreSQL mTLS: PASS
- PostgreSQL wrong CA rejection: PASS
- PostgreSQL plaintext rejection: PASS
- PostgreSQL CRL revocation: PASS
- Redis TLS: PASS
- Redis mTLS: PASS
- Redis old certificate rejection: PASS
- Redis new certificate connection: PONG
- Redis health check: HEALTHY

## Start the Lab
    docker compose up -d

## Check Containers
    docker compose ps

## View Logs
    docker compose logs

## Security Notes
- Never upload private keys.
- Never publish passwords or tokens.
- Protect CA private keys.
- Use read-only certificate mounts where possible.
- This is an educational local lab, not a production deployment.

## Disclaimer
For educational and defensive cybersecurity testing only.
