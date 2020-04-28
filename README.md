# docker-compose-verifier
Verifies docker-compose files using a pre-commit hook and docker-compose


# Steps
1. Ensure that docker-compose is installed globally
2. Run `git config core.hooksPath .githooks`
3. Commit any file with `docker-compose` in the name.
4. Profit