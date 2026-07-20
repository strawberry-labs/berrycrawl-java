# Reference
<details><summary><code>client.crawl(request) -> JobCreatedResponse</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```java
client.crawl(
    CrawlDto
        .builder()
        .url("https://example.com")
        .build()
);
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**allowExternalLinks:** `Optional<Boolean>` — Whether to allow crawling external domains
    
</dd>
</dl>

<dl>
<dd>

**allowSubdomains:** `Optional<Boolean>` — Whether to allow crawling subdomains
    
</dd>
</dl>

<dl>
<dd>

**crawlEntireDomain:** `Optional<Boolean>` — Whether to crawl entire domain or just subtree
    
</dd>
</dl>

<dl>
<dd>

**deduplicateSimilarUrLs:** `Optional<Boolean>` — Deduplicate similar URLs using intelligent matching
    
</dd>
</dl>

<dl>
<dd>

**delay:** `Optional<Double>` — Delay between page scrapes in milliseconds
    
</dd>
</dl>

<dl>
<dd>

**excludePaths:** `Optional<List<String>>` — Regex patterns to exclude paths
    
</dd>
</dl>

<dl>
<dd>

**ignoreQueryParameters:** `Optional<Boolean>` — Ignore query parameters when deduplicating URLs
    
</dd>
</dl>

<dl>
<dd>

**includePaths:** `Optional<List<String>>` — Regex patterns to include paths
    
</dd>
</dl>

<dl>
<dd>

**limit:** `Optional<Double>` — Maximum number of pages to crawl
    
</dd>
</dl>

<dl>
<dd>

**maxConcurrency:** `Optional<Double>` — Maximum number of concurrent scrapes for this crawl
    
</dd>
</dl>

<dl>
<dd>

**maxDiscoveryDepth:** `Optional<Double>` — Maximum depth for URL discovery
    
</dd>
</dl>

<dl>
<dd>

**prompt:** `Optional<String>` — Natural language instructions for crawl configuration
    
</dd>
</dl>

<dl>
<dd>

**scrapeOptions:** `Optional<Map<String, Object>>` — Scrape options to apply to each page. actions accepts at most 25 bounded browser actions. zeroDataRetention: true is currently rejected with 400 ZERO_DATA_RETENTION_NOT_SUPPORTED.
    
</dd>
</dl>

<dl>
<dd>

**sitemap:** `Optional<CrawlDtoSitemap>` — Sitemap handling strategy
    
</dd>
</dl>

<dl>
<dd>

**url:** `String` — Starting URL to crawl
    
</dd>
</dl>

<dl>
<dd>

**webhook:** `Optional<WebhookConfigDto>` — Webhook configuration
    
</dd>
</dl>

<dl>
<dd>

**zeroDataRetention:** `Optional<Boolean>` — Reserved for a future zero-data-retention mode. true is currently rejected with 400 ZERO_DATA_RETENTION_NOT_SUPPORTED; omit or use false.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.extract(request) -> JobCreatedResponse</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```java
client.extract(
    ExtractDto
        .builder()
        .prompt("Extract all product names, prices, and descriptions from these pages")
        .build()
);
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**agent:** `Optional<AgentConfigDto>` — Agent configuration
    
</dd>
</dl>

<dl>
<dd>

**enableWebSearch:** `Optional<Boolean>` — Enable web search for URL discovery
    
</dd>
</dl>

<dl>
<dd>

**ignoreInvalidUrLs:** `Optional<Boolean>` — Ignore invalid URLs and process remaining valid ones
    
</dd>
</dl>

<dl>
<dd>

**ignoreSitemap:** `Optional<Boolean>` — Ignore sitemap during URL discovery
    
</dd>
</dl>

<dl>
<dd>

**includeSubdomains:** `Optional<Boolean>` — Include subdomains in extraction
    
</dd>
</dl>

<dl>
<dd>

**prompt:** `String` — Natural language prompt describing what to extract. Maximum 16384 UTF-8 bytes.
    
</dd>
</dl>

<dl>
<dd>

**schema:** `Optional<Map<String, Object>>` — JSON Schema for structured output. Serialized schema is limited to 65536 UTF-8 bytes.
    
</dd>
</dl>

<dl>
<dd>

**scrapeOptions:** `Optional<Map<String, Object>>` — Scrape options for each URL. zeroDataRetention: true is currently rejected with 400 ZERO_DATA_RETENTION_NOT_SUPPORTED.
    
</dd>
</dl>

<dl>
<dd>

**showSources:** `Optional<Boolean>` — Include source citations in response
    
</dd>
</dl>

<dl>
<dd>

**urls:** `Optional<List<String>>` — 1–20 unique public HTTP(S) URLs. May be omitted only when enableWebSearch is true. Each URL is limited to 2048 UTF-8 bytes.
    
</dd>
</dl>

<dl>
<dd>

**webhook:** `Optional<ExtractWebhookConfigDto>` — Webhook configuration
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.map(request) -> MapResponse</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```java
client.map(
    MapDto
        .builder()
        .url("https://example.com")
        .build()
);
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**ignoreQueryParameters:** `Optional<Boolean>` — Ignore query parameters when discovering URLs
    
</dd>
</dl>

<dl>
<dd>

**includeSubdomains:** `Optional<Boolean>` — Include subdomains in the map
    
</dd>
</dl>

<dl>
<dd>

**limit:** `Optional<Double>` — Maximum number of URLs to return
    
</dd>
</dl>

<dl>
<dd>

**location:** `Optional<LocationDto>` — Location configuration
    
</dd>
</dl>

<dl>
<dd>

**search:** `Optional<String>` — Search filter for URLs
    
</dd>
</dl>

<dl>
<dd>

**sitemap:** `Optional<MapDtoSitemap>` — How to handle sitemaps
    
</dd>
</dl>

<dl>
<dd>

**timeout:** `Optional<Double>` — Timeout for map operation in milliseconds
    
</dd>
</dl>

<dl>
<dd>

**url:** `String` — URL to map
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.parse(request) -> ScrapeResponse</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```java
client.parse(
    ParseDto
        .builder()
        .url("https://example.com/report.pdf")
        .build()
);
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**timeout:** `Optional<Double>` 
    
</dd>
</dl>

<dl>
<dd>

**url:** `String` — Public PDF, Word document, or spreadsheet URL
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.scrape(request) -> ScrapeResponse</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```java
client.scrape(
    ScrapeDto
        .builder()
        .build()
);
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**actions:** `Optional<List<ActionDto>>` — Browser actions to execute
    
</dd>
</dl>

<dl>
<dd>

**blockAds:** `Optional<Boolean>` — Enable ad-blocking and cookie popup blocking
    
</dd>
</dl>

<dl>
<dd>

**domain:** `Optional<String>` — Domain to scrape. Normalized to https://domain when url is omitted.
    
</dd>
</dl>

<dl>
<dd>

**excludeTags:** `Optional<List<String>>` — CSS selectors to exclude
    
</dd>
</dl>

<dl>
<dd>

**extractionSchema:** `Optional<Map<String, Object>>` — Schema for structured data extraction (used with json format)
    
</dd>
</dl>

<dl>
<dd>

**formats:** `Optional<List<ScrapeDtoFormatsItem>>` — Output formats - can be simple strings or format objects with options
    
</dd>
</dl>

<dl>
<dd>

**headers:** `Optional<Map<String, Object>>` — Custom headers
    
</dd>
</dl>

<dl>
<dd>

**includeTags:** `Optional<List<String>>` — CSS selectors to include
    
</dd>
</dl>

<dl>
<dd>

**location:** `Optional<LocationDto>` — Location settings
    
</dd>
</dl>

<dl>
<dd>

**maxAge:** `Optional<Double>` — Cache max age in milliseconds
    
</dd>
</dl>

<dl>
<dd>

**mobile:** `Optional<Boolean>` — Emulate mobile device for scraping
    
</dd>
</dl>

<dl>
<dd>

**onlyMainContent:** `Optional<Boolean>` — Extract only main content
    
</dd>
</dl>

<dl>
<dd>

**proxy:** `Optional<ScrapeDtoProxy>` — Proxy mode. auto starts direct and escalates only when blocked. basic is an alias for none.
    
</dd>
</dl>

<dl>
<dd>

**removeBase64Images:** `Optional<Boolean>` — Remove base64 images from output (keeps alt text)
    
</dd>
</dl>

<dl>
<dd>

**screenshotAsBase64:** `Optional<Boolean>` — Return screenshot/PDF output inline as a base64 data URL instead of an uploaded CDN URL. Default false (a CDN URL is returned).
    
</dd>
</dl>

<dl>
<dd>

**skipTlsVerification:** `Optional<Boolean>` — Skip TLS certificate verification
    
</dd>
</dl>

<dl>
<dd>

**storeInCache:** `Optional<Boolean>` — Store result in cache
    
</dd>
</dl>

<dl>
<dd>

**timeout:** `Optional<Double>` — Request timeout in milliseconds
    
</dd>
</dl>

<dl>
<dd>

**url:** `Optional<String>` — URL to scrape. Either url or domain is required.
    
</dd>
</dl>

<dl>
<dd>

**waitFor:** `Optional<Double>` — Wait time before scraping (ms)
    
</dd>
</dl>

<dl>
<dd>

**zeroDataRetention:** `Optional<Boolean>` — Reserved for a future zero-data-retention mode. true is currently rejected with 400 ZERO_DATA_RETENTION_NOT_SUPPORTED; omit or use false.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.screenshot(request) -> ScrapeResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Cookie banners, blocking overlays, chat widgets, and lazy loading are handled by default. Every cleanup pass can be controlled per request.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```java
client.screenshot(
    ScreenshotDto
        .builder()
        .url("https://example.com")
        .build()
);
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**blockAds:** `Optional<Boolean>` — Block common advertising and analytics requests
    
</dd>
</dl>

<dl>
<dd>

**clickSelector:** `Optional<String>` — Click this CSS selector before capture
    
</dd>
</dl>

<dl>
<dd>

**clip:** `Optional<ScreenshotClipDto>` — Capture an exact pixel rectangle instead of the page
    
</dd>
</dl>

<dl>
<dd>

**colorScheme:** `Optional<ScreenshotDtoColorScheme>` 
    
</dd>
</dl>

<dl>
<dd>

**cookies:** `Optional<List<ScreenshotCookieDto>>` — Cookies to set before loading the page
    
</dd>
</dl>

<dl>
<dd>

**delay:** `Optional<Double>` — Extra settling time after the page is ready, in milliseconds
    
</dd>
</dl>

<dl>
<dd>

**device:** `Optional<ScreenshotDtoDevice>` — Named viewport preset
    
</dd>
</dl>

<dl>
<dd>

**disableAnimations:** `Optional<Boolean>` 
    
</dd>
</dl>

<dl>
<dd>

**format:** `Optional<ScreenshotDtoFormat>` 
    
</dd>
</dl>

<dl>
<dd>

**fullPage:** `Optional<Boolean>` — Capture the complete page instead of only the viewport
    
</dd>
</dl>

<dl>
<dd>

**fullPageAlgorithm:** `Optional<ScreenshotDtoFullPageAlgorithm>` — auto uses native capture for normal pages and stitched slices for very tall pages
    
</dd>
</dl>

<dl>
<dd>

**headers:** `Optional<Map<String, Object>>` — Headers sent while loading the page
    
</dd>
</dl>

<dl>
<dd>

**hideFixedElements:** `Optional<Boolean>` — Show fixed/sticky UI once instead of repeating it in stitched captures
    
</dd>
</dl>

<dl>
<dd>

**hideSelectors:** `Optional<List<String>>` — Hide matching elements before capture
    
</dd>
</dl>

<dl>
<dd>

**location:** `Optional<ScreenshotLocationDto>` 
    
</dd>
</dl>

<dl>
<dd>

**maskColor:** `Optional<String>` 
    
</dd>
</dl>

<dl>
<dd>

**maskSelectors:** `Optional<List<String>>` — Cover matching elements with a solid privacy mask
    
</dd>
</dl>

<dl>
<dd>

**maxHeight:** `Optional<Double>` — Maximum full-page height. Prevents endless captures on infinite pages.
    
</dd>
</dl>

<dl>
<dd>

**omitBackground:** `Optional<Boolean>` — Use a transparent background where the page allows it
    
</dd>
</dl>

<dl>
<dd>

**proxy:** `Optional<ScreenshotDtoProxy>` — Proxy mode
    
</dd>
</dl>

<dl>
<dd>

**quality:** `Optional<Double>` — JPEG or WebP quality
    
</dd>
</dl>

<dl>
<dd>

**reducedMotion:** `Optional<Boolean>` 
    
</dd>
</dl>

<dl>
<dd>

**removeChatWidgets:** `Optional<Boolean>` — Hide common support and chat widgets
    
</dd>
</dl>

<dl>
<dd>

**removeCookieBanners:** `Optional<Boolean>` — Accept known consent dialogs, hide remaining cookie banners, and restore page scrolling
    
</dd>
</dl>

<dl>
<dd>

**removeOverlays:** `Optional<Boolean>` — Remove newsletter gates, modal backdrops, and blocking overlays
    
</dd>
</dl>

<dl>
<dd>

**responseFormat:** `Optional<ScreenshotDtoResponseFormat>` — Return a CDN URL or an inline data URL
    
</dd>
</dl>

<dl>
<dd>

**scale:** `Optional<ScreenshotDtoScale>` — Capture at CSS pixel size or the emulated device pixel ratio
    
</dd>
</dl>

<dl>
<dd>

**scrollDelay:** `Optional<Double>` — Pause between lazy-load scroll steps, in milliseconds
    
</dd>
</dl>

<dl>
<dd>

**scrollPage:** `Optional<Boolean>` — Scroll through the page first so lazy content is loaded
    
</dd>
</dl>

<dl>
<dd>

**selector:** `Optional<String>` — Capture one element instead of the page
    
</dd>
</dl>

<dl>
<dd>

**styles:** `Optional<List<String>>` — CSS rules to apply before capture
    
</dd>
</dl>

<dl>
<dd>

**timeout:** `Optional<Double>` 
    
</dd>
</dl>

<dl>
<dd>

**url:** `String` — Public webpage URL to capture
    
</dd>
</dl>

<dl>
<dd>

**viewport:** `Optional<ScreenshotViewportDto>` — Custom viewport. Overrides the named device dimensions.
    
</dd>
</dl>

<dl>
<dd>

**waitForSelector:** `Optional<String>` — Wait for this CSS selector before capture
    
</dd>
</dl>

<dl>
<dd>

**waitUntil:** `Optional<ScreenshotDtoWaitUntil>` — Page readiness milestone used before capture
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.search(request) -> SearchResponse</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```java
client.search(
    SearchDto
        .builder()
        .query("machine learning tutorials")
        .build()
);
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**categories:** `Optional<List<String>>` — Category filters
    
</dd>
</dl>

<dl>
<dd>

**country:** `Optional<String>` — Country code
    
</dd>
</dl>

<dl>
<dd>

**limit:** `Optional<Double>` — Maximum number of results
    
</dd>
</dl>

<dl>
<dd>

**location:** `Optional<String>` — Location for geo-targeting
    
</dd>
</dl>

<dl>
<dd>

**query:** `String` — Search query
    
</dd>
</dl>

<dl>
<dd>

**sources:** `Optional<List<String>>` — Source types to search
    
</dd>
</dl>

<dl>
<dd>

**tbs:** `Optional<String>` — Time-based filter (e.g., qdr:d for past day)
    
</dd>
</dl>

<dl>
<dd>

**timeout:** `Optional<Double>` — Timeout for search operation in milliseconds
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

## Account
<details><summary><code>client.account.get() -> AccountResponse</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```java
client.account().get();
```
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

## Brand
<details><summary><code>client.brand.retrieve(request) -> BrandResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Send one website URL. BerryCrawl returns the brand identity found on that site.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```java
client.brand().retrieve(
    BrandDto
        .builder()
        .url("https://stripe.com")
        .build()
);
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**refresh:** `Optional<Boolean>` — Ignore a cached profile and fetch the website again
    
</dd>
</dl>

<dl>
<dd>

**timeout:** `Optional<Double>` — Maximum time to spend building the profile, in milliseconds
    
</dd>
</dl>

<dl>
<dd>

**url:** `String` — The public website whose brand profile should be extracted
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

## Jobs
<details><summary><code>client.jobs.list() -> ListJobsResponse</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```java
client.jobs().list(
    ListJobsRequest
        .builder()
        .build()
);
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**type:** `Optional<ListJobsRequestType>` 
    
</dd>
</dl>

<dl>
<dd>

**status:** `Optional<ListJobsRequestStatus>` 
    
</dd>
</dl>

<dl>
<dd>

**page:** `Optional<Double>` 
    
</dd>
</dl>

<dl>
<dd>

**limit:** `Optional<Double>` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.jobs.get(id) -> JobResponse</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```java
client.jobs().get(
    "id",
    GetJobsRequest
        .builder()
        .build()
);
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**id:** `String` 
    
</dd>
</dl>

<dl>
<dd>

**page:** `Optional<Double>` 
    
</dd>
</dl>

<dl>
<dd>

**limit:** `Optional<Double>` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.jobs.cancel(id) -> CancelJobResponse</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```java
client.jobs().cancel(
    "id",
    CancelJobsRequest
        .builder()
        .build()
);
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**id:** `String` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

## Webhooks
<details><summary><code>client.webhooks.list() -> ListWebhooksResponse</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```java
client.webhooks().list();
```
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.webhooks.create(request) -> WebhookResponse</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```java
client.webhooks().create(
    CreateWebhookDto
        .builder()
        .url("https://api.example.com/webhooks")
        .events(
            Arrays.asList("crawl.completed", "extract.failed")
        )
        .build()
);
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**events:** `List<String>` — Event types to subscribe to
    
</dd>
</dl>

<dl>
<dd>

**url:** `String` — Webhook URL to send events to
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.webhooks.get(id) -> WebhookResponse</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```java
client.webhooks().get(
    "id",
    GetWebhooksRequest
        .builder()
        .build()
);
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**id:** `String` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.webhooks.delete(id) -> MessageResponse</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```java
client.webhooks().delete(
    "id",
    DeleteWebhooksRequest
        .builder()
        .build()
);
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**id:** `String` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.webhooks.update(id, request) -> WebhookResponse</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```java
client.webhooks().update(
    "id",
    UpdateWebhookDto
        .builder()
        .build()
);
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**id:** `String` 
    
</dd>
</dl>

<dl>
<dd>

**events:** `Optional<List<String>>` — Event types to subscribe to
    
</dd>
</dl>

<dl>
<dd>

**isActive:** `Optional<Boolean>` — Enable or disable webhook
    
</dd>
</dl>

<dl>
<dd>

**url:** `Optional<String>` — Webhook URL to send events to
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.webhooks.test(id, request) -> TestWebhookResponse</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```java
client.webhooks().test(
    "id",
    TestWebhookDto
        .builder()
        .event("crawl.completed")
        .build()
);
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**id:** `String` 
    
</dd>
</dl>

<dl>
<dd>

**event:** `String` — Event type to test
    
</dd>
</dl>

<dl>
<dd>

**payload:** `Optional<Map<String, Object>>` — Optional custom payload for testing
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

