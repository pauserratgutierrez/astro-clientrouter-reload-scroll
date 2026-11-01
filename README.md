# ClientRouter: a reload paints the top of the page before the scroll is restored

Two identical long pages: `/` has `<ClientRouter />`, `/native` does not.

1. `npm install`, then `npm run build && npm run preview` (or `npm run dev`).
2. Open `/` in Chrome, scroll far down (to Section 50 or so).
3. In DevTools, Network, set throttling to "Slow 4G" (any throttling makes it longer).
4. Reload the page: it paints at its top (Section 1) and then jumps back to where it was.
5. Do the same on `/native`: the page comes back where it was from its first frame.
