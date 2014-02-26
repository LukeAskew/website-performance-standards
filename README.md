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

TODO

#### <a name="link">&#10697; Frames</a> 

TODO 

#### <a name="link">&#9872; Page Speed</a> 

TODO 


## Code Quality

TODO: define code quality standards specific to performance.

- Progressive JPGs
- CSS
    + Only CSS in head
    + Inefficient selectors
- JS
    + ???


## Guidelines

TODO: fill in each with a brief summary/guideline

- [Google's web performance best practices](https://developers.google.com/speed/docs/best-practices/rules_intro)
- [Designers](https://speakerdeck.com/lara/design-for-performance)

## Additional Resources

TODO




