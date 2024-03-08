# Testing GitHub Actions Auto Deployment on Mock Landing Page for StyleThief
## What is StyleThief?
StyleThief is an idea for a Chrome extension that allows users to copy fonts, colors, and CSS snippets from websites directly from their browser.
### Access the page [here](https://earth2emma.site/) :)

## How Did We Set Up Auto Deployment?
Essentially, the YAML workflow will automatically build the Hugo website with the latest changes based on source code from `gh-pages`. Any pushes to main will trigger a deployment that reflects those changes.

To set this up, we created a workflow that aligns with GitHub Actions (for more info, see [this documentation](https://docs.github.com/en/actions/quickstart)).

The workflow code can be found at .github/workflows/gh-pages-deployment.yaml

It functions like so:
- workflow detects pushes to main
- when a push event occurs, the workflow will:
  - perform a job named deploy, which will check the source code repo and fetches the entire commit history
  - set up a hugo environment and run `hugo` to compile static files
  - publish the compiled static files to `gh-pages` branch of the repo, letting GitHub pages deploy the changes

### Notes:
- mock landing page implemented using Hugo
- based on this [Hugo Bootstrap Theme](https://github.com/filipecarneiro/hugo-bootstrap-theme)
- developed for CIS 3500 HW1
- testing auto deployment for CIS 3500 HW2
- time log found [here](https://docs.google.com/spreadsheets/d/1rwTnWFviAz19ZLrrE3WtiCTp54X6YdVcuBLMYkktKes/edit?usp=sharing)

<i>Emma Lee | 3/7/2024</i>
