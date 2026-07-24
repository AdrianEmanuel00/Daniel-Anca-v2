# Daniel & Anca - Git and cPanel Workflow

This is a static wedding invitation site. The deployable files are:

- `index.html`
- `assets/`

The old manual deploy files are intentionally ignored by Git:

- `deploy/`
- `deploy.zip`

## Local Workflow

1. Edit the site locally in `index.html` and `assets/`.
2. Preview locally:

```bash
python -m http.server 8000
```

3. Open `http://localhost:8000`.
4. Commit the update:

```bash
git status
git add index.html assets README.md README-CLIENT.md .cpanel.yml .gitignore CONTEXT
git commit -m "Update site"
```

5. Push to the remote repository:

```bash
git push origin main
```

## First-Time Git Setup

Create a private Git repository on GitHub, GitLab, or Bitbucket, then connect it locally:

```bash
git remote add origin <REMOTE_URL>
git branch -M main
git push -u origin main
```

Use the HTTPS or SSH clone URL shown by your Git provider.

## cPanel Pull Deployment

In cPanel:

1. Open `Files` -> `Git Version Control`.
2. Create/clone the repository from the same remote URL.
3. Use a repository path outside `public_html`, for example:

```text
repositories/daniel-anca-v2
```

4. In `Manage` -> `Pull or Deploy`, click `Update from Remote`.
5. Click `Deploy HEAD Commit`.

The `.cpanel.yml` file copies `index.html` and `assets/` to the subdomain document root:

```bash
$HOME/daniel-anca.aerdigital.ro/
```

If cPanel shows a different `Document Root` for the subdomain, change `DEPLOYPATH` in `.cpanel.yml` before deploying.

Official cPanel flow: `Update from Remote` pulls new commits, then `Deploy HEAD Commit` runs `.cpanel.yml`.
