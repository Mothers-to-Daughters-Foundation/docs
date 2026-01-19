# Deployment Information

## Repository Information

- **Repository**: `mothers-to-daughters-foundation/docs`
- **GitHub URL**: https://github.com/mothers-to-daughters-foundation/docs
- **Documentation URL**: https://mothers-to-daughters-foundation.github.io/docs/

## Configuration

The documentation hub is configured to deploy to:
- **Site URL**: `https://mothers-to-daughters-foundation.github.io/docs/`
- **Repository**: `mothers-to-daughters-foundation/docs`
- **Branch**: `main`

## GitHub Pages Setup

### Automatic Deployment

The repository includes a GitHub Actions workflow (`.github/workflows/deploy.yml`) that:
1. Builds the documentation on every push to `main`
2. Deploys automatically to GitHub Pages
3. Uses the latest GitHub Pages deployment actions

### Manual Setup (if needed)

If automatic deployment doesn't work, enable GitHub Pages manually:

1. Go to repository **Settings** → **Pages**
2. **Source**: Deploy from a branch
3. **Branch**: `gh-pages` (or select the branch with the workflow)
4. **Folder**: `/ (root)`
5. Click **Save**

### Workflow Permissions

Ensure the workflow has proper permissions:

1. Go to repository **Settings** → **Actions** → **General**
2. Under **Workflow permissions**:
   - Select "Read and write permissions"
   - Check "Allow GitHub Actions to create and approve pull requests"
3. Click **Save**

## Verification

After pushing to GitHub:

1. **Check GitHub Actions**:
   - Go to the **Actions** tab in the repository
   - Verify the workflow runs successfully
   - Check for any errors

2. **Check GitHub Pages**:
   - Go to repository **Settings** → **Pages**
   - Verify the site is being deployed
   - Note: It may take a few minutes for the first deployment

3. **Visit the Site**:
   - After deployment completes, visit: https://mothers-to-daughters-foundation.github.io/docs/
   - The site should be live!

## Troubleshooting

### Site Not Deploying

1. **Check GitHub Actions**:
   - Look for failed workflow runs
   - Check error messages
   - Verify Python version and dependencies

2. **Check Permissions**:
   - Ensure workflow has write permissions
   - Verify GitHub Pages is enabled

3. **Check Configuration**:
   - Verify `site_url` in `mkdocs.yml` is correct
   - Check that `repo_name` matches the repository

### Build Errors

1. **Dependencies**:
   - Verify `requirements.txt` has all needed packages
   - Check that Python version is compatible

2. **Configuration**:
   - Check `mkdocs.yml` for syntax errors
   - Verify all referenced files exist

### Site Not Updating

1. **Clear Cache**:
   - Hard refresh browser (Ctrl+F5 or Cmd+Shift+R)
   - Wait a few minutes for CDN to update

2. **Check Deployment**:
   - Verify latest workflow run completed
   - Check GitHub Pages settings

## Next Steps

1. ✅ Code has been pushed to GitHub
2. ⏳ Wait for GitHub Actions to build and deploy
3. ⏳ Verify the site is accessible at the configured URL
4. ⏳ Test all features (navigation, search, tags)

## Support

If you encounter issues:
- Check the GitHub Actions logs
- Review the workflow configuration
- Verify GitHub Pages settings
- Check the [SETUP.md](SETUP.md) guide for detailed setup instructions
