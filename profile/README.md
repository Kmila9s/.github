<p align="right"><a href="https://github.com/Kmila9s/.github/blob/main/profile/README.es.md">Español</a></p>

<p align="center"><picture>
  <source media="(prefers-color-scheme: dark)" srcset="https://github.com/Kmila9s/.github/raw/main/assets/banner-en-dark.svg">
  <source media="(prefers-color-scheme: light)" srcset="https://github.com/Kmila9s/.github/raw/main/assets/banner-en-light.svg">
  <img src="https://github.com/Kmila9s/.github/raw/main/assets/banner-en-dark.svg" alt="Kmila — Write, simulate and debug HDL without an FPGA" width="100%">
</picture></p>

<p align="center"><img src="https://img.shields.io/badge/GHDL%20bench-149%20cases-3c82f6?style=flat-square" alt="GHDL bench: 149 cases"> <img src="https://img.shields.io/badge/practice-135%20auto--graded-3c82f6?style=flat-square" alt="practice: 135 auto-graded"> <img src="https://img.shields.io/badge/UI-7%20languages-3c82f6?style=flat-square" alt="UI: 7 languages"> <img src="https://img.shields.io/badge/license-MIT-3c82f6?style=flat-square" alt="license: MIT">
  <a href="https://github.com/Kmila9s/Kmila/releases/latest"><img src="https://img.shields.io/github/v/release/Kmila9s/Kmila?style=flat-square&color=475569&label=release" alt="release"></a></p>

**Kmila** is an open-source lab to learn and debug hardware description languages without an FPGA: write VHDL, simulate it, and see waveforms, the synthesized schematic, step-by-step replay and an interactive board, plus lessons and auto-graded practice. Its simulator is checked case by case against GHDL.

<h3 align="center">Start here</h3>
<p align="center"><a href="https://kmila.com.mx/demo"><img src="https://img.shields.io/badge/Try%20the%20demo-3c82f6?style=for-the-badge" alt="Try the demo"></a>&nbsp;<a href="https://github.com/Kmila9s/Kmila/releases/latest"><img src="https://img.shields.io/badge/Download-475569?style=for-the-badge" alt="Download"></a>&nbsp;<a href="https://github.com/Kmila9s/Documentation/releases"><img src="https://img.shields.io/badge/User%20manual-475569?style=for-the-badge" alt="User manual"></a></p>

<table><tr><td align="center"><img src="https://github.com/Kmila9s/.github/raw/main/assets/shots/kmila.png" width="100%" alt=""><br><sub>Editor and waveforms</sub></td><td align="center"><img src="https://github.com/Kmila9s/.github/raw/main/assets/shots/librarycompiler.png" width="100%" alt=""><br><sub>Synthesized schematic</sub></td></tr><tr><td align="center"><img src="https://github.com/Kmila9s/.github/raw/main/assets/shots/interpreter.png" width="100%" alt=""><br><sub>Concept lessons</sub></td><td align="center"><img src="https://github.com/Kmila9s/.github/raw/main/assets/shots/practicevalidator.png" width="100%" alt=""><br><sub>Auto-graded practice</sub></td></tr></table>

### Repositories

| | | |
|---|---|---|
| <img src="https://github.com/Kmila9s/.github/raw/main/assets/icons/kmila.png" width="36" alt=""> | [**Kmila**](https://github.com/Kmila9s/Kmila) | Write, simulate and debug HDL without an FPGA |
| <img src="https://github.com/Kmila9s/.github/raw/main/assets/icons/parser.png" width="36" alt=""> | [**Parser**](https://github.com/Kmila9s/Parser) | VHDL lexer and front-door parsing for Kmila |
| <img src="https://github.com/Kmila9s/.github/raw/main/assets/icons/interpreter.png" width="36" alt=""> | [**Interpreter**](https://github.com/Kmila9s/Interpreter) | Delta-cycle HDL simulation engine and synthesis |
| <img src="https://github.com/Kmila9s/.github/raw/main/assets/icons/debugger.png" width="36" alt=""> | [**Debugger**](https://github.com/Kmila9s/Debugger) | Structural checks and lint for VHDL designs |
| <img src="https://github.com/Kmila9s/.github/raw/main/assets/icons/librarycompiler.png" width="36" alt=""> | [**LibraryCompiler**](https://github.com/Kmila9s/LibraryCompiler) | IEEE libraries, use clauses and primitive lowering |
| <img src="https://github.com/Kmila9s/.github/raw/main/assets/icons/timemachine.png" width="36" alt=""> | [**TimeMachine**](https://github.com/Kmila9s/TimeMachine) | Discrete time base: ticks, clocks and events |
| <img src="https://github.com/Kmila9s/.github/raw/main/assets/icons/practicevalidator.png" width="36" alt=""> | [**PracticeValidator**](https://github.com/Kmila9s/PracticeValidator) | Validates every practice against GHDL |
| <img src="https://github.com/Kmila9s/.github/raw/main/assets/icons/simulatorbench.png" width="36" alt=""> | [**SimulatorBench**](https://github.com/Kmila9s/SimulatorBench) | Kmila vs GHDL accuracy bench |
| <img src="https://github.com/Kmila9s/.github/raw/main/assets/icons/tests.png" width="36" alt=""> | [**Tests**](https://github.com/Kmila9s/Tests) | Unit, end-to-end and performance suites |
| <img src="https://github.com/Kmila9s/.github/raw/main/assets/icons/documentation.png" width="36" alt=""> | [**Documentation**](https://github.com/Kmila9s/Documentation/releases) | Thesis and user manual (PDF) |

### How it is built

```mermaid
flowchart LR
  kmila["Kmila<br/>app · web · CLI"]
  debugger["Debugger"]
  interpreter["Interpreter"]
  parser["Parser"]
  librarycompiler["LibraryCompiler"]
  timemachine["TimeMachine"]
  practicevalidator["PracticeValidator"]
  simulatorbench["SimulatorBench"]
  tests["Tests"]
  ghdl["GHDL 6<br/>(reference)"]
  kmila-->debugger
  kmila-->interpreter
  kmila-->librarycompiler
  debugger-->interpreter
  interpreter-->parser
  interpreter-->timemachine
  interpreter-->librarycompiler
  librarycompiler-->parser
  practicevalidator-->kmila
  simulatorbench-->kmila
  tests-->kmila
  practicevalidator-.->ghdl
  simulatorbench-.->ghdl
  classDef me fill:#3c82f6,stroke:#1d4ed8,color:#fff
  classDef other fill:#475569,stroke:#334155,color:#fff
  classDef ext fill:#94a3b8,stroke:#64748b,color:#0f172a
  class kmila,debugger,interpreter,parser,librarycompiler,timemachine,practicevalidator,simulatorbench,tests other
  class ghdl ext
  click kmila "https://github.com/Kmila9s/Kmila"
  click debugger "https://github.com/Kmila9s/Debugger"
  click interpreter "https://github.com/Kmila9s/Interpreter"
  click parser "https://github.com/Kmila9s/Parser"
  click librarycompiler "https://github.com/Kmila9s/LibraryCompiler"
  click timemachine "https://github.com/Kmila9s/TimeMachine"
  click practicevalidator "https://github.com/Kmila9s/PracticeValidator"
  click simulatorbench "https://github.com/Kmila9s/SimulatorBench"
  click tests "https://github.com/Kmila9s/Tests"
```

<sub>MIT © 2026 Ulrich Tamayo Daniel.  · Developed as the degree project TT 2026-B059 at IPN ESCOM (Mexico).</sub>
