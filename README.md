[![Netlify Status](https://api.netlify.com/api/v1/badges/f4aa5b93-ab95-498c-a3a0-afdec8a69ab8/deploy-status)](https://app.netlify.com/sites/eloquent-poitras-af14f0/deploys)

# dfinity-docs-playbook
[Antora playbook](https://docs.antora.org) for the Dfinity Internet Computer Documentation Site. Antora allows you to pull documentation from multiple repositories, select a UI to display them, and combines everything into a static site. The rules for the generated site are defined in `antora-playbook.yml`.

## Sources
- The ui comes from the `ui-bundle.zip` in the master branch of the [dfinity-lab/antora-sdk](https://github.com/dfinity-lab/antora-sdk) repo
- the docs come from the masteer branch of the [dfinity-lab/docs](https://github.com/dfinity-lab/docs) repo (and possibly others in the future)

## Building Project Locally
In general you'll only need to build the project if you'd like to test out how the site will look locally before deploying.
1. Make sure you have Antora installed: https://docs.antora.org/antora/2.2/install/install-antora/
2. run `antora antora-playbook.yml`
3. open the `build` folder in your browser


## Making Changes
- To update the user interface, make changes in [dfinity-lab/antora-sdk](https://github.com/dfinity-lab/antora-sdk)
- To update documentation, make changes in [dfinity-lab/docs](https://github.com/dfinity-lab/docs)
- To update the UI and Docs sources, make changes in `antora-playbook.yml`

## Deployments
Deployments are handled automatically through Netlify every time a commit to master in this repo is made. As making changes here is rare, you'll likely end up manually triggering deployments on the netlify website as changes to in the UI repo or the Docs repo do not trigger a new deployment. 

Netlify deployment configurations are outlined in `netlify.toml`
