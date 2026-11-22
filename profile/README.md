<p align="right"><a href="README.es.md">Español</a></p>

<p align="center"><img src="../assets/banner-en.png" alt="Kmila" width="100%"></p>

<p align="center">
  <a href="https://kmila.com.mx/demo"><b>Try the browser demo</b></a> · <a href="https://kmila.com.mx">Website</a> · <a href="https://github.com/Kmila9s/Documentation/releases">User manual (PDF) and thesis</a>
</p>

**Kmila** is an open-source lab to learn and debug hardware description languages without an FPGA: write VHDL, simulate it, and see waveforms, the synthesized schematic, step-by-step replay and an interactive board, plus lessons and auto-graded practice. Its simulator is checked case by case against GHDL.

<table><tr><td align="center"><img src="../assets/shots/kmila.png" width="100%" alt=""><br><sub>Editor and waveforms</sub></td><td align="center"><img src="../assets/shots/librarycompiler.png" width="100%" alt=""><br><sub>Synthesized schematic</sub></td></tr><tr><td align="center"><img src="../assets/shots/interpreter.png" width="100%" alt=""><br><sub>Concept lessons</sub></td><td align="center"><img src="../assets/shots/practicevalidator.png" width="100%" alt=""><br><sub>Auto-graded practice</sub></td></tr></table>

### Repositories

| | | |
|---|---|---|
| <img src="../assets/icons/kmila.png" width="36" alt=""> | [**Kmila**](https://github.com/Kmila9s/Kmila) | Write, simulate and debug HDL without an FPGA |
| <img src="../assets/icons/parser.png" width="36" alt=""> | [**Parser**](https://github.com/Kmila9s/Parser) | VHDL lexer and front-door parsing for Kmila |
| <img src="../assets/icons/interpreter.png" width="36" alt=""> | [**Interpreter**](https://github.com/Kmila9s/Interpreter) | Delta-cycle HDL simulation engine and synthesis |
| <img src="../assets/icons/debugger.png" width="36" alt=""> | [**Debugger**](https://github.com/Kmila9s/Debugger) | Structural checks and lint for VHDL designs |
| <img src="../assets/icons/librarycompiler.png" width="36" alt=""> | [**LibraryCompiler**](https://github.com/Kmila9s/LibraryCompiler) | IEEE libraries, use clauses and primitive lowering |
| <img src="../assets/icons/timemachine.png" width="36" alt=""> | [**TimeMachine**](https://github.com/Kmila9s/TimeMachine) | Discrete time base: ticks, clocks and events |
| <img src="../assets/icons/practicevalidator.png" width="36" alt=""> | [**PracticeValidator**](https://github.com/Kmila9s/PracticeValidator) | Validates every practice against GHDL |
| <img src="../assets/icons/simulatorbench.png" width="36" alt=""> | [**SimulatorBench**](https://github.com/Kmila9s/SimulatorBench) | Kmila vs GHDL accuracy bench |
| <img src="../assets/icons/tests.png" width="36" alt=""> | [**Tests**](https://github.com/Kmila9s/Tests) | Unit, end-to-end and performance suites |
| <img src="../assets/icons/documentation.png" width="36" alt=""> | [**Documentation**](https://github.com/Kmila9s/Documentation/releases) | Thesis and user manual (PDF) |

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
