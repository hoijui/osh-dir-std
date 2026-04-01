# Designish — OSH Project Directory Structure (Circular & Lifecycle-Driven)

**Principle:** "Process over product" — lifecycle-driven, designer-friendly, and circular.

The **Designish** standard is built around the **product lifecycle** and the **design process**. Instead of naming directories after file types or technical domains, they are named after the **phase** a file belongs to. This approach makes a project's maturity, progress, and sustainability path immediately visible to contributors of all backgrounds.

---

## Naming Rules

- **Numbered prefixes:** `10_`, `20_`, `30_` for top-level areas; `01_`, `02_`, ... for sub-phases.
    
- **Lowercase with underscores:** `assembly_guide` not `AssemblyGuide` or `assembly-guide`.
    
- **Descriptive phase names:** `03_make` not `output` or `export`.
    

---

## Directory Tree


``` m

root((my-osh-project))
├── LICENSES/                  # REUSE license files (CERN-OHL, GPL, CC-BY-SA)
├── README.md                  # Project overview
├── okh.toml                   # Open Know-How manifest for crawlers & indexers
├── 10_management/             # The Studio — "Why" and "Who"
│   ├── 01_roadmap/            # Visual timelines and milestones
│   ├── 02_meetings/           # Community sync notes (YYYY-MM-DD_topic.md)
│   ├── 03_stakeholders/       # Map of contributors and community members
│   ├── input/                 # Incoming briefs and stakeholder requests
│   └── output/                # Approved plans and mandates
├── 20_legal/                  # The Safety Net — Open Source protection
│   ├── compliance/            # CE/FCC certificates and test reports
│   ├── input/                 # Draft agreements and incoming requests
│   └── output/                # Signed licenses and legal approvals
├── 30_engineering/            # The Creative Pipeline — 5-Phase Process
│   ├── 01_concept/            # The Sketchbook — Ideas & Requirements
│   │   ├── requirements/      # Functional & sustainability requirements
│   │   ├── moodboards/        # Visual explorations and block diagrams
│   │   └── adr/               # Architecture Decision Records (NNN_topic.md)
│   ├── 02_design/             # The Workbench — Discipline-organized sources
│   │   ├── electronics/       # Schematics and PCB layouts (KiCad)
│   │   ├── mechanical/        # 3D CAD (FreeCAD/STEP) and 2D drawings
│   │   ├── wear_parts/        # Components designed for frequent replacement [NEW]
│   │   └── firmware/          # The "brain" of the hardware
│   ├── 03_make/               # The Factory — Everything to build one unit
│   │   ├── bom/               # Bill of Materials (CSV/MD with material data)
│   │   ├── assembly_guide/    # Visual step-by-step instructions
│   │   └── fabrication_files/ # Ready-to-manufacture files (STL, DXF, Gerbers)
│   ├── 04_validation/         # The Lab — Safety & Prototype testing
│   │   ├── safety/            # Risk analysis (FMEA)
│   │   └── test_reports/      # Documentation of what worked or broke
│   └── 05_release/            # The Gallery — Sharing with the world
│       ├── oshwa_certification/ # OSHWA compliance evidence
│       └── media/             # Hero shots, videos, and press kits
├── 40_stewardship/            # Circularity — Repair & Recovery [NEW]
│   ├── 01_maintenance/        # Cleaning, calibration, and upkeep logs [NEW]
│   ├── 02_repair/             # Troubleshooting and disassembly guides [NEW]
│   └── 03_recovery/           # Recycling paths and upcycling ideas [NEW]
└── 50_usage/                  # Implementation & Examples
    └── example/               # Settings, samples, and use-cases
```

---

## Key Characteristics

|**Property**|**Value**|
|---|---|
|**Naming Style**|Lifecycle phase (e.g., `10_management/`, `30_engineering/01_concept/`)|
|**Modularity**|Flat — single product; sub-assemblies live inside `02_design/`|
|**Decision Tracking**|ADRs in `01_concept/adr/` — design rationale is first-class|
|**Circular Focus**|Maintenance, Repair, and Recovery are prioritized in `40_stewardship/` [NEW]|
|**Handoff Zones**|`input/` and `output/` folders act as zones between disciplines|
|**Generated Files**|Explicitly separated in `fabrication_files/`|

---

## Why this works for Designers & Circularity

1. **Logical Flow**: Teams move naturally from `01_concept` to `05_release`.
    
2. **No "Code" Required**: Contributors work in discipline-specific folders using familiar tools.
    
3. **Sustainability by Design**: By pairing assembly with **disassembly** and **recovery** guides, the project moves from a linear to a circular lifecycle.
    
4. **Transparency**: Keeping `ADRs` and `test_reports` visible allows the "Trial and Error" process to become a community learning resource.
    

---

## Recommended For

Designer-led teams, sustainable hardware startups, and OSH projects aiming for long-term community stewardship and environmental responsibility.

## References

- `definition.csv` — machine-readable source
    
- `okh.toml` — Open Know-How (OKH) specification
    
- `REUSE specification` — License management
    
- `9R Framework` — Circular Economy principles [NEW]