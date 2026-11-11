# Rolls-Royce Aircraft Engine (100% Accurate Replica) | Higgsfield AI & Blender Link

A high-fidelity digital twin and procedural replica of the **Rolls-Royce Trent Turbofan Aircraft Engine** (Trent 1000 / Trent XWB / UltraFan architecture) featuring a **Higgsfield AI Generative Studio** and a dedicated **Send and Link to Blender** integration bridge.

---

## 🌐 Live Web Preview & 3D Interactive Viewport
- **Live Preview URL**: [https://antigravity.luch.dev/site/4186e3b8-b0f0-4166-92ac-d5020524e0c4/2728d39a1bddb927d57d53c7/](https://antigravity.luch.dev/site/4186e3b8-b0f0-4166-92ac-d5020524e0c4/2728d39a1bddb927d57d53c7/)

---

## 🛠️ Engine Architecture & Subsystems (100% Accurate Replica)

The engine features Rolls-Royce's signature **three-shaft (triple-spool)** high-bypass turbofan architecture, with 12 distinct mechanical sub-assemblies:

1. **LP Fan & Aerodynamic Scimitar Blades**: 22 wide-chord hollow-core diffusion-bonded titanium blades with aerodynamic twist and scimitar curvature.
2. **Spinner Cone with Spiral**: Bullet nose cone painted with the trademark high-contrast white spiral line (warns ground crew and repels birds).
3. **Fan Containment Casing & Bypass OGVs**: Titanium containment case with 36 outlet guide vanes (OGVs) to straighten swirling bypass air.
4. **Intermediate Pressure Compressor (IPC)**: 8-stage axial compressor blisks on the IP spool.
5. **High Pressure Compressor (HPC)**: 6-stage axial compressor blisks delivering a 50:1 overall pressure ratio.
6. **Annular Combustor & 20 Radial Fuel Nozzles**: Ceramic Matrix Composite (CMC) thermal barrier liner with 20 radial lean-burn dual-orifice fuel nozzles and glowing flame core.
7. **High Pressure Turbine (HPT)**: Single-crystal nickel superalloy (CMSX-4) blades with film cooling channels driven by 1,720 °C combustor gases.
8. **Intermediate Pressure Turbine (IPT)**: Turbine disc driving the IPC via the middle concentric shaft.
9. **Low Pressure Turbine (5-Stage LPT)**: 5 consecutive turbine stages driving the 118-inch front fan.
10. **Concentric Triple-Spool Shafts**: 3 nested concentric drive shafts (LP inner shaft, IP middle sleeve, HP outer sleeve) rotating at differential speeds without internal gearboxes.
11. **Core Exhaust Nozzle & Chevrons**: Conical aerodynamic tail plug and 16 Rolls-Royce triangular serrated chevrons for jet noise attenuation.
12. **Accessory Gearbox & Dual FADEC**: Bottom-mounted accessory gearbox with radial driveshaft tower, dual-channel Full Authority Digital Engine Control (EEC) computers, fuel pumps, oil tank, and hydraulic lines.
13. **Nacelle Cowling & Wing Pylon Mount**: Polished titanium intake cowl lip, split 180° cowl shells with 50% cutaway mode, and wing pylon bracket.

---

## 🚀 How to Send and Link to Blender

### Option A: 1-Click Blender Script (`rolls_royce_blender_link.py`)
1. Open **Blender** (version 3.0, 4.0, or newer).
2. Switch to the **Scripting** tab at the top.
3. Click **+ New** to create a new script.
4. Open or paste [`rolls_royce_blender_link.py`](rolls_royce_blender_link.py).
5. Click **▶ Run Script** (or press `Alt + P`).
6. **Done!** The script automatically creates:
   - 9 organized collections:
     - `RR_01_Fan_and_Spinner`
     - `RR_02_IP_Compressor`
     - `RR_03_HP_Compressor`
     - `RR_04_Combustor`
     - `RR_05_Turbine_Stages`
     - `RR_06_Concentric_Shafts`
     - `RR_07_Casing_and_Chevrons`
     - `RR_08_Accessory_Gearbox_FADEC`
     - `RR_09_Nacelle_Cowling`
   - Principled BSDF materials (Titanium, Nickel Superalloy, Ceramic Thermal Barrier, Combustor Flame, Aviation White paint).
   - Differential rotation drivers (`#frame * speed`) for LP (2,700 RPM), IP (7,150 RPM), and HP (12,480 RPM) spools.
   - Press **Spacebar** in Blender to watch the live engine simulation!

### Option B: Export 3D Wavefront Mesh (`.obj`)
- In the web app, click **Send & Link to Blender** → **Wavefront OBJ 3D Export** → **Export & Download rolls_royce_engine.obj**.
- In Blender, go to `File → Import → Wavefront (.obj)`.

### Option C: Live Bridge Server Link
1. Run the local bridge server:
   ```bash
   python3 blender_bridge_server.py --port 8081
   ```
2. In the web app, click **Send & Link to Blender** → **Live Bridge Server Link** → **Push Higgsfield Mesh to Blender**.

---

## 🧬 Higgsfield AI Generative Studio
The built-in **Higgsfield AI Generative Studio** allows synthesizing and re-generating components via neural tensor diffusion:
- **Aerodynamic Presets**:
  - *Trent XWB-97* (Airbus A350-1000 spec, 97,000 lbf thrust)
  - *Trent 1000* (Boeing 787 Dreamliner spec, bleedless electric start)
  - *Rolls-Royce UltraFan* (100,000 lbf geared turbofan, 14:1 bypass ratio)
  - *Trent 7000* (Airbus A330neo spec, high-efficiency FADEC)
- **Generative Controls**:
  - Blade Twist Angle (20° to 55°)
  - Bypass Ratio (8.0:1 to 14.0:1)
  - Acoustic Chevron Serrations
- **Real-Time Synthesis**: Simulates multi-step latent diffusion, logs component generation, and updates the 3D model and Blender export in real time.

---

## 🎮 Interactive Controls in the Web App
- **Differential Triple-Spool Rotation**: LP, IP, and HP spools spin at authentic relative speed ratios.
- **FADEC Throttle Slider**: Adjust from 20% Ground Idle to 100% Max Takeoff with dynamic thrust (lbf) and EGT (°C) telemetry.
- **Exploded View Slider**: Smoothly expands all 12 sub-assemblies along axial and radial vectors (0% to 100%).
- **Cutaway Mode Toggle**: Instantly toggles between Solid Shell, 50% Cutaway, and Core Only to reveal inner rotating compressor and turbine blisks.
- **Dynamic Particle Airflow**: Real-time streamlines showing cold intake air, bypass stream, and high-velocity exhaust gases.
- **Procedural Sound Engine**: Web Audio API turbofan spool-up whine and jet core roar with mute toggle.
- **Component Inspector**: Click any part in 3D or the hierarchy list to view metallurgy, max temperatures, and part specifications.
