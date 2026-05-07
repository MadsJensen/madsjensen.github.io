# WeakAI Blog

A Hugo blog using the [PaperMod](https://github.com/adityatelange/hugo-PaperMod) theme, hosted on GitHub Pages, and integrated with Substack.

## Features
- **Fast & Minimal:** Powered by Hugo and PaperMod.
- **Substack Integration:** Newsletter signup form embedded in the footer of every post.
- **SEO Ready:** Support for `canonicalURL` to handle cross-posting to Substack without SEO penalties.
- **Auto-Deployment:** GitHub Actions automatically builds and deploys to GitHub Pages on every push to `main`.

## Workflow: Hugo + Substack

To maintain SEO while cross-posting to Substack, follow this workflow:

1. **Write the Post in Hugo:**
   - Run `hugo new posts/your-post-name.md`.
   - Write your content.
   - Set `draft = false`.
   - Commit and push to GitHub.

2. **Cross-post to Substack:**
   - Once the post is live on your Hugo site (e.g., `https://weakai.github.io/posts/your-post-name/`), copy the content to a new Substack post.
   - **Crucial:** In Substack's "Settings" for that post, find the **"Canonical URL"** field and paste the URL of your Hugo post.
   - This tells Google that the Hugo version is the original.

3. **Alternative (Import RSS):**
   - You can also import your Hugo RSS feed (`https://weakai.github.io/index.xml`) into Substack to easily pull in new posts.

## Development
To run the site locally:
```bash
hugo server -D
```

## Adding a New Post
```bash
hugo new posts/my-new-story.md
```
The new post will automatically include the `canonicalURL` field in its front matter.
