### DNS Factory – Digital Mock-up of a 5-Line Production Plant
DNS Factory is a fully featured factory simulation built in **Factory I/O** and driven by an **Allen-Bradley Logix Emulate 5580** controller running **Studio 5000 v34**.  
The plant uses **500 + discrete and analogue I/O tags** that are documented, verified, and neatly grouped in the accompanying Excel tag map.

---

#### 📦 Repository contents
| Path | What it is | Why it matters |
|------|------------|----------------|
| `/factory-io/DNS_Factory.factory` | Factory I/O scene | Digital twin of the entire plant—open in Factory I/O and hit **Run** |
| `/plc/DNS_Factory.acd` | Studio 5000 project (v34, Emulate 5580) | Complete ladder-logic & structured-text program |
| `/docs/Production_Factory_TagMap_Clean.xlsx` | **Clean Tag Map** (2 sheets) | *Clean Tag List* → de-duplicated & categorised; *Gaps Summary* → audit of any missing tag numbers |
| `/docs/DNS_Factory_IO-Architecture.pdf` | Block diagram | High-level signal & power layout for rapid onboarding |
| `/hmi/` | ViewSE sample screens | Minimal HMI that mirrors the tag-naming scheme |

---

#### 🛠️ Line layout

| System | Colour used in scene | Core functions |
|--------|---------------------|----------------|
| **Blue System** | Blue | Base & lid assembly + palletising |
| **Green System** | Green | Secondary assembly & palletising |
| **Metal System** | Grey/Metallic | Heavy-duty line with additional guarding |
| **Sorting System** | Yellow (diverters) | Vision-guided diverter gate network |
| **Product Movement System** | Orange | AGV tracks & overhead shuttle interface |

---

#### 💡 Design highlights

* **Intuitive tag naming** – `Prefix` + `Series` + `Index` (e.g. `PE2032`).  
* **500 + tags** grouped into sensors, drives, operator devices, safety, and auxiliaries—ready for ViewSE, Ignition, or any OPC client.  
* **Rock-solid diagnostics** – built-in fault bits, time-outs, and alarm banners expose every sensor miss and motor overload.  

---

#### 🚀 Getting started

1. **Clone** the repo and open the `.factory` file in Factory I/O (v2.5 + recommended).  
2. Open `DNS_Factory.acd` in Studio 5000 v34, set the controller type to **Logix Emulate 5580**, and start the emulator.  
3. Match the IP/Slot in *Drivers → Allen-Bradley ControlLogix* inside Factory I/O.  
4. Press **Run**—boxes flow from assembly to palletising while the tag map lights up in the HMI.

---

#### 🤝 Contributing
Spotted a logic edge case or want to add a new line? Open an issue or PR—tag-naming guidelines are in `CONTRIBUTING.md`.

---

#### 📄 Licence
All original PLC code, tag documentation, and CAD layouts are released under the MIT Licence. Factory I/O assets are redistributed under Factory I/O’s educational sharing terms.

> *“Simulate boldly, deploy safely.”*
