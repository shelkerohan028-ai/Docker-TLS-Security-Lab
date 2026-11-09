# Docker TLS Security Lab

A defensive cybersecurity lab demonstrating TLS encryption, mutual TLS (mTLS), certificate validation, revocation, and certificate rotation using Docker.

## Project Overview

This project demonstrates how PostgreSQL and Redis services can be secured using TLS and client certificate authentication.

## Architecture

```text
          Local Docker Environment
                    |
             Docker Compose
                    |
          +---------+---------+
          |                   |
      PostgreSQL             Redis
          17                   7
          |                   |
       TLS/mTLS             TLS/mTLS
          |                   |
    Certificate          Certificate
    Validation           Validation