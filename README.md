# True Dual-Port RAM Verification Environment using UVM (Universal Verification Methodology)

A comprehensive, modular UVM-based verification environment built to verify a True Dual-Port RAM design, ensuring data integrity across simultaneous read and write operations.

## 🚀 Verification Architecture & Components
* **Test (`ram_test.sv`)**: Configures and initiates the test sequences.
* **Environment (`ram_env.sv`)**: Houses the verification components (Agents, Scoreboard).
* **Agents (Write & Read Agents)**: Contains drivers (`ram_wdrv.sv`, `ram_rdrv.sv`), monitors (`ram_wmon.sv`, `ram_rmon.sv`), sequencers, and sequences (`ram_wseqs.sv`, `ram_rseqs.sv`) for handling independent transactions.
* **Scoreboard (`ram_sb.sv`)**: Automatically checks output data against expected results to verify correctness.
* **Interface (`ram_if.sv`)**: Defines clocking blocks and modports for clean signal interaction with the DUT.

## 📂 Project Structure
```text
├── design.sv          # True Dual-Port RAM RTL Design
├── ram_if.sv          # UVM Interface with clocking blocks
├── testbench.sv       # Top-level module instantiating DUT and interface
├── ram_test.sv        # UVM Test component
├── ram_env.sv         # UVM Environment
├── ram_wdrv.sv        # Write Driver
├── ram_rdrv.sv        # Read Driver
├── ram_wmon.sv        # Write Monitor
├── ram_rmon.sv        # Read Monitor
├── ram_sb.sv          # Scoreboard
└── README.md          # Project documentation

🛠️ Key Verification Features
Independent stimulus generation for Write and Read ports.

Automated scoreboarding for transaction-level self-checking.

Modular UVM component hierarchy ensuring reusability and scalability.
