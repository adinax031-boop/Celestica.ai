# Celestica AI

A student research project on verifying AI-generated Rust. Choose an exhibit case, inspect the compiler’s judgment, then run a separate check of the program’s behavior. A simple refill function provides the classroom example.

## Open the exhibit

Download `index.html` and open it in a browser. Select **Exhibition** and choose **Recorded experiment** or **Offline simulation**. The recorded mode uses historical model outputs. The simulation compares deterministic rules. The optional live service runs on a prepared Linux computer and executes only the six curated exhibit specifications.

- [Exhibit HTML](index.html)
- [Source and reproduction guide](Celestica_Verify_Source.zip)
- [Machine-readable result summary](results.json)

## Results

| Historical condition | Functional passes | Compiled | Repair | Generation |
| --- | ---: | ---: | ---: | ---: |
| Original Qwen3.5-4B | 12/30 | 18/30 | 3/9 | 9/21 |
| Step-48 Rust adapter | 6/30 | 12/30 | 4/9 | 2/21 |
| Compiler-gated specialist route | 16/30 | 23/30 | 6/9 | 10/21 |
| One compiler edit | 13/30 | 20/30 | 4/9 | 9/21 |

The retrospective route gained four and lost zero against one-shot base. It used 42 versus 30 model calls and 317.20 versus 231.58 seconds of model generation. Its exact paired p-value is 0.125, descriptive on reused development data. The original model remains the incumbent.

A separate frozen study of 60 publisher-provided buggy Rust bodies found that 59 compiled and zero passed functional checks. One bounded compiler edit recovered zero cases. This cohort contained no model-generated inputs. A full matched fresh LLM result, a new adapter and a promotion claim remain open.

Additional paid model, API and cloud expenditure was ₹0. Existing equipment, subscriptions, power, internet and any printing are separate. The project measured no environmental savings.

## Attribution

The project used Qwen3.5-4B, LoRA/QLoRA, Rust, Wasmtime and the MIT-licensed HumanEvalPack and MultiPL-E benchmark families. Benchmark notices and pinned references are inside the source archive. Codex assisted with implementation, research analysis, example drafting and presentation materials. This repository provides project evidence and code for inspection. The authors of upstream materials retain their original rights.
