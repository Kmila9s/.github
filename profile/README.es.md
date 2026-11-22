<p align="right"><a href="https://github.com/Kmila9s/.github/blob/main/profile/README.md">English</a></p>

<p align="center"><picture>
  <source media="(prefers-color-scheme: dark)" srcset="https://github.com/Kmila9s/.github/raw/main/assets/banner-es-dark.svg">
  <source media="(prefers-color-scheme: light)" srcset="https://github.com/Kmila9s/.github/raw/main/assets/banner-es-light.svg">
  <img src="https://github.com/Kmila9s/.github/raw/main/assets/banner-es-dark.svg" alt="Kmila — Escribe, simula y depura HDL sin FPGA" width="100%">
</picture></p>

<p align="center"><img src="https://img.shields.io/badge/banco%20GHDL-149%20casos-3c82f6?style=flat-square" alt="banco GHDL: 149 casos"> <img src="https://img.shields.io/badge/pr%C3%A1cticas-135%20autocalificadas-3c82f6?style=flat-square" alt="prácticas: 135 autocalificadas"> <img src="https://img.shields.io/badge/interfaz-7%20idiomas-3c82f6?style=flat-square" alt="interfaz: 7 idiomas"> <img src="https://img.shields.io/badge/licencia-MIT-3c82f6?style=flat-square" alt="licencia: MIT">
  <a href="https://github.com/Kmila9s/Kmila/releases/latest"><img src="https://img.shields.io/github/v/release/Kmila9s/Kmila?style=flat-square&color=475569&label=release" alt="release"></a></p>

**Kmila** es un laboratorio libre para aprender y depurar lenguajes de descripción de hardware sin FPGA: escribe VHDL, simúlalo y mira formas de onda, el esquemático sintetizado, la repetición paso a paso y un tablero interactivo, además de lecciones y prácticas autocalificadas. Su simulador se compara caso por caso contra GHDL.

<h3 align="center">Empieza aquí</h3>
<p align="center"><a href="https://kmila.com.mx/demo"><img src="https://img.shields.io/badge/Prueba%20la%20demo-3c82f6?style=for-the-badge" alt="Prueba la demo"></a>&nbsp;<a href="https://github.com/Kmila9s/Kmila/releases/latest"><img src="https://img.shields.io/badge/Descargar-475569?style=for-the-badge" alt="Descargar"></a>&nbsp;<a href="https://github.com/Kmila9s/Documentation/releases"><img src="https://img.shields.io/badge/Manual%20de%20usuario-475569?style=for-the-badge" alt="Manual de usuario"></a></p>

<table><tr><td align="center"><img src="https://github.com/Kmila9s/.github/raw/main/assets/shots/kmila.png" width="100%" alt=""><br><sub>Editor y formas de onda</sub></td><td align="center"><img src="https://github.com/Kmila9s/.github/raw/main/assets/shots/librarycompiler.png" width="100%" alt=""><br><sub>Esquemático sintetizado</sub></td></tr><tr><td align="center"><img src="https://github.com/Kmila9s/.github/raw/main/assets/shots/interpreter.png" width="100%" alt=""><br><sub>Lecciones de conceptos</sub></td><td align="center"><img src="https://github.com/Kmila9s/.github/raw/main/assets/shots/practicevalidator.png" width="100%" alt=""><br><sub>Prácticas autocalificadas</sub></td></tr></table>

### Repositorios

| | | |
|---|---|---|
| <img src="https://github.com/Kmila9s/.github/raw/main/assets/icons/kmila.png" width="36" alt=""> | [**Kmila**](https://github.com/Kmila9s/Kmila) | Escribe, simula y depura HDL sin FPGA |
| <img src="https://github.com/Kmila9s/.github/raw/main/assets/icons/parser.png" width="36" alt=""> | [**Parser**](https://github.com/Kmila9s/Parser) | Analizador léxico y sintáctico de VHDL para Kmila |
| <img src="https://github.com/Kmila9s/.github/raw/main/assets/icons/interpreter.png" width="36" alt=""> | [**Interpreter**](https://github.com/Kmila9s/Interpreter) | Motor de simulación por ciclos delta y síntesis |
| <img src="https://github.com/Kmila9s/.github/raw/main/assets/icons/debugger.png" width="36" alt=""> | [**Debugger**](https://github.com/Kmila9s/Debugger) | Validación estructural y lint de diseños VHDL |
| <img src="https://github.com/Kmila9s/.github/raw/main/assets/icons/librarycompiler.png" width="36" alt=""> | [**LibraryCompiler**](https://github.com/Kmila9s/LibraryCompiler) | Librerías IEEE, cláusulas use y primitivas |
| <img src="https://github.com/Kmila9s/.github/raw/main/assets/icons/timemachine.png" width="36" alt=""> | [**TimeMachine**](https://github.com/Kmila9s/TimeMachine) | Base de tiempo discreta: ticks, relojes y eventos |
| <img src="https://github.com/Kmila9s/.github/raw/main/assets/icons/practicevalidator.png" width="36" alt=""> | [**PracticeValidator**](https://github.com/Kmila9s/PracticeValidator) | Valida cada práctica contra GHDL |
| <img src="https://github.com/Kmila9s/.github/raw/main/assets/icons/simulatorbench.png" width="36" alt=""> | [**SimulatorBench**](https://github.com/Kmila9s/SimulatorBench) | Banco de exactitud Kmila contra GHDL |
| <img src="https://github.com/Kmila9s/.github/raw/main/assets/icons/tests.png" width="36" alt=""> | [**Tests**](https://github.com/Kmila9s/Tests) | Pruebas unitarias, de extremo a extremo y de rendimiento |
| <img src="https://github.com/Kmila9s/.github/raw/main/assets/icons/documentation.png" width="36" alt=""> | [**Documentation**](https://github.com/Kmila9s/Documentation/releases) | Tesis y manual de usuario (PDF) |

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
