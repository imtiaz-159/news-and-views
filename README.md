<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0" />
  <title>News & Views</title>
  <script src="https://cdn.tailwindcss.com"></script>
  <!-- Google AdSense Verification -->
  <script async src="https://pagead2.googlesyndication.com/pagead/js/adsbygoogle.js?client=ca-pub-6021770397712812"
       crossorigin="anonymous"></script>
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

  <!-- Header -->
  <header class="bg-black bg-opacity-70 p-6 shadow-lg">
    <div class="container mx-auto flex justify-between items-center">
      <h1 class="text-3xl font-bold text-white">News & Views</h1>
      <div class="flex-1 mx-6" id="header-news-controls">
        <marquee id="live-news-marquee" behavior="scroll" direction="left" class="text-yellow-400 font-semibold text-sm w-full">
          📢 Fetching live headlines from Pakistan...
        </marquee>
        <button onclick="toggleMarquee()" class="text-xs text-white border border-yellow-400 px-2 py-1 rounded hover:bg-yellow-500 hover:text-black">⏯</button>
      </div>
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

  <!-- Main Section -->
  <section id="home" class="h-screen flex items-center justify-center bg-black bg-opacity-50">
    <div class="bg-black bg-opacity-60 p-10 rounded-xl text-center max-w-xl">
      <h2 class="text-4xl font-bold mb-4">Stay Informed. Stay Ahead.</h2>
      <p class="text-lg mb-6">The latest news and sharp opinions, straight from your laptop.</p>
      <a href="#categories" class="bg-blue-600 hover:bg-blue-700 px-6 py-3 rounded-full transition">Explore Categories</a>
    </div>
  </section>

  <!-- Live News Channels -->
  <section id="live-news" class="py-16 px-6 bg-gray-950 bg-opacity-90">
    <div class="max-w-6xl mx-auto">
      <h3 class="text-3xl font-bold mb-10 text-center text-white">Live News Channels</h3>
      <div class="grid grid-cols-1 md:grid-cols-3 gap-8">
        <div class="bg-gray-800 p-4 rounded-xl text-center shadow-lg">
          <h4 class="text-xl font-bold text-yellow-400 mb-2">ARY News (Live)</h4>
          <iframe class="w-full h-48" src="https://www.youtube.com/embed/live_stream?channel=UCqwUrj10mAEsqezcItqvwEw" frameborder="0" allowfullscreen></iframe>
        </div>
        <div class="bg-gray-800 p-4 rounded-xl text-center shadow-lg">
          <h4 class="text-xl font-bold text-yellow-400 mb-2">Geo News (Live)</h4>
          <iframe class="w-full h-48" src="https://www.youtube.com/embed/live_stream?channel=UCr8oc-LOaApCXWLjBp-F3CQ" frameborder="0" allowfullscreen></iframe>
        </div>
        <div class="bg-gray-800 p-4 rounded-xl text-center shadow-lg">
          <h4 class="text-xl font-bold text-yellow-400 mb-2">92 News (Live)</h4>
          <iframe class="w-full h-48" src="https://www.youtube.com/embed/live_stream?channel=UC27z6mRtD9pN7M3msqRBj2A" frameborder="0" allowfullscreen></iframe>
        </div>
      </div>
    </div>
  </section>

  <!-- Blogs (unchanged) -->
  <!-- ... Existing Blogs Section ... -->

  <!-- Sports News Section (unchanged) -->
  <!-- ... Existing Sports Section ... -->

  <!-- News Fetch Scripts -->
  <script>
    async function fetchNews(url, updateCallback, fallbackMessage, append = false) {
      try {
        const response = await fetch(url);
        const data = await response.json();
        if (!data.items || !Array.isArray(data.items)) throw new Error('Invalid data format');
        updateCallback(data.items, null, append);
      } catch (error) {
        console.error("News fetch failed:", error);
        updateCallback(null, fallbackMessage);
      }
    }

    function updateSportsList(items, fallback, append = false) {
      const sportsList = document.getElementById('sports-news-list');
      if (!append) sportsList.innerHTML = '';
      if (!items) {
        if (!append) sportsList.innerHTML = `<li>${fallback}</li>`;
        return;
      }
      items.slice(0, 5).forEach(item => {
        const li = document.createElement('li');
        li.textContent = '🏏 ' + item.title;
        sportsList.appendChild(li);
      });
    }

    function updateMarquee(items, fallback) {
      const marquee = document.getElementById('live-news-marquee');
      if (!items) {
        marquee.textContent = fallback;
        return;
      }
      marquee.textContent = '📢 ' + items.slice(0, 8).map(item => item.title).join(' | ');
    }

    const newsFeeds = [
      {
        url: 'https://api.rss2json.com/v1/api.json?rss_url=https://www.espncricinfo.com/rss/content/story/feeds/0.xml',
        callback: updateSportsList,
        fallback: '⚠️ Unable to load Cricket news.'
      },
      {
        url: 'https://api.rss2json.com/v1/api.json?rss_url=https://www.geo.tv/rss/1',
        callback: updateMarquee,
        fallback: '⚠️ Unable to load Pakistani news headlines.'
      }
    ];

    function updateAllFeeds() {
      newsFeeds.forEach(feed => {
        fetchNews(feed.url, feed.callback, feed.fallback);
      });
    }

    function toggleMarquee() {
      const marquee = document.getElementById('live-news-marquee');
      if (marquee.getAttribute('behavior') === 'scroll') {
        marquee.setAttribute('behavior', 'alternate');
        marquee.stop();
      } else {
        marquee.setAttribute('behavior', 'scroll');
        marquee.start();
      }
    }

    updateAllFeeds();
    setInterval(updateAllFeeds, 60000);
  </script>

</body>
</html>
