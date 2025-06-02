from flask import Flask, render_template_string

app = Flask(__name__)

HTML_TEMPLATE = """
<!DOCTYPE html>
<html lang='en'>
<head>
  <meta charset='UTF-8'>
  <meta name='viewport' content='width=device-width, initial-scale=1.0'>
  <title>Ananya Kurikala | Marketing Portfolio</title>
  <link href='https://fonts.googleapis.com/css2?family=Playfair+Display:wght@500&family=Poppins:wght@400;600&display=swap' rel='stylesheet'>
  <style>
    body {
      font-family: 'Poppins', sans-serif;
      background: #fff;
      color: #333;
      line-height: 1.6;
    }
    header {
      background: url('https://images.unsplash.com/photo-1517817748498-4e9e69a3f189?auto=format&fit=crop&w=1500&q=80') center/cover no-repeat;
      height: 100vh;
      display: flex;
      flex-direction: column;
      justify-content: center;
      align-items: center;
      color: white;
      text-align: center;
      padding: 2rem;
    }
    h1 {
      font-family: 'Playfair Display', serif;
      font-size: 3rem;
    }
    nav a {
      margin: 0 15px;
      color: white;
      font-weight: bold;
      text-decoration: none;
    }
    section {
      padding: 4rem 2rem;
      max-width: 1000px;
      margin: auto;
    }
    h2 {
      font-family: 'Playfair Display', serif;
      font-size: 2rem;
      color: #ff69b4;
      margin-bottom: 1rem;
    }
    ul {
      list-style-type: square;
      padding-left: 1.5rem;
    }
    a {
      color: #ff1493;
    }
    footer {
      text-align: center;
      padding: 2rem;
      background: #fdf0f5;
      font-size: 0.9rem;
      color: #555;
    }
  </style>
</head>
<body>
  <header>
    <h1>Ananya Kurikala</h1>
    <p>Marketing Strategist | Content Creator | Digital Brand Builder</p>
    <nav>
      <a href="#about">About</a>
      <a href="#experience">Experience</a>
      <a href="#projects">Projects</a>
      <a href="#contact">Contact</a>
    </nav>
  </header>

  <section id="about">
    <h2>About Me</h2>
    <p>I’m a marketing strategist who merges art and analytics. From visual storytelling to SEO optimization, I thrive at the intersection of strategy and creativity.</p>
  </section>

  <section id="experience">
    <h2>Experience</h2>
    <ul>
      <li><strong>NEC Corporation of America</strong> – Marketing Communications Intern</li>
      <li><strong>Pulp Cosmetics</strong> – Marketing & Brand Strategist</li>
      <li><strong>@ananya_kurikala</strong> – Beauty Content Creator</li>
    </ul>
  </section>

  <section id="projects">
    <h2>Projects</h2>
    <ul>
      <li>SEO Strategy – Altar’d State</li>
      <li>eCommerce Build – Shopify</li>
      <li>Endo Sheer Market Entry Plan</li>
    </ul>
  </section>

  <section id="contact">
    <h2>Contact</h2>
    <p>Email: <a href="mailto:kurikalaananya@gmail.com">kurikalaananya@gmail.com</a></p>
    <p>LinkedIn: <a href="https://www.linkedin.com/in/ananya-kurikala" target="_blank">linkedin.com/in/ananya-kurikala</a></p>
    <p>Instagram: <a href="https://www.instagram.com/ananya_kurikala" target="_blank">@ananya_kurikala</a></p>
  </section>

  <footer>
    &copy; 2025 Ananya Kurikala — Strategy meets storytelling. Made with ❤️
  </footer>
</body>
</html>
"""

@app.route("/")
def home():
    return render_template_string(HTML_TEMPLATE)

if __name__ == "__main__":
    app.run(debug=True)
