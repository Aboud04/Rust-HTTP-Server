# Simple Rust HTTP Server

This repository contains a minimal, single-threaded HTTP server written in Rust. It is designed for educational purposes and demonstrates the basics of handling HTTP requests using the Rust standard library.

## Features

- Single-threaded HTTP server
- Handles basic GET requests
- Minimal and readable code
- No external dependencies beyond the Rust standard library
- Serves static HTML, CSS, and other files
- Educational foundation for understanding HTTP and TCP in Rust

## Getting Started

### Prerequisites

- Rust and Cargo installed  
  [Install Rust](https://www.rust-lang.org/tools/install)

### Build and Run

1. Clone the repository:
   ```bash
   git clone https://github.com/Aboud04/Rust-HTTP-Server.git
   cd into the repo
   ```

2. Build the project:
   ```bash
   cargo build --release
   ```

3. Run the server:
   ```bash
   cargo run
   ```

4. Test the server:
   By default, the server will start on `127.0.0.1:8080`. You can test it using a browser or curl:
   ```bash
   curl http://127.0.0.1:8080
   ```

## Project Structure

```
simple-rust-http-server/
├── src/
│   ├── main.rs       # Main server logic
│   └── rest*         # rest of the server
├── public/
│   ├── index.html       # Default HTML page
│   └── style.css        # CSS styling
├── Cargo.toml           # Project configuration
└── README.md            # This file
```

## How It Works

The server listens on a TCP socket and handles incoming connections sequentially. Each request is read, parsed minimally, and responded to with appropriate HTTP responses. This simple structure makes it easy to understand the fundamentals of HTTP and TCP programming in Rust.

Key concepts demonstrated:
- TCP socket binding and listening
- HTTP request parsing
- HTTP response formatting
- File serving
- Error handling in network programming


## Configuration

You can modify the server configuration in `src/main.rs`:

- **Port**: Change `127.0.0.1:8080` to your desired address

## Educational Value

This project is perfect for learning:
- Rust networking with `std::net`
- HTTP protocol fundamentals
- TCP socket programming
- File I/O operations in Rust
- Error handling patterns
- Basic web server architecture

## Limitations

As an educational project, this server has intentional limitations:
- Single-threaded (handles one request at a time)
- Minimal HTTP parsing
- No middleware or advanced routing
- No security features (authentication, HTTPS, etc.)

For production use, consider frameworks like [Axum](https://github.com/tokio-rs/axum), [Warp](https://github.com/seanmonstar/warp), or [Actix-web](https://github.com/actix/actix-web).

## Next Steps

To extend this server, consider implementing:
- Multi-threading with `std::thread`
- Async I/O with `tokio`
- JSON API endpoints
- Template rendering
- Database integration
- Request logging
- Configuration files

## Contributing

Contributions are welcome! Feel free to:
- Submit bug reports or feature requests
- Improve documentation
- Add example routes or features
- Enhance error handling

Please keep in mind that this server is intentionally minimal and educational.

## License

This project is open-source and available under the MIT License.


Happy coding! 🦀
