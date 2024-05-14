# My List: ReseaachPocket

A template repository to deploy your
[research pocket](https://github.com/KorigamiK/ResearchPocket) on github pages

# Getting Started

As of now we only support [GetPocket](https://getpocket.com) as a source for
your research list.

- Get the `consumer_key` and `access_token` from Pocket
  - Create a new Pocket consumer key: https://getpocket.com/developer/apps/new
  - Get the [ResearchPocket](https://github.com/KorigamiK/ResearchPocket) Cli
    - Use cargo: `cargo install research`
    - Alternatively you can use the lateset GitHub releases binary for your
      platform
  - Initialize a database locally with the Cli
    - `research init .`
  - Get your access_token with the Cli
    - `research auth --key <consumer_key>`

- Create a new repository from this template
  - Click on the `Use this template` button
  - Fill in the repository name and description

- Set up GitHub action workflow in your repository
  - Set the `CONSUMER_KEY` and `ACCESS_TOKEN` secrets in your repository
    settings
    - Go to `Settings` -> `Secrets and variables` -> `Actions` ->
      `New repository secret`
    - Create two secrets: `CONSUMER_KEY` and `ACCESS_TOKEN` with the values you
      got from Pocket
    - Enable Github pages deployment in the repository settings
      - Go to `Settings` -> `Pages` -> `Source` and set it to `GitHub Actions`

- Now you can manually run the workflow to deploy the site through a workflow
  dispatch which you can find in the `Actions` tab
  - Click on the `Run workflow` button
  - Select the `Deploy` workflow and click on the `Run workflow` button

- The site will be available at `https://<username>.github.io/<repository-name>`
  ✨
