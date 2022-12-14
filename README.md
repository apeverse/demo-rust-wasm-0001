# demo-rust-wasm-0001


https://www.graalvm.org/22.2/docs/introduction/

- qemu 
- kvm
- graalvm

## vm

https://wiki.nikiv.dev/web/webassembly

- wasmtime
- wasmer
- wasm3
- wavm
- wasmi

wasmer 官方给出的 wasmer 与 wasmtime 的对比

https://wasmer.io/wasmer-vs-wasmtime

各种各样的 wasm runtime 列表

https://github.com/appcypher/awesome-wasm-runtimes

https://wapm.io/saghul/quickjs

https://github.com/wasmerio/wasmer/tree/master/examples

https://webassembly.sh

https://docs.rs/wasmer/latest/wasmer

https://medium.com/wasmer/introducing-wax-a-webassembly-package-runner-d69943209d58

https://docs.wasmer.io/

https://wasmer.io/posts

https://wapm.io/vshymanskyy/wasm3

https://blog.logrocket.com/webassembly-runtimes-compared/

https://blog.logrocket.com/modern-browser-apis-to-use-today/

![image](https://user-images.githubusercontent.com/32976079/185843637-40737ef6-0e8d-4648-be08-924723890d93.png)



## part 0

https://rustwasm.github.io/docs

https://rustwasm.github.io/docs/book

https://rustwasm.github.io/wasm-pack/book/introduction.html

https://rustwasm.github.io/docs/wasm-bindgen/introduction.html

https://github.com/rustwasm

https://github.com/rustwasm/wasm-bindgen

https://github.com/rustwasm/wasm-pack

https://github.com/rustwasm/wasm-pack-template

https://rustwasm.github.io/wasm-pack

https://webpack.js.org/concepts

> wasm-pack seeks to be a one-stop shop for building and working with rust-generated WebAssembly that you would like to interop with JavaScript, in the browser or with Node.js. 

> wasm-pack helps you build rust-generated WebAssembly packages that you could publish to the npm registry, or otherwise use alongside any javascript packages in workflows that you already use, such as webpack.

> wasm-bindgen is a Rust library and CLI tool that facilitate high-level interactions between wasm modules and JavaScript. 

> In rust, tools like wasm-bindgen, which is part of wasm-pack workflow, abstracts away linear memory, and allows using native data structures between rust and Javascript. https://wasmbyexample.dev/examples/webassembly-linear-memory/webassembly-linear-memory.rust.en-us.html


## wasm gas metering

https://github.com/paritytech/wasm-instrument

https://github.com/paritytech/wasm-utils

https://openethereum.github.io/WebAssembly-GasMetering

https://openethereum.github.io/WebAssembly-Links

https://github.com/ewasm/wasm-metering

https://github.com/ewasm/wasm-metering

## binaryen & emscripten

https://github.com/WebAssembly/binaryen

https://github.com/emscripten-core/emscripten

> Binaryen is a compiler and toolchain infrastructure library for WebAssembly, written in C++. It aims to make compiling to WebAssembly easy, fast, and effective.

> Emscripten compiles C and C++ to WebAssembly using LLVM and Binaryen. Emscripten output can run on the Web, in Node.js, and in wasm runtimes.


## part 1

https://webassembly.org/

https://rustwasm.github.io/wasm-pack

https://rustwasm.github.io/wasm-pack/book

https://github.com/rustwasm/wasm-bindgen/issues/979

https://doc.rust-lang.org/nightly/rustc/platform-support.html

wasm32-unknown-unknown

wasm32 指 cpu类型与寻址空间大小，32 指 32bit 的内存寻址空间，64 指 64bit 的内存寻址空间（目前没有实现）。

第一个 unknown，指对程序进行编译的平台（任意）；第二个 unknown，指运行目标程序的平台（任意）。

https://rustmagazine.github.io/rust_magazine_2021/chapter_7/lark-rust-wasm-sqlite.html

WASM 三种工作模式：emscripten、wasi、无依赖

前两种模式分别需要宿主提供 posix 接口和 wasi 接口功能，最后一种模式完全没有外部依赖

Rust 中分别对应三种编译目标

- wasm32-unknown-emscripten （依赖 posix 接口）
- wasm32-wasi （依赖 wasi 接口）
- wasm32-unknown-unknown （无依赖）

这三种模式，对 C/C++ 代码的友好度：emscripten > wasi >> unknown

Rust 社区的生态基本是围绕着 wasm32-unknown-unknown 和 wasm32-wasi 构建的，如 wasm-bindgen 工具等；

Rust has Emscripten integration, with the wasm32-unknown-emscripten and asmjs-unknown-emscripten targets.

## part 2

https://github.com/second-state/substrate-wasmedge

https://github.com/second-state/wasm-learning

https://www.secondstate.io/articles/webassembly-in-the-browser

https://www.secondstate.io/articles/rust-and-webassembly

https://www.secondstate.io/articles/extend-webassembly

https://www.secondstate.io/articles/ebpf-and-webassembly-whose-vm-reigns-supreme

此文对 ebpf 和 wasm 两个 vm 进行了简单对比


## part 3

https://github.com/WebAssembly/wabt

https://webassembly.github.io/spec/core/binary/index.html

https://wasdk.github.io/wasmcodeexplorer/

![image](https://user-images.githubusercontent.com/32976079/186940067-821dc2d8-e615-44a3-a33b-edae602edbf1.png)

![image](https://user-images.githubusercontent.com/32976079/186940526-8ce517fe-b305-434d-93f9-cf438b672125.png)

![image](https://user-images.githubusercontent.com/32976079/187008263-3d2e2d54-0d93-4d1f-abf2-e48f6c7d78a8.png)

![image](https://user-images.githubusercontent.com/32976079/187008373-d60efb77-f457-49bd-a702-0e5d6b3535ea.png)

https://segmentfault.com/a/1190000040737725/en

https://hacks.mozilla.org/2018/01/making-webassembly-even-faster-firefoxs-new-streaming-and-tiering-compiler/

https://rsms.me/wasm-intro

https://developer.mozilla.org/en-US/docs/WebAssembly

https://webassembly.github.io/spec/




## 其他

https://wasm.fastlylabs.com/docs/rust/http_guest/kvstore/struct.KVStore.html

https://www.fastly.com/blog/edge-programming-rust-web-assembly




