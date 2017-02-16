# rust-webplatform

A Rust library for use with emscripten to access the DOM. Fork of (http://github.com/tcr/rust-webplatform)



```rust
extern crate rdom;
use rdom::*;

fn main() {
    let doc = init_gui();
    doc.get_elem("body").load("<h1>HELLO FROM RUST</h1> <button id='btHello'>CLICK ME</button>")
    Button::from(doc.get_elem("#btHello")).on_click(|_| alert("Hello from Rust"));    
}
```

Used with `cargo build --target=asmjs-unknown-emscripten`.

## License

MIT or Apache-2.0, at your option.
