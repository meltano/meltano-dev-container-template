# Meltano Dev Container Template [![Open in Visual Studio Code](https://open.vscode.dev/badges/open-in-vscode.svg)](https://open.vscode.dev/meltano/meltano-dev-container-template)


A project template for DataOps CI/CD on GitHub.

## Testing

To test, first use the `Open in VS Code` link above to open the project in VS Code using Docker containers.

_Note: The only prerequisites to get started is to install **VS Code** and **Docker**. As needed, VS Code will prompt 
you to install any additional extensions needed to <a href="vscode://ms-vscode-remote.remote-containers/cloneInVolume?url=https%3A%2F%2Fgithub.com%2Fmeltano%2Fmeltano-cicd-lab-template">open the project</a>._

### Run a simple Meltano pipeline

Once you've opened the project, test that meltano is running executing the following
in a new VS Code terminal. These commands add a sample tap and target and then run a simple
pipeline test:

```bash
meltano add extractor tap-carbon-intensity
meltano add loader target-jsonl
meltano elt tap-carbon-intensity target-jsonl 
```

Debugging:

- If you get a message that the plugin is not yet installed, you might need to wait until all installs have
  completed. These should automatically run in a new terminal the first time you open the repo.
- If the plugins are still not available and you don't see an open terminal with the install progress, you
  can create a new terminal and manually run `meltano install` to install any missing plugins.

### Launch the web UI

```bash
meltano ui start 
```

After running the above command, you should see an option from VS Code to "Open in Browser". If not, you can manually navigate to http://localhost:5000.
