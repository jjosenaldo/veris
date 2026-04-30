# VeRIS

VeRIS (*Verifier of Railway Interlocking Systems*) is a tool that allows you to automatically verify, using CSP (Communicating Sequential Processes) and the FDR4 model checker, safety properties about relay-based circuits modeled with Clearsy's diagram editor. It was developed as the artifact of the undergraduate thesis available at [https://repositorio.ufrn.br/items/741db2cc-223d-4deb-b7fd-58bb659e535b](https://repositorio.ufrn.br/items/741db2cc-223d-4deb-b7fd-58bb659e535b).

## Usage

VeRIS is currently only supported on **Windows**.

You can download portable versions of VeRIS from the [Releases](https://github.com/jjosenaldo/veris/releases) tab. Since it is portable software, you don't need to install anything other than FDR4. These releases come with example projects modeled in the Clearsy's diagram editor that you can use to test the tool.

### Prerequisites

VeRIS requires [FDR4](https://cocotec.io/fdr/) to run.

**Important:** Before running VeRIS for the first time, you must open FDR4 and accept its license agreement. If you do not accept the license in FDR4, VeRIS will eventually crash when trying to verify properties.

## Building

VeRIS can only be built on **Windows**.

### Prerequisites

You need [FDR4](https://cocotec.io/fdr/) installed on your machine to build the project. The build configuration expects the FDR4 library to be located at a specific path. Ensure that FDR4 is installed and its JAR file is at:

`C:\Program Files\FDR\bin\fdr.jar`

If your installation path is different, you will need to update the `dependencies` block in the `build.gradle.kts` file to point to the correct location of `fdr.jar`.

Once FDR4 is set up, you can build the project using standard Gradle commands (e.g., `./gradlew build` or `./gradlew packageDistributionForCurrentOS`).
