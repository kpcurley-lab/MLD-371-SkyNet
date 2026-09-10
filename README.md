# MLD-371-SkyNet

A student-created, beginner-friendly MLD 371 tutorial: understand ChatGPT/Codex and Git/GitHub, build a meeting-agenda tool, check it, save and share it, and document AI use. Not an official Harvard or OpenAI resource.

## Preview

Open `dist/index.html` directly for core reading. For consistent browser storage and clipboard behavior, serve it over localhost. With Node.js already installed, run `node preview.mjs` from this repository and open http://127.0.0.1:4173. Stop with Ctrl+C. Node is only a maintainer preview convenience, not a visitor or student-exercise requirement. The preview server only exposes the three public site files and binds to loopback.

## Maintain

- `dist/index.html`: all eight lessons, sources, prompts and stable checkpoint IDs. Content and navigation remain readable without JavaScript.
- `dist/style.css`: responsive styles, native controls and visible keyboard focus.
- `dist/app.js`: progress, OS preference, reset confirmation and copy feedback. No libraries or build step.
- `.github/workflows/pages.yml`: manual-only GitHub Pages publication. No push trigger.

Keep `data-check` IDs stable so returning students retain progress. Browser storage uses `mld371-guide-v1`; it holds only boolean checkmarks and an OS preference. No names, accounts, analytics, API calls or credentials are collected. Storage failures fall back to current-visit state; no data syncs between devices or between preview and published origins. Reset only clears this guide's checkmarks. OS preference is retained. Methods notes are copyable templates, not submitted forms. The agenda in the introduction is a labeled example; students build their own working tool in lesson 5.

Recheck official links and setup wording before each class, particularly OpenAI app naming and access, Git installation and GitHub Pages eligibility. Update the visible last-verified date only after checking. Current verification: September 10, 2026. Official OpenAI Codex app/quickstart URLs currently redirect to ChatGPT Learn; the guide flags the naming change rather than assuming every student has the same interface. The Git book link initially failed retrieval and was replaced with GitHub's verified Git introduction. Windows OneDrive naming varies by organization.

## Publish — pending owner approval

**Recommended: GitHub Pages**, because the site is three static files and the team already uses GitHub. No additional service account or custom domain is necessary. GitHub Free supports Pages from public repositories; private source repositories require an eligible plan (Pro, Team or Enterprise). The resulting Pages site is normally public. Do not change source visibility automatically. A repository administrator must confirm eligibility, approve the intended audience, and review all public content before enabling publication.

Official sources, checked September 10, 2026:

- [Pages availability and visitor IP logging](https://docs.github.com/en/pages/getting-started-with-github-pages/what-is-github-pages)
- [Configure the publishing source](https://docs.github.com/en/pages/getting-started-with-github-pages/configuring-a-publishing-source-for-your-github-pages-site)
- [Custom Pages workflows](https://docs.github.com/en/pages/getting-started-with-github-pages/using-custom-workflows-with-github-pages)

After explicit approval to commit, push and publish:

1. Review the source and validation report. Confirm the repository plan supports its existing visibility; if it does not, stop and select another host instead of making the repository public.
2. Commit and push the approved files, including the manual workflow, to the intended branch. No changes have been committed or pushed by this build task.
3. In repository **Settings → Pages → Build and deployment → Source**, select **GitHub Actions**. Organization policy may require an administrator.
4. In **Actions**, select **Publish tutorial (manual approval only)**, choose **Run workflow**, and select the approved branch. Configure a required reviewer for the `github-pages` environment if available and desired. No publication is triggered merely by future pushes.
5. Wait for the workflow to succeed. Open the URL reported by the deployment, verify all assets and lesson links, then check it signed out before sharing it with classmates.
6. For updates, review and push changes, then manually run the workflow again. To roll back, restore the desired source revision through a reviewed change and republish. To take the site offline, use GitHub Pages unpublishing controls.

**Alternative: Sites hosting** is available through this workspace's Sites connector. Its normal private deployment is owner-only, so it is not yet a class-shareable result. Registration, source upload and deployment were deliberately deferred until approval. A future Sites flow must register this existing checkout, set `static.directory` to `dist` in `.openai/hosting.json`, review access settings for the class, and save/deploy the approved source. Do not replace this repository or assume owner-only access includes classmates. No hosting credentials or project IDs have been created for this tutorial.

The guide has no application analytics, but a hosting provider can maintain security logs. Do not promise that external hosting records no information.

## Validation

See `VALIDATION.md` for actual checks and limitations. Re-run `node --check dist/app.js` and `git diff --check` after editing. Browser-check all eight anchors, 20 checkboxes, section/overall progress, reload persistence, both OS views, copy controls, reset cancel/confirm/Escape, keyboard focus, and narrow layouts. Repeat on the final published origin after approval; localhost storage does not carry over.
