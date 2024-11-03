# Scripture Source

Scripture Source is an open-source project dedicated to making gospel resources more accessible. This repository houses a Rust-based back-end API that scrapes and indexes Latter-day Saint scriptures, general conference talks, apocryphal books, and Hebrew and Greek cross-references, with SDKs for Rust, JavaScript, Python, SwiftUI, and Kotlin to simplify integration across platforms.

## License

This project is licensed under the Apache License 2.0.

## Project Overview

Scripture Source provides a single, unified API for querying and cross-referencing a range of gospel resources. Users can look up passages, retrieve cross-references, and integrate data effortlessly into their applications using SDKs in multiple languages.

### Features

- Rust Back-End API: The core of Scripture Source, written in Rust, provides high performance for data scraping, indexing, and querying.
- Cross-Reference Functionality: Cross-reference between scriptures, conference talks, apocryphal texts, and Greek/Hebrew translations.
- Multi-Language SDKs: Integration SDKs in Rust, JavaScript, Python, Swift (SwiftUI), and Kotlin for broad platform support.
- Single Query Interface: Enables a consistent query experience to retrieve scripture passages and contextual references.

### Repository Structure

- /api: Rust-based back-end API for data scraping and query handling.
- /sdk-rust: Rust SDK for integration with Rust applications.
- /sdk-js: JavaScript SDK for front-end frameworks and Node.js.
- /sdk-python: Python SDK for data science and server-side use.
- /sdk-swift: Swift SDK for iOS/macOS applications with SwiftUI compatibility.
- /sdk-kotlin: Kotlin SDK for Android and JVM-based environments.

## Getting Started

### Prerequisites

- Rust: Required to build and run the back-end API.
- Node.js: Required for the JavaScript SDK and Node usage.
- Python: Required for the Python SDK.
- Xcode: For developing with the Swift SDK.
- Android Studio: For working with the Kotlin SDK on Android.

### Installation

1. Clone the repository:

```
git clone https://github.com/kenthejr/scripture-source
cd scripture-source
```

2. Set up the Back-End API:

- Navigate to the /backend directory and follow the installation instructions in the README to build and start the server.

3. SDK Setup:

- Each SDK includes its own README with setup instructions and usage examples.

### Usage

Each SDK offers a simple interface to connect with the back-end API. Refer to each SDK’s documentation for specific examples.

#### Example Queries

```
// Rust Example
let query = sdk_rust::query_scripture("John 3:16").await?;
```

```
// JavaScript Example
sdk_js.queryScripture("John 3:16").then(console.log);
```

```
# Python Example
from sdk_python import query_scripture
print(query_scripture("John 3:16"))
```

## Contribution

We welcome contributions! To help expand this project, fork the repo, make your changes, and submit a pull request.

This README now includes the project name “Scripture Source” and the Apache 2.0 licensing. Let me know if you need further customization!
