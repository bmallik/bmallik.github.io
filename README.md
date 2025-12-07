# Bitan Mallik - Personal Portfolio Website

A personal academic portfolio website built with Jekyll and hosted on GitHub Pages.

🔗 **Live Site:** [https://bmallik.github.io](https://bmallik.github.io)

---

## 🚀 Running Locally in VS Code

### Prerequisites
- [Visual Studio Code](https://code.visualstudio.com/)
- [Docker Desktop](https://www.docker.com/products/docker-desktop/) (Recommended method)
- OR Ruby, Bundler, and Node.js (Manual method)

---

### Method 1: Using Docker (Recommended) 🐳

This is the easiest way to run the project without installing dependencies.

1. **Open the project in VS Code**
   ```bash
   cd bmallik.github.io
   code .
   ```

2. **Start Docker Desktop** (make sure it's running)

3. **Open VS Code Terminal** (`Ctrl + `` ` `` or `Cmd + `` ` `` on Mac)

4. **Run the following commands:**
   ```bash
   # Give necessary permissions
   chmod -R 777 .
   
   # Start the Docker container
   docker-compose up
   ```

5. **Open your browser** and go to: [http://localhost:4000](http://localhost:4000)

6. **To stop the server:**
   ```bash
   docker-compose down
   ```

---

### Method 2: Using VS Code Dev Container 📦

1. **Install the "Dev Containers" extension** in VS Code
   - Press `Cmd + Shift + X` (Mac) or `Ctrl + Shift + X` (Windows/Linux)
   - Search for "Dev Containers" and install it

2. **Open the project folder** in VS Code

3. **Reopen in Container**
   - Press `F1` and type `Dev Containers: Reopen in Container`
   - Select it and wait for the container to build

4. The site will automatically be available at [http://localhost:4000](http://localhost:4000)

---

### Method 3: Manual Setup (Without Docker) 💻

#### On macOS:
```bash
# Install Homebrew (if not installed)
/bin/bash -c "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/HEAD/install.sh)"

# Install Ruby and Node.js
brew install ruby
brew install node

# Add Ruby to PATH (add to ~/.zshrc)
echo 'export PATH="/opt/homebrew/opt/ruby/bin:$PATH"' >> ~/.zshrc
source ~/.zshrc

# Install Bundler
gem install bundler

# Navigate to project directory
cd bmallik.github.io

# Configure bundle to install gems locally
bundle config set --local path 'vendor/bundle'

# Install dependencies
bundle install

# Start the Jekyll server
bundle exec jekyll serve -l -H localhost
```

#### On Windows (WSL) / Linux:
```bash
# Update packages
sudo apt update && sudo apt upgrade -y

# Install dependencies
sudo apt install ruby-dev ruby-bundler nodejs build-essential gcc make

# Navigate to project directory
cd bmallik.github.io

# Configure bundle to install gems locally
bundle config set --local path 'vendor/bundle'

# Install dependencies
bundle install

# Start the Jekyll server
bundle exec jekyll serve -l -H localhost
```

5. **Open your browser** and go to: [http://localhost:4000](http://localhost:4000)

---

## 📁 Project Structure

```
bmallik.github.io/
├── _config.yml          # Site configuration
├── _data/               # Data files (JSON, YAML)
├── _includes/           # Reusable HTML components
├── _layouts/            # Page templates
├── _pages/              # Static pages
├── _posts/              # Blog posts
├── _publications/       # Publication entries
├── _portfolio/          # Portfolio items
├── _talks/              # Talks and presentations
├── assets/              # CSS, JS, images
├── files/               # Downloadable files (PDFs, etc.)
└── images/              # Image assets
```

---

## ✏️ Making Changes

- **Edit content:** Modify files in `_pages/`, `_posts/`, `_publications/`, etc.
- **Update site settings:** Edit `_config.yml` (requires server restart)
- **Add images:** Place them in the `images/` folder
- **Add downloadable files:** Place them in the `files/` folder

> **Note:** Changes to `_config.yml` require restarting the Jekyll server. Other file changes will auto-reload.

---

## 🌐 Deploying to GitHub Pages

1. Commit your changes:
   ```bash
   git add .
   git commit -m "Your commit message"
   ```

2. Push to GitHub:
   ```bash
   git push origin main
   ```

3. GitHub Pages will automatically build and deploy your site to [https://bmallik.github.io](https://bmallik.github.io)

---

## 📝 Credits

This website is built using the [Academic Pages](https://github.com/academicpages/academicpages.github.io) template, which was forked from the [Minimal Mistakes Jekyll Theme](https://mmistakes.github.io/minimal-mistakes/).
