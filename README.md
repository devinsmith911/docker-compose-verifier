# docker-compose-verifier
Verifies docker-compose files using a pre-commit hook and docker-compose


# Steps
1. Ensure that docker-compose is installed globally
2. Commit the pre-commit file to your repo in the .githooks folder
3. Ensure that you have run chmod +x on the pre-commit script.
4. Run `git config core.hooksPath .githooks` inside your repo that you want the hook to work in

Once you have done the above and commited to your branch, the test will run on any file with 'docker-compose' in the file name
