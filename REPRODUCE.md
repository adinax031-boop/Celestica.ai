# Run and verify Convergence

## Exhibition with no internet

Open the downloaded `index.html` with a current Chrome, Edge or Firefox. The offline file starts all three labs, including real browser neural training and orbit calculations. KC's recorded and simulation modes need no model. Export the experiment ledger from the Evidence section. Browser storage behavior varies when the page is opened from a file.

## Rebuild or rerun evidence

Node 22 or newer is recommended. Install the local development dependencies (`npm install`), then run:

```sh
npm run build
npm test
npm run benchmark
```

Re-running the benchmark refreshes timing measurements. Training and inference resource counts are tracked separately. `npm run build` rebundles the data and JavaScript into a self-contained HTML file. `npm test` exercises the algorithms and the packaged application's offline DOM flows.

## Optional Linux live mode

Install Rust 1.85.1 with `wasm32-wasip1` in a single prefix, Python, bubblewrap with user namespaces, prlimit and libseccomp. Install `wasmtime==30.0.0` and `pint==0.25.2`. Set `CELESTICA_RUST_ROOT` to the Rust prefix. For genuine live KC and Axiom AI proposals, download the pinned [Qwen2.5-Coder-0.5B-Instruct Q4_K_M GGUF](https://huggingface.co/Qwen/Qwen2.5-Coder-0.5B-Instruct-GGUF/resolve/ebb2015119c907b064c512bf053e945850b5875f/qwen2.5-coder-0.5b-instruct-q4_k_m.gguf). SHA-256 is `1d9614638d18024d0fbb36575a15f1302a3adf044df10345688ec4f6e1c4ff32`.

```sh
llama-server -m qwen2.5-coder-0.5b-instruct-q4_k_m.gguf --host 127.0.0.1 --port 9160 -t 4 -np 1 -c 4096 -ngl 0
```

In a separate terminal in this directory:

```sh
export CELESTICA_RUST_ROOT=/absolute/path/to/rust-prefix
python serve.py --port 8040 --model-url http://127.0.0.1:9160
```

Open http://127.0.0.1:8040. The model and dependency downloads are preparation steps. No live requests leave the machine. Run `python serve.py` without the model URL for the browser physics lab plus AxiomForge unit-check service. The server binds loopback and accepts only curated KC tasks. The independent Rust verifier and Axiom physics checks can reject outputs. Do not expose the local server as a public service.
