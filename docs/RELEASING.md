# Release & update process

## Distribution policy

This public repository holds product documentation and announcements. Keep application source, paid executables, installers, build archives, signing keys, and customer information in separate private storage.

| Channel | Publish here |
| --- | --- |
| GitHub repository | Product documentation, public changelog, approved marketing assets |
| GitHub releases (optional) | Notes and the public Gumroad product-page link; no uploaded assets |
| Gumroad paid product content | Windows download and installation instructions for purchasers |

Do not put a paid binary in Git, Git LFS, GitHub Pages, public workflow artifacts, issue attachments, or release assets. GitHub automatically supplies repository archives for releases; keeping the repository documentation-only keeps those archives free of the paid app.

The .gitignore reduces accidental additions. It cannot prevent forced additions, release uploads, or customer redistribution. Gumroad delivery controls access to the download; application license validation or DRM would require separate app development.

## Before the first paid release

1. Confirm the app's actual version, supported devices, Windows/iPadOS requirements, installation steps, and connection method.
2. Test the package and screen-sharing flow on the supported devices.
3. Set up the Gumroad product, pricing, purchase terms, and included-update policy.
4. Place the Windows package in paid product content, not public previews or descriptions. Verify access using Gumroad's supported test-purchase flow.
5. Provide installation instructions and the version number alongside the download.
6. Replace the pending URL notices in README.md and docs/ACCESS.md with the verified public product-page link. Keep private customer download URLs out of GitHub.
7. Confirm a private support contact and update SUPPORT.md.
8. Choose any repository license deliberately before adding a LICENSE file.

No Gumroad product, live checkout, application licensing, or paid file upload has been configured by these documents.

## Each application update

1. Build and test in a private location outside this checkout.
2. Use a consistent version such as v1.2.3, matching the app's actual version. Reserve patch increments for fixes, minor increments for compatible features, and major increments for breaking changes.
3. Record changes, compatibility notes, and upgrade instructions in CHANGELOG.md under the real version and release date.
4. Upload the tested package to the appropriate paid Gumroad product content. Verify the intended purchasers can access it under the published update terms.
5. Keep a private backup of the previous working package for rollback.
6. Publish the public documentation and, if useful, a notes-only GitHub release after the Gumroad download is ready.
7. Notify customers through the chosen Gumroad update channel when authorized. Never include customer-specific download links or keys in public notes.

Manual Gumroad delivery is the initial update strategy. A future in-app updater must check purchase entitlement before providing a private download; do not point it at a public binary URL.

## Public release-note template

Copy this into a GitHub release only after replacing every placeholder:

> # WindyApple vX.Y.Z
>
> Released: YYYY-MM-DD
>
> ## Changes
> - Describe the user-visible change.
>
> ## Compatibility & upgrade
> - State requirements and any installation changes.
>
> ## Download
> Purchase or access WindyApple through the official Gumroad product page: REPLACE_WITH_PUBLIC_PRODUCT_URL.
>
> Paid application files are delivered through Gumroad. GitHub's automatic source archives contain only the public repository materials.

Do not upload any release assets. Do not create a placeholder application release before a real version is ready.

## Final publication check

- Inspect every staged file and the complete commit history intended for publication.
- Confirm no executable, installer, archive, secrets, receipts, or private download links are included.
- Confirm public links point to the product page, not a customer's download.
- Check the release has no uploaded assets.
- Verify the paid download through the intended purchaser flow.

References: [GitHub releases](https://docs.github.com/en/repositories/releasing-projects-on-github/about-releases) · [Gumroad customer access](https://gumroad.com/help/article/282-how-do-purchases-work-for-my-customers.html).
