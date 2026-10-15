# Publish VOIDNET on public GitHub Pages

1. Create a **public** GitHub repository (e.g. `voidnet`).
2. Upload **the contents of this ZIP** to the repository root, keeping `.github/workflows/deploy.yml` in that exact location. GitHub's web uploader can skip hidden files in some workflows; verify `.github/workflows/deploy.yml` appears in the repository's file browser.
3. Commit the files to the `main` branch.
4. Open **Settings > Pages > Build and deployment** and choose **GitHub Actions** as the source.
5. Open **Actions > Deploy VOIDNET to GitHub Pages**. The workflow should build and publish automatically on every push to `main` (or select **Run workflow**).
6. Open the deployment URL from the successful workflow or Settings > Pages. For a repository named `voidnet`, it is typically `https://YOUR-USERNAME.github.io/voidnet/`.

## Important
- This is a React/Vite **source** project. Do not select **Deploy from a branch** for the raw source; the GitHub Actions workflow compiles it into `dist` and deploys that.
- The relative Vite asset base (`./`) supports GitHub Pages project paths.
- The fictional `.void` addresses are handled inside the app; they are **not** real DNS domains. Browser tabs within the app are different from browser URL paths.
- This foundation contains **planned placeholders**, not 251 finished sites.
- Do not commit Supabase service-role keys, passwords or other secrets. No secrets are required for this foundation.
- The first build is not locally verified here because npm package installation timed out; GitHub Actions will provide the actual build result. If the workflow fails, share its build log for a targeted fix.
