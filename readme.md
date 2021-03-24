# Rust + GKT mwe

This is a minimal working example for creating a graphical user interface with Rust and GKT.

The entire installation and mwe creation process is documented below. But if you want to clone and test this yourself, you only need to follow steps 1 and 4 below.

## 1) Install Rust:

* See: https://www.rust-lang.org/tools/install

## 2) Initiate Cargo Project

Cargo is a package manager for Rust.

Reference: https://doc.rust-lang.org/book/ch01-03-hello-cargo.html

Create a new project:

```

cargo new project_name

```

## 3) Add GTK Dependencies to Cargo Package Manager

If you are familiar with Node.js, Cargo is the equivalent for Rust. At least that's what I've gathered at the time of writing.

Requires glib before build: `sudo apt-get install libgtk-3-dev`

And add the following package declarations under 'dependencies' in your `cargo.toml` file.

```
[dependencies.gtk]
version = "0.9.0"
features = ["v3_16"]

[dependencies.gio]
version = ""
features = ["v2_44"]
```

Reference: https://gtk-rs.org/

## 4) Build and Test

To test the application, from this projects directory run the following commands in terminal: 

```
cargo build
# test application
./target/debug/project_name
```

