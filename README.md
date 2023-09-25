# Solana Buffer Deploy Github Action

Use this github action to automate Solana program deployments straight from Github. Use in conjunction with https://github.com/cardinal-labs/squads-program-upgrade.

## Usage

You can now consume the action by referencing the v1 branch

```yaml
uses: actions/solana-buffer-deploy@v0.1.6
with:
  network: https://api.devnet.solana.com
  program: my_program
  keypair: ${{ env.DEPLOYER_KEYPAIR }}
  program-id: prgCo6HJ2bP8xPJ3zwVnfVbqhBbBgY8t7moykr7wzCx
  buffer-authority: 7CLWzQ3pGwk9TCBnNFVq2p79NGQ8WyhSrrjfXiPN4L9m
```

## Package for distribution

GitHub Actions will run the entry point from the action.yml.

Packaging assembles the code into one file in the dist folder that can be checked in to Git, enabling fast and reliable execution and preventing the need to check in node_modules.

Run prepare

```bash
yarn prepare
```

Since the packaged index.js is run from the dist folder.

```bash
git add dist
```

See the [actions tab](https://github.com/actions/solana-buffer-deploy/actions) for runs of this action! :rocket:
