## Hi there 👋

This organization is where the infrastructure to write and build blog posts for [dfm.io](https://dfm.io) lives.

**How does it work?**:

- Each post lives in a repository within this organization with a name prefixed with `post--`. Take a look at [dfm-io/template](https://github.com/dfm-io/template) for more info about how new posts are created.
- The Jupyter notebook with the post's content gets executed within that repo's GitHub Actions environment and the executed version is pushed to the `executed` branch.
- Then, when the `build` workflow within the [dfm-io/dfm.io](https://github.com/dfm-io/dfm.io) repository is triggered (usually via a workflow dispatch), it finds all the `dfm-io/post--*` repos and collects them as posts on [the blog](https://dfm.io/posts).
