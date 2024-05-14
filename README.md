<div align="center">
  <h1>ResearchPocket</h1>
  <p>
    <strong>A template repository to deploy your research pocket on github pages</strong>
  </p>
  <p>
    <a href="https://github.com/ResearchPocket/ResearchPocket">ResearchPocket</a>
    |
    <a href="https://researchpocket.github.io/my-list/">Demo</a>
  </p>
<h2> My Research List </h2>
</div>


### Getting Started

As of now we only support [GetPocket](https://getpocket.com) as a source for
your research list.

1. Get the `consumer_key` and `access_token` from Pocket

   - Create a new Pocket consumer key: https://getpocket.com/developer/apps/new
   - Get the [ResearchPocket](https://github.com/ResearchPocket/ResearchPocket) Cli
     - Use cargo: `cargo install research`
     - Alternatively you can use the lateset GitHub releases binary for your
       platform
   - Initialize a database locally with the Cli
     - `research init .`
   - Get your access_token with the Cli
     - `research auth --key <consumer_key>`

2. Create a new repository from this template

   - Click on the `Use this template` button
   - Fill in the repository name and description

3. Set up GitHub action workflow in your repository

   - Set the `CONSUMER_KEY` and `ACCESS_TOKEN` secrets in your repository
     settings
     - Go to `Settings` -> `Secrets and variables` -> `Actions` ->
       `New repository secret`
     - Create two secrets: `CONSUMER_KEY` and `ACCESS_TOKEN` with the values you
       got from Pocket
     - Enable Github pages deployment in the repository settings
       - Go to `Settings` -> `Pages` -> `Source` and set it to `GitHub Actions`

4. Now you can manually run the workflow to deploy the site through a workflow
   dispatch which you can find in the `Actions` tab

   - Click on the `Run workflow` button
   - Select the `Deploy` workflow and click on the `Run workflow` button

5. The site will be available at
   `https://<username>.github.io/<repository-name>` ✨
