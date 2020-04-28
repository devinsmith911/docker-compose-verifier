# docker-compose-verifier
Verifies docker-compose files using a pre-commit hook and docker-compose


# Steps
1. Ensure that docker-compose is installed globally
2. Commit the pre-commit file to your repo in the .githooks folder
3. Ensure that you have run chmod +x on the pre-commit script.
4. Run `git config core.hooksPath .githooks` inside your repo that you want the hook to work in

Once you have done the above and commited to your branch, the test will run on any file with 'docker-compose' in the file name

# Notes:
- The command will stub out any env_file declaration in your compose files, as having this causes the config check to fail with file not found errors
- The hook uses git diff-tree to find any files being commited, we cannot do a diff on files that do not exist yet in git, so your file will only be validated once it already exists in the git history. (IE, it will not be checked the first time you commit it, commit again to test it)