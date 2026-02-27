# personal# Since the user is having trouble downloading the ZIP directly, we can create the ZIP file here and provide a direct link.
import zipfile
import os

# Define filenames and their content
files = {
    "index.html": """
<!DOCTYPE html>
<html lang="ar">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>أمل سلامي - مشروع فلاحي</title>
<style>
  body { font-family: 'Arial', sans-serif; margin: 0; padding: 0; background-color: #f4f3ee; color: #2e2e2e; }
  header { position: relative; background: url('farm-bg.jpg') no-repeat center center/cover; text-align: center; padding: 60px 20px 40px 20px; color: white; }
  header img { width: 150px; height: 150px; border-radius: 50%; border: 4px solid #8B4513; object-fit: cover; }
  header h1 { margin: 15px 0 5px; font-size: 2em; }
  header p { margin: 5px 0; font-weight: bold; }
  nav { display: flex; justify-content: center; background-color: #8B4513; }
  nav a { color: white; text-decoration: none; margin: 0 20px; padding: 15px 0; font-weight: bold; }
  nav a:hover { text-decoration: underline; }
  section { padding: 50px 20px; max-width: 900px; margin: auto; }
  h2 { color: #2E7D32; margin-bottom: 20px; }
  .projects ul { list-style: none; padding: 0; }
  .projects li { margin: 15px 0; padding: 15px; background-color: #e6f0e6; border-left: 5px solid #2E7D32; border-radius: 5px; }
  .contact p { margin: 10px 0; }
  .contact a { display: inline-block; margin-top: 15px; padding: 10px 20px; background-color: #2E7D32; color: white; text-decoration: none; border-radius: 5px; font-weight: bold; }
  .contact a:hover { background-color: #1b4d1b; }
  footer { text-align: center; background-color: #2E7D32; color: white; padding: 20px; }
</style>
</head>
<body>
<header>
  <img src="your-photo.jpg" alt="أمل سلامي">
  <h1>أمل سلامي</h1>
  <p>صاحبة مشروع فلاحي وباحثة في المجال الزراعي</p>
  <p>أطمح لتطوير الأعلاف وبيع منتجاتي مباشرة من المنتج إلى المستهلك</p>
</header>
<nav>
  <a href="#about">من أنا</a>
  <a href="#projects">مشاريعي</a>
  <a href="#contact">تواصل معي</a>
</nav>
<section id="about">
  <h2>من أنا</h2>
  <p>مواليد 1999، أصيلة ولاية جندوبة.</p>
  <p>خبيرة في الزراعة والأعلاف، وأسعى لتطوير تقنيات إدارة المحاصيل والأعلاف في تونس.</p>
  <p>أبيع منتجاتي مباشرة للمستهلك لضمان جودة عالية وأسعار عادلة.</p>
</section>
<section id="projects" class="projects">
  <h2>مشاريعي</h2>
  <ul>
    <li>مشروع SmartFodder: تطبيق لإدارة محاصيل الأعلاف (Alfalfa, Maize, Rhodes)</li>
    <li>تجارب زراعية لتحسين إنتاجية الأعلاف في تونس</li>
    <li>بيع منتجات الأعلاف مباشرة من المنتج إلى المستهلك</li>
    <li>أبحاث حول تحسين البروتين ونوعية الأعلاف</li>
  </ul>
</section>
<section id="contact">
  <h2>تواصل معي</h2>
  <div class="contact">
    <p>رقم الهاتف: <a href="tel:+21656858773">+21656858773</a></p>
    <p>البريد الإلكتروني: <a href="mailto:sallamiamal3@gmail.com">sallamiamal3@gmail.com</a></p>
    <a href="tel:+21656858773">اتصل الآن</a>
  </div>
</section>
<footer>
  <p>© 2026 أمل سلامي - جميع الحقوق محفوظة</p>
</footer>
</body>
</html>
""",
    ".gitignore": """
.DS_Store
Thumbs.db
*.log
""",
    "LICENSE": """
MIT License

Copyright (c) 2026 Amal Sallami

Permission is hereby granted, free of charge, to any person obtaining a copy
of this website and associated files, to deal in the Website without restriction,
including without limitation the rights to use, copy, modify, merge, publish,
distribute, sublicense, and/or sell copies of the Website, and to permit persons
to whom the Website is furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in all
copies or substantial portions of the Website.

THE WEBSITE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR
IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY,
FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE
AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER
LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM,
OUT OF OR IN CONNECTION WITH THE WEBSITE OR THE USE OR OTHER DEALINGS IN THE
WEBSITE.
"""
}

# Create ZIP
zip_path = "/mnt/data/personal_agri_website.zip"
with zipfile.ZipFile(zip_path, 'w') as zipf:
    for filename, content in files.items():
        zipf.writestr(filename, content)

zip_path
