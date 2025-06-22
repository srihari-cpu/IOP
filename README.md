# IOP – C Infrastructure & Java Front‑End for IOP System 🚀

A complete tooling suite for SRI‑CSL’s **IOP** framework:  
• Core C libraries and command‑line tools (`iop`)  
• Java‑based launchers (`jlambda`) and GUI (powered by `iop.jar`)

---

## 📦 Table of Contents

1. [About](#about)  
2. [Features](#features)  
3. [Requirements](#requirements)  
4. [Installation](#installation)  
5. [Usage](#usage)  
   - [C Tools (iop)](#c-tools-iop)  
   - [Java Launcher (jlambda)](#java-launcher-jlambda)  
6. [Documentation](#documentation)  
7. [Examples](#examples)  
8. [Building from Source](#building-from-source)  
9. [Tests](#tests)  
10. [Roadmap](#roadmap)  
11. [Contributing](#contributing)  
12. [License](#license)  
13. [Authors & Acknowledgments](#authors--acknowledgments)

---

## ABOUT

IOP (Input/Output Protocol) enables structured communication and orchestration in the Pathway Logic ecosystem. This repo provides the low‑level C code and Java integration layer for tool bundling.

---

## FEATURES

- 🔧 **C Core**: High-performance core instruments, actor messaging, protocol handling.  
- 🛠 **CLI Tools**:  
  - `iop`: command‑line protocol inspector/runner  
  - `jlambda`: JVM‑based launcher for advanced workflows  
- 🖥 **GUI Support**: Prebuilt `iop.jar` includes a Java‑Swing UI front‑end  
- 📚 **Docs**: Full Javadoc and user manuals in `doc/`

---

## REQUIREMENTS

- **C Development**: gcc/clang, make, GNU make  
- **Java** (minimum JRE/JDK 8) — required for `jlambda` and GUI  
- **Optional**: coverity or Travis CI scripts may require Perl, etc.

---

## INSTALLATION

```bash
git clone https://github.com/SRI-CSL/iopc.git
cd iopc
export IOPBINDIR=/usr/local/bin
make
sudo make install
USAGE
C Tools (iop)
bash
Copy
Edit
iop --help
# Common commands: inspect, run, debug, version
Java Launcher (jlambda)
bash
Copy
Edit
export PATH=$IOPBINDIR:$PATH
jlambda --help
# To run GUI:
iop-gui
DOCUMENTATION
Javadoc (for iop.jar): see doc/javadoc/

User Manuals:

doc/jlambda_manual.md

doc/iop_manual.md

EXAMPLES
Check scripts/ and lib/ for sample workflows. Typical usage:

bash
Copy
Edit
# Simple CLI run
iop --config examples/sample.cfg

# Java front‑end
jlambda examples/sample.json
BUILDING FROM SOURCE
bash
Copy
Edit
make clean
make
# For verbose build:
make V=1
TESTS
(If test suite exists; otherwise omit or note future addition.)

bash
Copy
Edit
make test
ROADMAP
 Add integration tests

 Expand protocol support (e.g. TLS, JSON-based protocols)

 Modernize GUI (JavaFX or web front‑end)

CONTRIBUTING
Contributions are welcome! Please:

Fork the repo

Create a feature branch (git checkout -b feature-x)

Commit changes with clear messages

Submit a PR

Refer to [CONTRIBUTING.md] for guidelines.

LICENSE
This project is licensed under the GPL‑2.0. See LICENSE for details.

AUTHORS & ACKNOWLEDGMENTS
SRI‑CSL: original authors and guardians of the IOP system

This open‑source port maintained by the IOP community
