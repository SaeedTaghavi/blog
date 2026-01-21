# Blog – How it works?

This blog is built with **MkDocs Material** and can be run locally using Docker.




## Project structure
```
docs/
├── index.md
├── compose.yml
├── mkdocs.yml
└── posts/
    ├── 2026-01-21-phase-synchronization-neural-populations.md
    └── ...
```
- **`docs/`**: All your Markdown content lives here.
- **`mkdocs.yml`**: MkDocs configuration.
- **`compose.yml`**: Docker Compose setup for local development.


## Add a new blog post

1. Create a new Markdown file inside `docs/posts/`:

   ```bash
   touch docs/posts/YYYY-MM-DD-your-title.md
   ```

2. Add the following frontmatter:

   ```yaml
   --- 
   title: "Your Post Title"
   date: YYYY-MM-DD
   author: Your Name
   tags: [tag1, tag2]
   --- 
   <!-- more -->
   Write your content in Markdown.
   ```

3. (Optional) Add the post to the homepage in `docs/index.md` under "Featured posts".


## Configuration

Edit `mkdocs.yml` to change:
- Site name and description
- Navigation structure
- Theme settings
- Plugins


## Stop the local server

```bash
docker compose down
```

Then, if you want to push the changes to GitHub, run:

```bash
git add .
git commit -m "Your commit message"
git push
```

The GitHub Actions will build the site and push it to the gh-pages branch.
