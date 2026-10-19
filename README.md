# Physical2RSI website deployment

**[Project website](https://physical2rsi.github.io/)** · **[Awesome-Physical2RSI](https://github.com/Physical2RSI/Awesome-Physical2RSI)**

This repository hosts the GitHub Pages deployment configuration for the organization website. The project source, survey summary, reference library, website, and assets are maintained in **[Awesome-Physical2RSI](https://github.com/Physical2RSI/Awesome-Physical2RSI)**. Submit content changes and issues there.

## Automatic updates

The **Deploy GitHub Pages** workflow checks out `Awesome-Physical2RSI/main`, runs its existing validation and build, and publishes only its `dist/` directory. It checks for new source commits every five minutes and skips scheduled deployments when the published source commit is unchanged. GitHub may delay scheduled runs.

For an immediate deployment, open this repository's **Actions → Deploy GitHub Pages → Run workflow**. A push to this repository also triggers deployment. Pages must use **GitHub Actions** as its source. The workflow uses GitHub's temporary repository token and Pages OIDC; no additional cross-repository secret is required.

The website's `_deployment.json` records the source repository and commit used for the live build. Revert a source change in `Awesome-Physical2RSI` to roll back, then run the deployment workflow. If GitHub disables scheduled workflows after repository inactivity, re-enable this workflow in Actions before relying on scheduled updates.
