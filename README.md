# demo-rust-wasm-0001

https://rustwasm.github.io/wasm-pack

https://rustwasm.github.io/wasm-pack/book

https://github.com/rustwasm/wasm-bindgen/issues/979

https://doc.rust-lang.org/nightly/rustc/platform-support.html

wasm32-unknown-unknown

wasm32 指 cpu类型与寻址空间大小，32 指 32bit 的内存寻址空间，64 指 64bit 的内存寻址空间（目前没有实现）。

第一个 unknown，指对程序进行编译的平台（任意）；第二个 unknown，指运行目标程序的平台（任意）。

https://rustmagazine.github.io/rust_magazine_2021/chapter_7/lark-rust-wasm-sqlite.html

目前 WASM 实际有三种工作模式：Emscripten 模式、WASI 模式、无任何依赖的纯粹模式，

前两种模式分别需要宿主提供 posix 接口和 wasi 接口功能，最后一种模式完全没有外部依赖

在Rust语言中，分别对应三种编译目标

- wasm32-unknown-emscripten （依赖 posix 接口）
- wasm32-wasi （依赖 wasi 接口）
- wasm32-unknown-unknown （无依赖）

这三种模式，对C/C++代码的友好度：Emscripten > Wasi >> Unknown

rust 社区的生态基本是围绕着 wasm32-unknown-unknown 和 wasm32-wasi 构建的，如 wasm-bindgen 工具等；

不过考虑到unknown环境对外部依赖少，所以 sdk 中的 rust 代码我们就先确定了，优先使用 wasm32-unknown-unknown 模式，wasm32-wasi 模式次之。

而对于 sqlite 部分，我们则将三种 wasm 工作模式都尝试了


