# My Book Insights Blog

A Hugo-powered blog for sharing insights and lessons learned from books. Built with Hugo and the PaperMod theme.

## Local Development

1. Clone this repository:
   ```bash
   git clone --recursive YOUR_REPOSITORY_URL
   cd blog
   ```

2. Start the Hugo development server:
   ```bash
   hugo server -D
   ```

3. View your site at `http://localhost:1313/`

## Creating New Posts

To create a new book insight post:

1. Create a new markdown file in `content/posts/`:
   ```bash
   hugo new content posts/book-title-insights.md
   ```

2. Edit the front matter and content of your post:
   ```yaml
   ---
   title: "Book Title - Key Insights"
   date: YYYY-MM-DD
   description: "Main takeaways and insights from Book Title"
   tags: ["category", "topic", "theme"]
   categories: ["book-summary"]
   draft: false
   ---
   ```

## Deployment

This blog is automatically deployed to GitHub Pages when changes are pushed to the main branch. To set up deployment:

1. Create a new repository on GitHub
2. Push this code to your repository
3. In your repository settings, enable GitHub Pages and set the source to "GitHub Actions"
4. Update the `baseURL` in `hugo.yaml` to match your GitHub Pages URL
5. Push your changes to the main branch

## Customization

- Edit `hugo.yaml` to customize your site configuration
- Modify theme settings in the `params` section of `hugo.yaml`
- Add your profile picture by updating the `imageUrl` in the configuration

## Theme Features

The PaperMod theme includes:
- Responsive design
- Dark/light mode
- Search functionality
- Tags and categories
- Table of contents
- Reading time
- Social sharing buttons

## License

This project is open source and available under the [MIT License](LICENSE).