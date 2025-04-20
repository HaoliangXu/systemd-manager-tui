# Systemd manager tui

![rust](https://img.shields.io/badge/Rust-000000?style=for-the-badge&logo=rust&logoColor=white)

A program for managing systemd services through a TUI (Terminal User Interfaces).

This tool allows you to manage systemd services with ease. You can view logs, list services, view properties, and control their lifecycle—start, stop, restart, enable, and disable—using the D-Bus API.

## Screenshots
![screenshot1](assets/screeshot1.png)
View more [screenshots](docs/screenshots.md)

## Usage

Must be run as sudo (or root).

**It's recommended to build a binary since it's simpler to run with sudo than to configure sudo to run "sudo cargo run".**

### Run in development mode
  ```
   sudo cargo run
  ```

### Build binary

1. Build the binary
    ```
      cargo build --release
    ```
3. Run it ( opcional )
    ```
      sudo target/release/systemd-manager-tui
    ```

## Architecture

See the architecture [here](docs/architecture.md).

## New features and properties

There are many possible actions and pieces of information that can be retrieved, so I’ve implemented the ones I found most relevant. If you’d like more to be added, feel free to open an issue with your request — or consider contributing directly! You can check all available methods and properties on D-Bus [here](https://www.freedesktop.org/software/systemd/man/latest/org.freedesktop.systemd1.html).

## Main libraries

- ratatui - 0.29.0
- zbus - 5.5.0

## Future Improvements

- Monitor CPU and memory usage per service
- Display user-specific systemd services
- Remotely manage services

## Weekly Updates

This project is actively maintained and updated every weekend.  

## Contributing

Contributions are welcome! Please open an issue or submit a pull request for any improvements or bug fixes.

## 📝 License

This project is open-source under the MIT License.
