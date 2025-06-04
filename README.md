<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <link rel="stylesheet" href="style.css">
</head>
<body>
  <h1>DevOps Internship - Task 6: Hosting Static Website with GitHub Pages</h1>

  <h2>📋 Task Description</h2>
  <p><strong>Objective:</strong> Deploy a simple HTML/CSS website using GitHub Pages</p>
  <p><strong>Tools Used:</strong> GitHub Pages, HTML, CSS</p>

  <h3>Key Requirements:</h3>
  <ul>
    <li>Create <code>index.html</code> and <code>styles.css</code> files</li>
    <li>Push code to a GitHub repository</li>
    <li>Enable GitHub Pages in repository settings</li>
    <li>Access live website via GitHub-provided URL</li>
    <li>Answer interview questions about GitHub Pages</li>
  </ul>

  <h2>🔗 Live Website</h2>
  <p>Access the deployed website here:<br>
  <a href="https://ramineni9925.github.io/Hosting-a-Static-Website-with-GitHub-Pages/" target="_blank">
    https://ramineni9925.github.io/Hosting-a-Static-Website-with-GitHub-Pages/
  </a></p>

  <h2>🛠 Implementation Details</h2>

  <h3>Files Created</h3>

  <h4>index.html (Homepage):</h4>
  <pre>
&lt;!DOCTYPE html&gt;
&lt;html&gt;
&lt;head&gt;
  &lt;title&gt;My GitHub Pages Website&lt;/title&gt;
  &lt;link rel="stylesheet" href="styles.css"&gt;
&lt;/head&gt;
&lt;body&gt;
  &lt;h1&gt;Welcome to My GitHub Pages Site!&lt;/h1&gt;
  &lt;p&gt;Successfully deployed via GitHub Pages.&lt;/p&gt;
  &lt;p&gt;By Gopichand Ramineni&lt;/p&gt;
&lt;/body&gt;
&lt;/html&gt;
  </pre>

  <h4>styles.css (Styling):</h4>
  <pre>
body {
  font-family: Arial, sans-serif;
  text-align: center;
  background-color: #fff5f5;
  margin: 50px;
}
h1 {
  color: #c0392b;
}
p {
  color: #7f0000;
}
  </pre>

  <h3>Steps Performed</h3>
  <ol>
    <li>Created repository <strong>Hosting Static Website with GitHub Pages</strong> on GitHub</li>
    <li>Added HTML and CSS files to the repository</li>
    <li>Enabled GitHub Pages in repository <strong>Settings</strong>:
      <ul>
        <li>Source branch: <code>main</code></li>
        <li>Source folder: <code>/</code> (root)</li>
      </ul>
    </li>
    <li>Verified live website availability after deployment</li>
    <li>Created this README with task documentation</li>
  </ol>

  <h2>📚 Interview Questions & Answers</h2>

  <h3>1. What is GitHub Pages?</h3>
  <p>GitHub Pages is a free static site hosting service provided by GitHub. It takes HTML, CSS, and JavaScript files directly from a repository, builds them, and publishes them as a website. Key features include:</p>
  <ul>
    <li>Hosted on GitHub's infrastructure</li>
    <li>Supports custom domains</li>
    <li>Automatic deployment on Git push</li>
    <li>Supports Jekyll for static site generation</li>
    <li>Free SSL/TLS encryption (HTTPS)</li>
  </ul>

  <h3>2. Can you host dynamic applications on GitHub Pages?</h3>
  <p>No. GitHub Pages is for static content only. It does not support:</p>
  <ul>
    <li>Server-side processing (e.g. PHP, Python, Node.js)</li>
    <li>Database connectivity</li>
    <li>User authentication</li>
    <li>Form processing (unless using third-party services)</li>
    <li>Server-side redirects or rewrites</li>
  </ul>

  <h3>3. What are the technical limits of GitHub Pages?</h3>
  <ul>
    <li>Repository Size: Max 1GB</li>
    <li>Bandwidth: 100GB/month</li>
    <li>Builds: 10 per hour</li>
    <li>File Size: ≤ 100MB</li>
    <li>Content Restrictions: No illegal or harmful content</li>
    <li>No <code>node_modules</code>, <code>.env</code> or server configuration files</li>
  </ul>

  <h3>4. How do you update the website content?</h3>
  <ol>
    <li>Modify files locally</li>
    <li>Commit and push:
      <pre>
git add .
git commit -m "Update content"
git push origin main
      </pre>
    </li>
    <li>Wait 1-3 minutes for GitHub to rebuild the site</li>
    <li>Refresh browser (clear cache if needed)</li>
  </ol>

  <h3>5. What happens when you delete the repository?</h3>
  <ul>
    <li>Website becomes inaccessible (404 error)</li>
    <li>All deployments and history are lost</li>
    <li>Custom domain and HTTPS settings are removed</li>
    <li>If named <code>&lt;username&gt;.github.io</code>, root domain is no longer available</li>
  </ul>

  <p><strong>To disable temporarily:</strong> Settings → Pages → Disable GitHub Pages</p>

  <h3>6. What is the default file that loads?</h3>
  <ul>
    <li><code>index.html</code> in root directory</li>
    <li>If not found: <code>index.md</code> → <code>README.md</code></li>
  </ul>

  <p>Custom path behavior:
    <br><code>domain.com/about</code> loads <code>about/index.html</code>
    <br><code>domain.com/blog/post</code> loads <code>blog/post/index.html</code>
  </p>

  <h3>7. How do you use a custom domain?</h3>
  <p><strong>Method 1: Using CNAME file</strong></p>
  <ol>
    <li>Create a <code>CNAME</code> file in the repo root</li>
    <li>Add: <code>www.yourdomain.com</code></li>
    <li>Update DNS:
      <ul>
        <li>Type: CNAME</li>
        <li>Name: www</li>
        <li>Value: <code>&lt;username&gt;.github.io</code></li>
      </ul>
    </li>
  </ol>

  <p><strong>Method 2: DNS Configuration</strong></p>
  <ul>
    <li>In GitHub Settings → Pages → Add domain</li>
    <li>Add DNS A records:
      <ul>
        <li>185.199.108.153</li>
        <li>185.199.109.153</li>
        <li>185.199.110.153</li>
        <li>185.199.111.153</li>
      </ul>
    </li>
    <li>HTTPS is enforced automatically</li>
    <li>May take 24–48 hours to propagate</li>
  </ul>

  <h2>📂 Repository Structure</h2>
  <pre>
github-pages-static-website/
├── index.html          # Homepage
├── styles.css          # Styling
└── README.md           # Project documentation
  </pre>

  <h2>✅ Conclusion</h2>
  <p>This task demonstrated the simplicity and power of GitHub Pages for hosting static websites. By completing this exercise, I:</p>
  <ul>
    <li>✅ Mastered the end-to-end deployment workflow</li>
    <li>✅ Learned GitHub Pages’ capabilities and limitations</li>
    <li>✅ Explored custom domains and HTTPS enforcement</li>
