# Parallel Web Crawler

This project implements a web crawler designed to explore and retrieve web pages efficiently by taking advantage of parallel execution. Traditional web crawlers process pages sequentially, but this project upgrades the crawler to use multiple threads or concurrent workers to improve throughput and discover more pages in less time.

The crawler starts from one or more seed URLs, follows links found on each page, and adds new URLs to the processing queue. By using parallel execution, it visits multiple URLs simultaneously, improving performance compared to a legacy single-threaded crawler.

## Project Overview

Web crawling is a key technique for indexing content on the internet, gathering data, and supporting search engines or analytical systems. A parallel web crawler distributes the workload across multiple threads or processes to speed up page retrieval and link discovery.

This repository provides a starter codebase and configuration for a parallel web crawler. The focus is on upgrading a legacy single-threaded crawler to leverage modern multi-core architectures to increase crawl throughput. It also includes performance measurement to demonstrate that a parallel implementation can visit more pages in the same amount of time.

## Objectives

- Improve crawl speed by using parallel execution
- Measure and compare throughput against a sequential crawler
- Maintain a scalable architecture for adding new crawling strategies
- Provide a foundation for further research or real-world crawling tasks

## Technologies and Tools

- Language: Java (requires Java 11 or higher)
- Build Tool: Maven (3.6.3 or higher)
- Development Environment: compatible with IntelliJ IDEA or similar IDE
- Libraries: standard Java concurrency utilities
- Outputs: performance results and downloaded content

## How It Works

The crawler reads seed URLs and uses a pool of worker threads to download pages in parallel. As each page is fetched, URLs contained within it are extracted and added to a shared queue. Workers consume URLs from this queue and continue crawling until a stopping condition is reached. Performance is measured to show the benefits of parallelism versus sequential execution.

## Getting Started

Before running the project, make sure you have JDK 11 or later installed and Maven set up on your system. You can use an IDE like IntelliJ IDEA to explore and build the project, or you can use terminal commands.

## Typical Workflow

1. Clone the repository to your local machine
2. Navigate to the project root where the pom.xml file is located
3. Build the project using Maven or your IDE
4. Run unit tests and verify functionality
5. Execute the crawler and observe performance improvements

## Use Cases and Applications

Parallel web crawlers are essential for search engine indexing, large-scale data collection, research on web structures, and analytics applications that require broad and deep coverage of online content. They can also serve as the foundation for distributed crawling systems and future enhancements involving scheduling and politeness policies.

## Conclusion

This Parallel Web Crawler project demonstrates how upgrading from a sequential to a parallel crawling approach can significantly improve performance on modern multi-core systems. It provides a scalable structure for further enhancements and practical use in large-scale web exploration tasks. The repository includes example code, testing configurations, and documentation to help you extend the crawler to meet your needs.
