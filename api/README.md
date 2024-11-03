> [!WARNING]
> This is all initialization structure. The API affordances are not accurate. They will change. This README is simply here to outline the project as a Rust project.

# Scripture Source API (Back-End)

The Scripture Source API is the core of the Scripture Source project, providing a unified back-end service to query and cross-reference Latter-day Saint scriptures, general conference talks, apocryphal texts, and Hebrew and Greek cross-references. Built with Rust for performance and reliability, this API scrapes and indexes gospel resources, enabling fast and efficient access through a RESTful interface.

## Features

- Comprehensive Data: Pulls from various gospel resources, including the Latter-day Saint scriptures, general conference talks, apocryphal texts, and original-language cross-references.
- Cross-Referencing: Offers contextual connections between passages, allowing users to explore related scriptures and topics.
- High Performance: Rust-based back-end for fast, scalable access to large datasets.
- RESTful API: Provides a standardized, JSON-based API for easy integration with front-end and mobile applications.

## Installation

### Prerequisites

- Rust: Make sure Rust is installed on your machine. You can download it here.
- Database: This project may require a database for storing scraped data. See the Configuration section for details.

### Clone the Repository

```
git clone https://github.com/your-username/scripture-source
cd scripture-source/backend
```

### Build and Run

1. Install dependencies:

```
cargo build --release
```

2. Run the API:

```
cargo run --release
```

The API server should now be running locally.

### Configuration

Configuration options can be found in the config file (e.g., config.toml). Here you can set options such as:

- Database settings: Configure the database type, connection strings, etc.
- API settings: Set the server port, allowed origins for CORS, and other API-specific options.

### Usage

The Scripture Source API provides a set of endpoints to retrieve and cross-reference gospel resources. Each endpoint returns JSON-formatted data, making it easy to consume in front-end or mobile applications.

### Example Endpoints

- Get Scripture Passage

```
GET /api/v1/scripture?book=John&chapter=3&verse=16
```

Retrieves a specific scripture passage with metadata.

- Search Scriptures

```
GET /api/v1/search?query=faith
```

Searches for scriptures matching a given query term.

- Get Cross-References

```
GET /api/v1/cross-references?book=John&chapter=3&verse=16
```

Returns related passages and references for a specific verse.

#### API Response Format

Each endpoint will return a JSON response structured as follows:

```
{
  "status": "success",
  "data": { /* ... relevant data ... */ }
}
```

In case of an error:

```
{
  "status": "error",
  "message": "Error details here"
}
```

## Data Sources

The API scrapes and processes data from public gospel resources. The following resources are supported:

- Latter-day Saint Scriptures (Bible, Book of Mormon, Doctrine and Covenants, Pearl of Great Price)
- General Conference Talks
- Apocryphal Texts
- Hebrew and Greek Cross-References

## Development

### Testing

Run tests to verify functionality:

```
cargo test
```

### Linting

Lint your code to maintain quality:

```
cargo fmt -- --check
cargo clippy
```

## Contribution

We welcome contributions! Please feel free to submit pull requests to improve the API or add new features.

1. Fork the repository.
2. Create a new branch.
3. Make your changes.
4. Submit a pull request.

## License

This project is licensed under the Apache 2.0 License. See the LICENSE file for details.