# What is it?
- A compiled notes I made from a couple of youtube videos.
- Links
  - https://www.youtube.com/watch?v=YJGCZCaIZkQ

## Performance budgets(PB)
- For many sites maintaining performance is just difficult than having performant in the first place.
- In a internal study by Google, 40% of brands regress on performance after 6 months.
- Performace budgets sets standard for the performance of your site.
- PB can be based on
  - time (e.g: less than 2s TTI)
  - resources(e.g: < 150kb JS)
  - metrics (e.g: Lighthouse score)
- Just like tests catch code issues, PB catches performance issues.
- Tools to measure PB
  - Lightwallet (https://web.dev/use-lighthouse-for-performance-budgets/)
  - Performance budget calculator allows us to forecast 
    TTI based on the JS and non-Js resources of your site.
    (http://bit.ly/perf-budget-calculator)

## Images
   - lazy loading: reduces initial load by almost 70%.
   - responsive images: by width or by density
   - Image CDN
     - Trivage ported to a image CDN by cloudinary.

## Javascript size
   > "If Javascript doesn't bring user joy , thank it and throw it away"
 
   - use of `<script defer>` instead of `<script>`
   - lazy load third-party embeds
   - remove expensive libraries
     - tree-shakable library instead of whole library
       - lodash ----> lodash-es
       - moment ----> date-fns
       - fetch  ----> fetch-unfetch
     - e.g: Tokopedia uses Svelte on their landing page instead of React.They didnot rewrite their entire site to Svelte.
     - Update libraries: e.g: Update react old version to new version to reduce load times. 
     - code-splitting - smaller js bundles
       - download: critical for 2g/3g (slow networks)
       - js execution: critical for devices with slow CPUs
     - PRPL Pattern (Push,Render,Precache,Lazyload)
       - `Push` minimal code to get interactive
       - `Render` fast
       - `Precache` other routes(SW)
       - `Lazyload` Js On demand

## Fonts
- By default, if a font is not loaded the browser will hide text for upto 3s(chrome,firefox)
- use font-display: swap

## Compression
- A new compression library  (better than Gzip)
  - Used by OYO (compress JS and CSS)
  - Used by Twitter (compress API responses)
