# JSON Structure Parser & Analytics Engine 📑

A low-latency data structure validator and hierarchical tokenization engine built in native JavaScript. This repository demonstrates optimized abstract syntax tree (AST) simulation, real-time object graph parsing, and deterministic syntax error isolation with zero processing lag.

## 🗂️ Architectural Overview

The analytics engine operates as an isolated syntax compiler, capturing raw JSON input streams, executing dynamic string validation, and tracking structural nesting levels through a modular token-matching pipeline.

### ⚙️ Core Technical Features:
* **Real-Time Tokenization:** Parses and expands object keys and data types instantly via synchronized execution loops.
* **Syntax Exception Isolation:** pinpoints formatting anomalies and trailing token bugs to protect the calculation stack.
* **Zero External Dependencies:** Built strictly with vanilla JavaScript, CSS, and HTML for direct hardware thread alignment.

## 🚀 Deployment Instructions

To run the JSON parser engine locally or host it on any web environment:
1. Clone this repository to your local storage.
2. Ensure `index.html`, `style.css`, and `script.js` are in the same directory.
3. Open `index.html` in any standard modern web browser (Chrome, Brave, Edge).

*Developed for structured data serialization analysis and core parsing logic prototyping.*

```mermaid
graph TD
    %% Estilo de nodos neón
    classDef safe color:#00ff66,fill:#000,stroke:#00ff66,stroke-width:2px;
    classDef alert color:#ff0033,fill:#000,stroke:#ff0033,stroke-width:2px;
    classDef process color:#00ffff,fill:#000,stroke:#00ffff,stroke-width:1px;

    Start([⚡ Parser Engine Init]) --> Load[🚀 DOM Input Area Rendered]
    Load --> Active[📡 Attached Real-Time Input Event Listeners]
    
    Active --> Wait{⌨️ Waiting for JSON Payload Ingestion}
    
    Wait -- NO --> Wait
    Wait -- SÍ --> Capture[📥 Capture Raw Text Stream Buffer]
    
    Capture --> Check{🔬 Execute Algorithmic Try-Catch Parse}
    
    Check -- Malformed JSON / Syntax Error --> Err[🚨 Trigger Structural Exception Log]:::alert
    Check -- Valid Syntax Structure --> Success[⚙️ Map Hierarchical Data Object Graph]:::process
    
    Err --> Output[🖥️ Flush Parser Status and Error Line to UI]
    Success --> Graph[🔄 Render Dynamic Nested DOM Tree Nodes]:::process
    
    Graph --> Output
    Output --> Return[🔄 Re-arm Listeners & Clear Volatile Token Arrays]
    Return --> Wait

    class Start,Load,Active,Wait safe;
    class Capture,Check,Success,Graph,Output,Return process;
```
