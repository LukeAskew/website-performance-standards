# Resource Website Performance Standards

TODO: Summary

This document is intentionally void of any specific tactical requirements such as caching and compression. Issues with implementation are revealed by the various testing resources.

## Metrics

### Test setup

Variable | Definition
--- | ---
Location | **Regional** (same continent)
Connection Speed | **5 Mbps** (Cable)
Browser | **Google Chrome**

### KPIs

Metric | Standard | Methodology
--- | --- | ---
Time to first byte | **200ms** | [&#9992;](#responsiveness)
Load time | **2s** | [&#9992;](#responsiveness)
Page size | **1333kb** (1.3mb) | [&#9992;](#responsiveness)
Time to interact | **3s** | [&#9992;](#responsiveness)
API response | **500ms** | [&#9992;](#responsiveness)
Animation | **60fps** (16.6ms) | [&#10697;](#frames)
Page speed score | **75/100** | [&#9872;](#pagespeed)

### Definitions

- **Time to first byte:** (TTFB) The time from the start of the initial request until the first byte is received by the browser. 
- **Load time:** The time from the start of the initial request until all the page's dependent assets have been loaded.
- **Page size:** The amount of data transfered up until the page is considered "loaded". See [calculation methodology](http://www.dslreports.com/calculator?sz=1333+KB&time=2+s&c2=Calc&speed=5+Mbps)
- **Time to interact**: (TTI) Time of the last visual change to the page. Also known as "visually complete".
- **API response:** The round trip time for a response from an API.
- **Animation:** The [frame rate](https://developers.google.com/chrome-developer-tools/docs/timeline#frames_mode) at which animation/movement is performed.
- **Page speed score:** Score determined by Google's [PageSpeed Insights tool](http://developers.google.com/speed/pagespeed/insights/).

### Testing Methodology

#### <a name="responsiveness">&#9992; Responsiveness</a> 

Use [webpagetest.org](http://www.webpagetest.org/).

#### <a name="link">&#10697; Frames</a> 

Use Chrome Dev Tools' [Frames Mode](http://blog.chromium.org/2012/11/build-smoother-web-apps-with-chrome.html) to measure frames per second.

Any event that breaks through the 60fps threshold should be noted.

<img src="http://i.imgur.com/x0t1jCG.png" alt="" />

#### <a name="link">&#9872; Page Speed</a> 

 Use [Google's PageSpeed Insights](http://developers.google.com/speed/pagespeed/insights/).

## Code Quality

- **CSS**
    + Only in the `<head>`
    + Avoid [inefficient selectors](https://github.com/resource/Front-End-Standards/blob/master/Stylesheets/CSS.md#efficiency)
- **JS**
    + Avoid binding window events (scroll, resize); [throttle](http://drupalmotion.com/article/debounce-and-throttle-visual-explanation) when you do.
    + Load scripts at the bottom of the document, immediately before the closing `</body>`.
    + Concatenate scripts when possible.
- **HTML**
    + Keep DOM [node depth](https://developer.mozilla.org/en-US/docs/Tools/3D_View) to a minimum
- **Images**
    + Appropriate format
        * **PNG**: limited color complexity
            - 8-bit standard; 24 bit for complex transparency
        * **JPG**: tons of color (photographs)
            - Must be [progressive](http://calendar.perfplanet.com/2012/progressive-jpegs-a-new-best-practice/)    


## Guidelines

- Google's [Web Performance Best Practices](https://developers.google.com/speed/docs/best-practices/rules_intro)
- [Good performance is good design](http://laraswanson.com/design/). Designers and developers must collaborate in order to deliver performant websites.
- Performance testing can be performed at any point in the project lifecycle. Some responsiveness KPIs can be verified before any code is written.

## Additional Resources

http://www.youtube.com/watch?v=z0_jD8nO5Zw
http://jankfree.org/
http://addyosmani.com/blog/performance-optimisation-with-timeline-profiles/
http://moz.com/blog/how-website-speed-actually-impacts-search-ranking

## Sources

http://www.damcogroup.com/white-papers/ecommerce_website_perf_wp.pdf
http://www.phocuswright.com/free_reports/consumer-response-to-travel-site-performance
http://www.getelastic.com/ttfb-and-tti-2-kpis-more-important-than-page-load-speed/
http://www.webperformancetoday.com/2013/10/15/new-findings-typical-leading-ecommerce-site-takes-5-3-seconds-to-become-interactive/
http://blog.kissmetrics.com/loading-time/
http://www.akamai.com/dl/reports/Site_Abandonment_Final_Report.pdf


