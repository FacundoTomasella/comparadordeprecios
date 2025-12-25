const CACHE_NAME = 'tradingchango-v1';
const ASSETS = [
  '/',
  '/index.html',
  // Agrega aquí tus archivos CSS o imágenes principales si los tienes por separado
];

self.addEventListener('install', (e) => {
  e.waitUntil(
    caches.open(CACHE_NAME).then((cache) => cache.addAll(ASSETS))
  );
});

self.addEventListener('fetch', (e) => {
  e.respondWith(
    caches.match(e.request).then((res) => res || fetch(e.request))
  );
});
