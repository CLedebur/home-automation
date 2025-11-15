Below is a **single-page, clean, shareable overview** of your **complete integrated home energy + heating modernisation plan**.  
It reflects *everything* we discussed: heat pump in annex, Baxi integration, minisplits, PV + battery, EV charger, tariffs, electrical layout, and system architecture.

---

# **🏡 Integrated Home Energy & Heating Modernisation Plan**

## **1. House & Context**
- **365 m²**, 3-storey concrete + terracotta brick home (built 2003, no insulation).  
- **Climate:** Portugal – winters 8–15 ºC, summers 18–30 ºC.  
- **Existing systems:**
  - **Baxi STS-300** solar-thermal water heater (roof of annex).  
  - **Zantia Electra** solid-fuel boiler (broken).  
  - **3-head Samsung mini-split** upstairs.  
  - **Piping between annex ↔ main house** for radiators already in place.  
  - **6.9 kVA** contracted power.  
  - **Annex** has 30 A electrical feed + 40 A RCCB; semi-vented with slatted window.

---

# **2. Heating & Cooling Strategy**

### **A. Air-to-water heat pump (A2W HP) in the annex**
- Replaces dead Zantia boiler.  
- Sized ~**8–12 kW thermal** (radiators + DHW support).  
- Annex is ideal: existing radiator pipes, Baxi proximity, adequate electrical feed.

### **B. Multi-split AC for full-zone heating & cooling**
- Keep **3-head Samsung** upstairs.  
- Add **4-head multi-split** for lower floors (office, dining, workshop, media room).  
- Splits handle most heating/cooling efficiently (COP 3–4).

### **C. Radiators retain a central role**
- Radiator loop fed by new heat pump.  
- Provides background heating; splits handle peak comfort.

---

# **3. Domestic Hot Water (DHW) – Solar + Heat Pump Integration**

### **Flow configuration (recommended):**
```
Mains cold
   ↓
Baxi STS-300 solar tank (preheat)
   ↓
Heat pump DHW inlet (top-up to 50–55 ºC)
   ↓
Thermostatic mixing valve
   ↓
House taps
```

### **Operation**
- Sunny days → Baxi heats water for free; HP stays mostly off.  
- Cloudy days → HP lifts from preheated level to setpoint.  
- **Baxi electric element OFF** except:
  - Weekly **Legionella cycle** (≥60 ºC for 1 hr)  
  - Emergency backup  
- HP and Baxi controlled via temperature sensors + optional Home Assistant logic.

---

# **4. PV + Battery System**

### **Recommended sizing**
- **6–7 kWp solar PV** (≈9,000–11,000 kWh/year potential).  
- **10 kWh battery** for:
  - Blackout resilience  
  - Peak shaving (avoid ponta periods)  
  - Self-consumption  
  - EV charging synergy

### **Hybrid inverter (garage)**
- Supports:
  - Battery storage  
  - Backup/UPS mode  
  - Dynamic export control  
  - Load-shedding integration  
- Brands: Huawei Sun2000, Solis, Sungrow, GoodWe.

### **Critical loads panel (optional)**
- Lights, fridge, Internet/servers, office, key circuits.  
- HP on limited mode during outage if needed.

---

# **5. EV Charging with Load Shedding**

### **Smart EVSE (dynamic amperage control)**
- 7.4 kW capable, but normally throttled to **≤16 A** due to 6.9 kVA contract.  
- Uses CT clamp on main feed to avoid breaker trips.  
- Can be solar-prioritized or off-peak biased.  
- Integrates with inverter CTs or dedicated load sensor.

### **Outcome**
- EV charges from:
  - **Solar surplus first**  
  - **Off-peak hours next**  
  - Pauses automatically when heat pump / house load spikes.

---

# **6. Electrical & Placement Overview**

### **Garage (energy hub)**
- Main quadro elétrico  
- **Hybrid PV inverter + battery**  
- **EV charger**  
- CT clamps for:
  - Load shedding  
  - PV export control  
  - Home Assistant monitoring

### **Annex (plant room)**
- **Air-to-water heat pump hydraulic unit**  
- **Connection to radiator loop**  
- **Connection to Baxi DHW tank**  
- Annex is ideal: sheltered, vented, existing feeds.

### **Outdoor unit**
- Mounted on annex exterior wall with good airflow and condensate drainage.

---

# **7. Tariff Choice (MEO Energia)**

### **Recommended:** **Bi-Horário**
- Charge battery off-peak.  
- Avoid ponta by using battery + PV.  
- Run heavy loads (HP, EV, laundry) off-peak or solar hours.  
- Tri-horário only worth it with ≥10 kWh battery and very strict automations.

---

# **8. Summary of the Final Integrated System**

- **Heat pump in annex** replacing pellet/wood boiler.  
- **Solar + HP hybrid DHW**: Baxi does preheat; HP finishes.  
- **Radiators + minisplits** → full-house heating & cooling.  
- **6–7 kWp PV + 10 kWh battery** in garage → major savings + outage protection.  
- **Smart EV charger** with load shedding.  
- **Bi-horário tariff** + automation for peak shaving.  
- Annex + existing piping make installation straightforward and cost-efficient.  
- System tightly integrable with **Home Assistant** for optimization.

---
Below is a **clear, structured explanation** of how all the plumbing/hydronic connections should be arranged between:

- **Heat pump (air-to-water)**  
- **Baxi STS-300 solar thermal tank**  
- **Radiators in the main house**  
- **Domestic hot water taps**  

I’ll give you two diagrams:

1. **High-level block diagram**  
2. **Detailed hydronic connections (installer-ready)**  

And then I’ll explain *why* it’s done this way.

---

# **1) High-Level System Diagram**

```
            [ Outdoor Heat Pump Unit ]
                       │
               Refrigerant Lines
                       │
           [ Heat Pump Hydro Module ]
                  (in Annex)
         ┌────────────┴─────────────┐
         │                          │
   [Radiator Circuit]        [DHW Circuit]
         │                          │
         ▼                          ▼
   Radiators in              Baxi STS-300 Tank
   Main House                    (Solar)
                                    │
                                    ▼
                         [Mixing Valve → House Taps]
```

---

# **2) Detailed Hydronic Piping (Installer-Ready)**

This is the complete picture of how the **heat pump**, **Baxi**, and **radiators** interconnect.

```
                           ┌─────────────────────────────────────────┐
                           │            Annex Plant Room             │
                           └─────────────────────────────────────────┘
                                  │
                                  ▼
                     ┌──────────────────────────┐
                     │ Heat Pump Hydro Module   │
                     │  (indoor part of A2W)    │
                     └──────────────────────────┘
                          │               │
                          │               │
                          │               │
                (1) Radiator Loop    (2) Domestic Hot Water Loop
                          │               │
══════════════════════════╪═══════════════╪════════════════════════════

(1) **RADIATOR CIRCUIT**
---------------------------------------

Supply (flow) from HP  ──────────────────────► Existing pipe to house  
Return from house radiators ◄────────────────────────── Existing return  

Add:
- **Circulating pump** (if HP’s internal pump isn’t enough)  
- **Dirt separator & magnetic filter**  
- **Air separator**  
- **Buffer tank (50–100 L)** if needed for stabilizing short radiator cycles  

────────────────────────────────────────────────────────────────────────

(2) **DHW CIRCUIT (Baxi + HP)**  
-------------------------------------------

                        From mains cold
                               │
                               ▼
                    ┌─────────────────────┐
                    │  Baxi STS-300 Tank  │  
                    │  (Solar pre-heat)   │
                    └─────────────────────┘
                               │
                          Hot outlet
                               │
                               ▼
                ┌───────────────────────────┐
                │ Heat Pump DHW Port (coil or plate) │
                │  HP boosts water to 50–55 ºC       │
                └───────────────────────────┘
                               │
                     HP → Baxi → HP loop ends
                               │
                               ▼
                   ┌───────────────────────┐
                   │ Thermostatic Mixing   │
                   │ Valve (50–55 ºC out)  │
                   └───────────────────────┘
                               │
                               ▼
                         Hot water to taps
```

---

# **3) Explanation of How Everything Works**

## **A) Radiator Circuit**
- The heat pump produces low-temperature water (35–55 ºC).  
- This circulates through the **existing annex → house → annex** piping to all radiators.  
- A small buffer may be added to prevent the HP from short cycling.  
- TRVs (smart radiator valves) control room-by-room heat demand.

**No modification to house radiator piping is needed.**

---

## **B) Domestic Hot Water (DHW) Circuit**

This is the elegant part of your setup.

### **Step 1 – Cold water enters the Baxi STS-300**
- Solar heats the water for FREE  
- You get 20–60 ºC depending on sunshine  

### **Step 2 – Preheated water flows into the heat pump**
- The HP boosts it gently to **50–55 ºC**  
- Using far less electricity because the water is already pre-heated  

### **Step 3 – Mixed and sent to taps**
- A thermostatic mixing valve ensures **safe outlet temperature**  

### **Element in Baxi stays OFF** except for:
- Weekly **legionella cycle**  
- Emergency backup  

This setup makes your hot water *extremely efficient*.

---

# **4) What Valves / Sensors / Safety Parts Are Required**

### **Essential**
- Check valves (anti-thermosiphon)  
- 3-bar safety valve on DHW side  
- Mixing valve (50–55 ºC)  
- Expansion vessels (DHW and heating)  
- Automatic air vents  
- Dirt/magnetic filter  
- Insulated pipes between annex ↔ house  
- Non-return valve between Baxi ↔ HP loop  

### **Sensors to integrate with Home Assistant**
- Baxi top & bottom temperature probes  
- Heat pump DHW setpoint reading  
- Grid power (via F520 – already available)  
- Radiator loop temp supply/return  

---

# **5) What the Heat Pump Does NOT Do**
- It does **not** circulate refrigerant through the Baxi.  
- It does **not** directly heat the solar tank (unless it has a dedicated coil).  
- It only heats water *after* the Baxi has preheated it.

This protects your solar gains.

---

# **6) Two Variants You Can Choose Between**

## **Variant A: HP directly heats Baxi tank (1-coil HP-compatible)**  
If the HP supports external tank heating with a coil:
- The HP heats the **Baxi tank** directly  
- Solar still contributes  
- DHW is tapped from the Baxi

## **Variant B: HP uses INTERNAL tank / plate exchanger (most common)**
- Baxi → HP → taps  
- Baxi remains purely a pre-heater  
- HP has built-in plate exchanger for DHW

Variant B is simpler and works with all heat pumps.

---

# **7) Why This Layout Is Ideal for Your House**
- Annex is the perfect plant room (already piped, powered, and semi-vented).  
- Baxi is perfectly integrated as a primary DHW heater.  
- Radiator loop is reused without modification.  
- Heat pump handles low-temperature hydronic heating efficiently.  
- Minisplits handle peak room comfort.  
- PV + battery + F520 + EV charger all orchestrate the electrical demand.  
- Home Assistant can coordinate EVERYTHING.


