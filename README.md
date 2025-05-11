<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0" />
  <meta name="description" content="News & Views brings you the latest headlines, live news, and editorial content across categories like sports, politics, and education." />
  <meta name="google-adsense-account" content="ca-pub-6021770397712812">
  <title>News & Views</title>
  <script src="https://cdn.tailwindcss.com"></script>
  <script async src="https://pagead2.googlesyndication.com/pagead/js/adsbygoogle.js?client=ca-pub-6021770397712812" crossorigin="anonymous"></script>
  <style>
    body {
      background-image: url('https://images.unsplash.com/photo-1507525428034-b723cf961d3e?auto=format&fit=crop&w=1920&q=80');
      background-size: cover;
      background-attachment: fixed;
      background-repeat: no-repeat;
      background-position: center;
    }
    .blog-highlight {
      background: linear-gradient(135deg, #1e3a8a, #2563eb, #1e40af);
      border: 2px solid #facc15;
      box-shadow: 0 0 20px rgba(250, 204, 21, 0.7);
    }
    #header-news-controls {
      display: flex;
      gap: 1rem;
      align-items: center;
    }
  </style>
</head>
<body class="bg-gray-900 bg-opacity-90 text-white font-sans">

  <!-- Header Section -->
  <header class="bg-black bg-opacity-70 p-6 shadow-lg">
    <div class="container mx-auto flex justify-between items-center">
      <h1 class="text-3xl font-bold text-white">News & Views</h1>
      <nav class="hidden md:flex">
        <a href="#home" class="mx-4 hover:text-blue-400">Home</a>
        <a href="#categories" class="mx-4 hover:text-blue-400">Categories</a>
        <a href="#sports" class="mx-4 hover:text-blue-400">Sports</a>
        <a href="#newspapers" class="mx-4 hover:text-blue-400">Newspapers</a>
        <a href="#live-news" class="mx-4 hover:text-blue-400">Live News</a>
        <a href="#featured-news" class="mx-4 hover:text-blue-400">Top Headlines</a>
        <a href="#upload" class="mx-4 hover:text-blue-400">Upload</a>
        <a href="#about" class="mx-4 hover:text-blue-400">About</a>
        <a href="#contact" class="mx-4 hover:text-blue-400">Contact</a>
      </nav>
    </div>
  </header>

  <!-- Main Content -->
  <main>

    <!-- Hero Section -->
    <section id="home" class="h-screen flex items-center justify-center bg-black bg-opacity-50">
      <div class="bg-black bg-opacity-60 p-10 rounded-xl text-center max-w-xl">
        <h2 class="text-4xl font-bold mb-4">Stay Informed. Stay Ahead.</h2>
        <p class="text-lg mb-6">The latest news and sharp opinions, straight from your laptop.</p>
        <a href="#categories" class="bg-blue-600 hover:bg-blue-700 px-6 py-3 rounded-full transition">Explore Categories</a>
      </div>
    </section>

    <!-- Categories -->
    <section id="categories" class="py-12 px-4 text-center">
      <h2 class="text-2xl font-bold text-yellow-300">Categories</h2>
      <ul class="text-white space-y-2 mt-4">
        <li><a href="#sports" class="hover:underline">🏏 Sports Headlines (Cricinfo)</a></li>
        <li><a href="#ary-news" class="hover:underline">📰 ARY News</a></li>
        <li><a href="#jang-news" class="hover:underline">📰 Jang Newspaper</a></li>
        <li><a href="#featured-news" class="hover:underline">📢 Top Headlines (BISE, PBCC, etc.)</a></li>
        <li><a href="#upload" class="hover:underline">📤 Upload Documents</a></li>
      </ul>
    </section>

    <!-- Newspapers Section -->
    <section id="newspapers" class="py-12 px-4 text-center">
      <h2 class="text-2xl font-bold text-yellow-300">Newspapers Section</h2>
      <div class="text-white space-y-4 mt-6">
        <div id="ary-news">
          <h3 class="text-xl font-semibold">ARY News</h3>
          <iframe title="ARY News Website" src="https://www.arynews.tv/" class="w-full h-96 border-2 border-yellow-500"></iframe>
        </div>
        <div id="jang-news">
          <h3 class="text-xl font-semibold mt-8">Jang Newspaper</h3>
          <iframe title="Jang Newspaper Website" src="https://jang.com.pk/" class="w-full h-96 border-2 border-yellow-500"></iframe>
        </div>
      </div>
    </section>

    <!-- Live News -->
    <section id="live-news" class="py-16 px-6 bg-gray-950 bg-opacity-90">
      <div class="max-w-6xl mx-auto">
        <h3 class="text-3xl font-bold mb-10 text-center text-white">Live News Channels</h3>
        <div class="grid grid-cols-1 md:grid-cols-3 gap-8">
          <div class="bg-gray-800 p-4 rounded-xl text-center shadow-lg">
            <h4 class="text-xl font-bold text-yellow-400 mb-2">ARY News (Live)</h4>
            <iframe title="ARY Live Stream" class="w-full h-48" src="https://www.youtube-nocookie.com/embed/live_stream?channel=UCqwUrj10mAEsqezcItqvwEw" frameborder="0" allowfullscreen></iframe>
          </div>
          <div class="bg-gray-800 p-4 rounded-xl text-center shadow-lg">
            <h4 class="text-xl font-bold text-yellow-400 mb-2">Geo News (Live)</h4>
            <iframe title="Geo Live Stream" class="w-full h-48" src="https://www.youtube-nocookie.com/embed/live_stream?channel=UCr8oc-LOaApCXWLjBp-F3CQ" frameborder="0" allowfullscreen></iframe>
          </div>
          <div class="bg-gray-800 p-4 rounded-xl text-center shadow-lg">
            <h4 class="text-xl font-bold text-yellow-400 mb-2">92 News (Live)</h4>
            <iframe title="92 News Live Stream" class="w-full h-48" src="https://www.youtube-nocookie.com/embed/live_stream?channel=UC27z6mRtD9pN7M3msqRBj2A" frameborder="0" allowfullscreen></iframe>
          </div>
        </div>
      </div>
    </section>

    <!-- Sports -->
    <section id="sports" class="py-12 px-4">
      <div class="max-w-4xl mx-auto">
        <h3 class="text-2xl font-bold text-yellow-300 mb-4">Cricket Sports Headlines</h3>
        <ul id="sports-news-list" class="list-disc list-inside text-white space-y-2"></ul>
      </div>
    </section>

    <!-- Featured News -->
    <section id="featured-news" class="py-12 px-4 text-center">
      <h2 class="text-2xl font-bold text-yellow-300">Top Headlines Section</h2>
      <p class="text-white">
        Linked sources:
        <a href="https://www.biselahore.com/" target="_blank" class="text-blue-400 underline">BISE Lahore</a>,
        <a href="https://www.bisefsd.edu.pk/" target="_blank" class="text-blue-400 underline">BISE Faisalabad</a>,
        <a href="https://www.bisegrw.edu.pk/" target="_blank" class="text-blue-400 underline">BISE Gujranwala</a>,
        <a href="https://www.pbcc.edu.pk/" target="_blank" class="text-blue-400 underline">PBCC News</a>
      </p>
    </section>

    <!-- Upload -->
    <section id="upload" class="py-12 px-4 text-center">
      <h2 class="text-2xl font-bold text-yellow-300">Upload Section</h2>
      <form action="#" method="POST" class="mt-4 max-w-lg mx-auto bg-gray-800 p-6 rounded-xl shadow-lg">
        <label class="block text-left mb-2">Upload a Document:</label>
        <input type="file" class="block w-full p-2 border border-gray-600 bg-gray-900 text-white rounded" />
        <button type="submit" class="mt-4 px-6 py-2 bg-blue-600 hover:bg-blue-700 rounded text-white">Submit</button>
      </form>
    </section>

    <!-- About -->
    <section id="about" class="py-12 px-4 text-center">
      <h2 class="text-2xl font-bold text-yellow-300">About Us</h2>
      <p class="text-white max-w-2xl mx-auto mt-4">We are dedicated to bringing the most accurate and timely news updates, from local stories to global events. Stay informed and connected with the latest headlines.</p>
    </section>

    <!-- Contact -->
    <section id="contact" class="py-12 px-4 text-center bg-black bg-opacity-60">
      <h2 class="text-2xl font-bold text-yellow-300">Contact Us</h2>
      <form action="#" method="POST" class="mt-4 max-w-lg mx-auto bg-gray-800 p-6 rounded-xl shadow-lg">
        <label class="block text-left mb-2">Your Message:</label>
        <textarea class="block w-full p-2 border border-gray-600 bg-gray-900 text-white rounded" rows="4"></textarea>
        <button type="submit" class="mt-4 px-6 py-2 bg-blue-600 hover:bg-blue-700 rounded text-white">Send Message</button>
      </form>
    </section>

  </main>

  <!-- Footer -->
  <footer class="py-6 bg-gray-900 text-center text-white">
    <p>&copy; 2025 News & Views. All rights reserved.</p>
  </footer>

</body>
</html>
