# How to contribute to this project?

1. Fork the [repository](https://github.com/doccano/doccano-client) by clicking on the 'Fork' button on the repository's page. This creates a copy of the code under your GitHub user account.

2. Clone your fork to your local disk, and add the base repository as a remote:

	```bash
	git clone git@github.com:<your Github handle>/doccano-client.git
	cd doccano-client
	git remote add upstream https://github.com/doccano/doccano-client.git
	```

3. Create a new branch to hold your development changes:

	```bash
	git checkout -b a-descriptive-name-for-my-changes
	```

	**do not** work on the `master` branch.

4. Set up a development environment by running the following command in a virtual environment:

	```bash
	poetry install
	poetry shell
	```

5. Develop the features on your branch.

6. Format your code. Run flake8 and isort so that your newly added files look nice with the following command:

	```bash
	poetry run task flake8
	poetry run task black
	poetry run task isort
	poetry run task test
	```

	Or use the following command:

	```bash
	make lint
	make test
	```

7. Once you're happy with your script file, add your changes and make a commit to record your changes locally:

	```bash
	git add doccano-client/<your_script_name>
	git commit
	```

	It is a good idea to sync your copy of the code with the original
	repository regularly. This way you can quickly account for changes:

	```bash
	git fetch upstream
	git rebase upstream/master
    ```

   Push the changes to your account using:

   ```bash
   git push -u origin a-descriptive-name-for-my-changes
   ```

8. Once you are satisfied, go the webpage of your fork on GitHub. Click on "Pull request" to send your to the project maintainers for review.
