# Resource Website Performance Standards

This document provides [research-based](#sources) KPIs for measuring the performance of websites.

**These are not recommendations**. The KPIs should be treated as <span style="color:green">pass</span>/<span style="color:red">fail</span>. Any failing KPI should be considered a *blocker* unless otherwise agreed upon by the project team.

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
Time to first byte | **250ms** | [&#9992;](#responsiveness)
Load time | **2s** | [&#9992;](#responsiveness)
Page size | **1333kb** (1.3mb) | [&#9992;](#responsiveness)
Time to interact | **3s** | [&#9992;](#responsiveness)
API response | **500ms** | [&#9992;](#responsiveness)
Animation | **60fps** (16.6ms) | [&#10697;](#frames)
Page speed score | **85/100** | [&#9872;](#pagespeed)

### Definitions

- **Time to first byte:** (TTFB) The time from the start of the initial request until the first byte is received by the browser. [More info](http://www.webpagetest.org/forums/showthread.php?tid=11441&pid=18155#pid18155)
- **Load time:** The time from the start of the initial request until all the page's dependent assets have been loaded.
- **Page size:** The amount of data transfered up until the page is considered "loaded". See [calculation methodology](http://www.dslreports.com/calculator?sz=1333+KB&time=2+s&c2=Calc&speed=5+Mbps)
- **Time to interact**: (TTI) Time of the last visual change to the page; a cue to the user that the page is ready to be interacted with. Also known as "visually complete".
- **API response:** The round trip time for a response from an API.
- **Animation:** The [frame rate](https://developers.google.com/chrome-developer-tools/docs/timeline#frames_mode) at which animation/movement is performed.
- **Page speed score:** Score determined by Google's [PageSpeed Insights tool](http://developers.google.com/speed/pagespeed/insights/).

### Testing Methodology

#### <span name="responsiveness">&#9992; Responsiveness</span> 

Use [webpagetest.org](http://www.webpagetest.org/) to test a web page. 

Use [Postman](https://chrome.google.com/webstore/detail/postman-rest-client/fdmmgilgnpjigdojojpjoooidkmcomcm) to test an API.

#### <span name="link">&#10697; Frames</span> 

Use Chrome Dev Tools' [Frames Mode](http://blog.chromium.org/2012/11/build-smoother-web-apps-with-chrome.html) to measure frames per second.

Any event that breaks through the 60fps threshold should be noted.

<img src="http://i.imgur.com/x0t1jCG.png" alt="" />

#### <span name="link">&#9872; Page Speed</span> 

 Use [Google's PageSpeed Insights](http://developers.google.com/speed/pagespeed/insights/).


## Guidelines

- Follow Google's [Web Performance Best Practices](https://developers.google.com/speed/docs/best-practices/rules_intro)
- Designers and developers **must** collaborate in order to deliver performant websites. [Good performance is good design](http://laraswanson.com/design/).
- Performance testing can be performed at any point in the project lifecycle. Some responsiveness KPIs can be verified before any code is written.

## Educational Resources

- http://www.youtube.com/watch?v=z0_jD8nO5Zw
- http://jankfree.org/
- http://addyosmani.com/blog/performance-optimisation-with-timeline-profiles/
- http://moz.com/blog/how-website-speed-actually-impacts-search-ranking
- https://github.com/Snugug/north#performance
- http://aerotwist.com/blog/dont-guess-it-test-it/

## Sources

- http://www.damcogroup.com/white-papers/ecommerce_website_perf_wp.pdf
- http://www.phocuswright.com/free_reports/consumer-response-to-travel-site-performance
- http://www.getelastic.com/ttfb-and-tti-2-kpis-more-important-than-page-load-speed/
- http://www.webperformancetoday.com/2013/10/15/new-findings-typical-leading-ecommerce-site-takes-5-3-seconds-to-become-interactive/
- http://blog.kissmetrics.com/loading-time/
- http://www.akamai.com/dl/reports/Site_Abandonment_Final_Report.pdf


