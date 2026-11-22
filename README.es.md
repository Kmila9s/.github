<p align="right"><a href="README.md">English</a></p>

<p align="center"><img src="assets/banner-es.png" alt="Kmila" width="100%"></p>

<p align="center">
  <a href="https://kmila.com.mx/demo"><b>Prueba la demo en el navegador</b></a> · <a href="https://kmila.com.mx">Sitio web</a> · <a href="https://github.com/Kmila9s/Documentation/releases">Manual de usuario (PDF) y tesis</a>
</p>

**Kmila** es un laboratorio libre para aprender y depurar lenguajes de descripción de hardware sin FPGA: escribe VHDL, simúlalo y mira formas de onda, el esquemático sintetizado, la repetición paso a paso y un tablero interactivo, además de lecciones y prácticas autocalificadas. Su simulador se compara caso por caso contra GHDL.

<table><tr><td align="center"><img src="assets/shots/kmila.png" width="100%" alt=""><br><sub>Editor y formas de onda</sub></td><td align="center"><img src="assets/shots/librarycompiler.png" width="100%" alt=""><br><sub>Esquemático sintetizado</sub></td></tr><tr><td align="center"><img src="assets/shots/interpreter.png" width="100%" alt=""><br><sub>Lecciones de conceptos</sub></td><td align="center"><img src="assets/shots/practicevalidator.png" width="100%" alt=""><br><sub>Prácticas autocalificadas</sub></td></tr></table>

### Repositorios

| | | |
|---|---|---|
| <img src="assets/icons/kmila.png" width="36" alt=""> | [**Kmila**](https://gitlab.lab/kmila-9s/Kmila) | Escribe, simula y depura HDL sin FPGA |
| <img src="assets/icons/parser.png" width="36" alt=""> | [**Parser**](https://gitlab.lab/kmila-9s/Parser) | Analizador léxico y sintáctico de VHDL para Kmila |
| <img src="assets/icons/interpreter.png" width="36" alt=""> | [**Interpreter**](https://gitlab.lab/kmila-9s/Interpreter) | Motor de simulación por ciclos delta y síntesis |
| <img src="assets/icons/debugger.png" width="36" alt=""> | [**Debugger**](https://gitlab.lab/kmila-9s/Debugger) | Validación estructural y lint de diseños VHDL |
| <img src="assets/icons/librarycompiler.png" width="36" alt=""> | [**LibraryCompiler**](https://gitlab.lab/kmila-9s/LibraryCompiler) | Librerías IEEE, cláusulas use y primitivas |
| <img src="assets/icons/timemachine.png" width="36" alt=""> | [**TimeMachine**](https://gitlab.lab/kmila-9s/TimeMachine) | Base de tiempo discreta: ticks, relojes y eventos |
| <img src="assets/icons/practicevalidator.png" width="36" alt=""> | [**PracticeValidator**](https://gitlab.lab/kmila-9s/PracticeValidator) | Valida cada práctica contra GHDL |
| <img src="assets/icons/simulatorbench.png" width="36" alt=""> | [**SimulatorBench**](https://gitlab.lab/kmila-9s/SimulatorBench) | Banco de exactitud Kmila contra GHDL |
| <img src="assets/icons/tests.png" width="36" alt=""> | [**Tests**](https://gitlab.lab/kmila-9s/Tests) | Pruebas unitarias, de extremo a extremo y de rendimiento |
| <img src="assets/icons/documentation.png" width="36" alt=""> | [**Documentation**](https://gitlab.lab/kmila-9s/Documentation) | Tesis y manual de usuario (PDF) |

### Cómo está hecho

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
  ghdl["GHDL 6<br/>(referencia)"]
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

<sub>MIT © 2026 Ulrich Tamayo Daniel.  · Desarrollado como Trabajo Terminal TT 2026-B059 en el IPN ESCOM (México).</sub>
