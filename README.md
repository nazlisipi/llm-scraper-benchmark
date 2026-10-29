# LLM Scraper Benchmark

AIMultiple benchmark of scraping providers that collect answers from ChatGPT, Perplexity, Google AI Mode and Gemini. It measures how often each provider delivers a usable answer and how many metadata fields it returns.

> [Read the benchmark on AIMultiple](https://aimultiple.com/llm-scrapers)

## Workload

Each provider received 100 unique prompts, each run 10 times, for 1,000 tests. The prompts are open-ended technical questions about AI and machine learning, with a ten-minute timeout per prompt.

Each prompt carries 5 keywords expected in a relevant answer. An answer with none of them counts as incorrectly extracted, and non-empty citations must include at least one valid HTTP or HTTPS URL. The article tracks submission, execution and validation success, and reports validation success. Metadata is the count of structured fields returned with the answer text.

## Benchmark results

Validation success rate, with metadata fields in parentheses. The article omits results under its 90% threshold.

| Provider | ChatGPT | Perplexity | Google AI Mode |
| --- | --- | --- | --- |
| Bright Data | 99% (25) | 100% (18) | 100% (11) |
| Oxylabs | below 90% | 94% (13) | 98% (12) |
| Decodo | 98% (4) | 96% (9) | 95% (4) |
| Apify | 99% (4) | below 90% | below 90% |

In ChatGPT mode, all three charted providers reach 98% or more, but Bright Data returns 25 fields while Apify and Decodo return 4. Bright Data was the only provider that used Gemini for prompt-based scraping and reached 100% with 14 fields.

## Scope

Results cover one prompt set and the scrapers as tested for the article, last updated Jun 29, 2026. SerpApi and ScrapingBee appear in the article without benchmark figures.

## Ownership

The benchmark implementation was developed for AIMultiple and belongs to AIMultiple. This repository contains a documentation summary. Source code and benchmark datasets are not distributed here.
