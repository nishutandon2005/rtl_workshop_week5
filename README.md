# 📋 Week 5: OpenROAD Flow - Floorplan & Placement

> **Mission:** Install OpenROAD Flow Scripts and execute Floorplan + Placement stages only

## 🔄 Physical Design Flow

```
RTL → Synthesis → Floorplan → Placement → Routing → GDSII
                     ↑           ↑
                  [START]     [STOP]
```

## 🌟 What is OpenROAD?

Open-source RTL-to-GDSII flow for digital IC design.

**Features:**
- 🚀 Rapid design iterations
- 🎓 Academic research friendly
- 🏭 Industry-standard prototyping
- 🆓 Fully open-source

## 📂 Directory Structure

```
OpenROAD-flow-scripts/
├── docker/          # Docker installation
├── flow/            # Core RTL-to-GDS flow
│   ├── designs/     # Example designs
│   ├── platforms/   # Technology libraries
│   └── Makefile     # Flow execution
├── tools/           # Required tools
└── setup_env.sh     # Environment setup
```

## 🚀 Installation Steps

### 1. Clone Repository
```bash
git clone --recursive https://github.com/The-OpenROAD-Project/OpenROAD-flow-scripts
cd OpenROAD-flow-scripts
```

### 2. Setup Dependencies
```bash
sudo ./setup.sh
```

### 3. Build OpenROAD
```bash
./build_openroad.sh --local
```

### 4. Verify Installation
```bash
source ./env.sh
yosys -help
openroad -help
```



## 🎯 Execute Floorplan & Placement

```bash
cd flow
make
```

**Stages Completed:**
- ✅ Floorplan: Core area, die dimensions, I/O placement
- ✅ Placement: Standard cell arrangement
- ⏸️ Routing: Stopped (as required)



## 👁️ Visualize Results

```bash
make gui_final
```


## 📊 Results Summary

| Stage | Status | Output |
|-------|--------|--------|
| Installation | ✅ | Tools operational |
| Floorplan | ✅ | Core area defined |
| Placement | ✅ | Cells placed |
| Routing | ⏸️ | Not executed |

## 🔍 Key Concepts

**Floorplanning:**
- Defines chip boundaries
- Places I/O pads and power rails
- Establishes design feasibility

**Placement:**
- Arranges standard cells
- Optimizes timing and congestion
- Prepares for routing

## 🎉 Conclusion

Successfully completed OpenROAD installation and executed Floorplan + Placement stages. Design ready for CTS & Routing.

