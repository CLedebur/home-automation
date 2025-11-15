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

---

# Example Equipment & Pricing

Here are **three strong options** for each of your four equipment categories: heat pump, solar panels, battery storage, and a smart mixing/thermostatic valve. These suggestions include brand/model, approximate Portuguese-supplier references, and estimated pricing (for budgeting purposes). You’ll still need to confirm actual quotes & install costs with local suppliers.

---

## 1) Heat Pump (Air-to‐Water)  
- **Daikin Altherma 3 M EBLA 8 kW** — supplier example ClimaMarket Portugal.  [oai_citation:0‡Climamarket B2C Europa](https://climamarket.com/products/daikin-altherma-3-m-ebla-8-kw-single-phase-air-to-water-heat-pump-with-hydronic-module?utm_source=chatgpt.com) Estimate: **€5 000–€7 000** for the unit (installer cost higher).  
- **Mitsubishi Electric Eco Inverter 8 kW (SUZ-SWM80VA)** — imported model; good efficiency.  [oai_citation:1‡heating-pump.com](https://heating-pump.com/product/mitsubishi-electric-eco-8-kw-suz-swm80va-external-air-to-water-heat-pump/?utm_source=chatgpt.com) Estimate: **€4 500–€6 000** unit cost.  
- **Aquapura Inverter HT (4-20 kW range)** — Portuguese supplier ENERGIE EST.  [oai_citation:2‡ENERGIE EST, Lda.](https://energie.pt/en/produtos-energie/aquapura-inverter-ht/?utm_source=chatgpt.com) Estimate: **€6 000–€8 000** including indoor + outdoor module.

---

## 2) Solar Panels / PV Kit (~6-7 kWp)  
- **SunPower / Premium mono panels** via Portuguese supplier (eg Solar Algarve)  [oai_citation:3‡solar-algarve.com](https://solar-algarve.com/?utm_source=chatgpt.com) Estimate: ~ **€6 000–€8 000** installed for 6-7 kWp.  
- **Grace Solar panels + mounting kit** from a Portuguese installer referenced among top companies.  [oai_citation:4‡bymea.com](https://www.bymea.com/blog/top-10-solar-companies-portugal?utm_source=chatgpt.com) Estimate: ~ **€5 500–€7 500**.  
- **Mid-tier mono panels (EU/Asian brand)** via national wholesaler (listed in supplier directory).  [oai_citation:5‡ENF Solar](https://www.enfsolar.com/directory/seller/Portugal?utm_source=chatgpt.com) Estimate: ~ **€5 000–€6 500**.

---

## 3) Battery Storage (12-15 kWh usable)  
- **15 kWh LiFePO4 “51.2 V” pack** from Portuguese online retailer (“HomeLowCost”) listed at ~ €2 312 for the module. Estimate full system (inverter + install) ~ **€4 000–€5 000**.  
- **Battery + inverter kit (≈10 kWh)** Portuguese market price ~ €6 500–€7 100 (for 10 kWh) after subsidies.  [oai_citation:6‡en.solarinverterbattery.com](https://en.solarinverterbattery.com/blog/portugal-10kwh-home-battery-costs-2025-save-with-subsidies?utm_source=chatgpt.com) Upscaled to 15 kWh might be ~ **€7 000–€9 000**.  
- **Large storage system (12-20 kWh) via local integrator (GSL ENERGY case 10.24 kWh)**  [oai_citation:7‡GSL Energy](https://www.gsl-energy.com/portugal-energy-storage-solutions-20kwh-lithium-battery-deye-inverter-installation.html?utm_source=chatgpt.com) For 15 kWh likely ~ **€8 000–€10 000** installed.

---

## 4) Mixing / Thermostatic Valve for DHW Integration  
- **Watts e-ULTRAMIX® Smart Thermostatic Mixing Valve** — supports remote control/modbus.  [oai_citation:8‡watts.eu](https://www.watts.eu/en-gb/products/eu/thermostatic-mixing-valves/high-productivity-mixing-valves/smart-thermostatic-mixing-valve-e-ultramix?utm_source=chatgpt.com) Estimate: **€300–€600** depending on size/ports.  
- Standard thermostatic mixing valve (non-smart) by major European brand + added temperature sensor for Home Assistant. Estimate: **€150–€300**.  
- High-end electronic mixing station (with legionella cycle, record logging) with remote interface. Estimate: **€500–€800**.

---

### 📋 Quick Summary Table

| Category        | Option Reference                           | Estimated Installed Cost*     |
|-----------------|--------------------------------------------|-------------------------------|
| Heat Pump       | Daikin / Mitsubishi Electric / Aquapura    | €5,000 – €8,000 (unit only)   |
| Solar PV Kit    | SunPower / Grace Solar / Mid-tier          | €5,000 – €8,000 (6-7 kWp)     |
| Battery Storage | 12-15 kWh usable                            | €4,000 – €10,000              |
| Mixing Valve    | Watts e-ULTRAMIX® or equivalent            | €150 – €800                   |

\* Excludes full labour/installation, piping/structural upgrades, permits.

---

# Inverters

Below are **three top-tier hybrid inverters** that meet **ALL** of your requirements:

✔ Work perfectly with **Home Assistant** (local API or MQTT)  
✔ Provide **backup power during outages** (UPS mode / islanding)  
✔ Support **dynamic load balancing** (with CT clamps)  
✔ Integrate smoothly with **batteries (12–20 kWh)**  
✔ Are widely available in **Portugal**  
✔ Have strong installer support & long warranties  

I’m giving you the **best-fit three**, not “10 random ones.”

---

# 🥇 **1. Huawei Sun2000 + LUNA Battery System (Top Smart Ecosystem)**

### **Why it fits your needs**
- Excellent **backup/UPS** function  
- **Zero-export** and **peak shaving** using CT clamps  
- Extremely efficient (97.5%+)  
- Excellent Portuguese installer coverage  
- Very good long-term reliability  
- Supports **Home Assistant via Modbus-TCP** or third-party integrations  
- Works beautifully with **12–15 kWh battery packs** (LUNA modules stack in 5 kWh blocks)

### **Pros**
- One of the best hybrid inverters globally  
- Elegant modular battery system  
- Fast UPS transfer (~20 ms)  
- Smart home integration is mature  
- Less noise and heat than many competitors  

### **Cons**
- Locked into the **LUNA battery** ecosystem (expensive)  
- Backup output may require a **separate “critical loads” panel**  

### **Best For:**  
A “no drama” smart system with deep integration and high reliability.

---

# 🥈 **2. Sungrow SH10RT / SH6.0RT Series (Best All-Rounder for HA)**

### **Why it fits your needs**
- Excellent **backup** performance  
- Very flexible **battery choices** (Sungrow SBR or third-party packs)  
- Fully compatible with **Home Assistant via Modbus-TCP**  
- Dynamic load control and zero-export modes  
- Great price/performance ratio in Portugal  

### **Pros**
- Strong, reliable brand with EU support  
- Battery packs are cheaper than Huawei  
- Easy to integrate with **DIY or third-party LiFePO4 batteries**  
- Great performance in both grid-tied & off-grid modes  

### **Cons**
- App is less polished  
- Backup output also typically requires a dedicated loads panel  

### **Best For:**  
Value + flexibility + HA automation, with room to grow to 15–20 kWh storage later.

---

# 🥉 **3. GoodWe EH/ET Series (Best for Open Protocols & HA Power Users)**

### **Why it fits your needs**
- Excellent support for **Home Assistant** (modbus, MQTT, or via SEMS API)  
- Superb **backup/off-grid** functionality (ET series does full-house islanding)  
- Works with a wide range of **third-party batteries** (Pylontech, BYD, Dyness, DIY packs)  
- Very affordable vs Huawei/Sungrow  

### **Pros**
- Hugely flexible ecosystem  
- HA integration is extremely strong  
- Good installer presence in Portugal  
- ET series supports **whole-home UPS**  
- Can use **generic 48 V LiFePO4 batteries** (cheap!)  

### **Cons**
- Fans can be louder under heavy load  
- Build quality slightly behind Huawei/Sungrow  

### **Best For:**  
Automation enthusiasts, DIY battery users, or anyone wanting maximum flexibility.

---

# ⚡ Quick Comparison Table

| Feature | **Huawei Sun2000** | **Sungrow SH-RT** | **GoodWe ET/EH** |
|--------|----------------------|-------------------|------------------|
| Home Assistant | Modbus-TCP, strong community integrations | Modbus-TCP, excellent | Modbus/MQTT, best flexibility |
| Backup | Yes (fast UPS) | Yes | Yes (whole-home capable) |
| Battery Type | Proprietary LUNA | Sungrow SBR or 3rd-party | Works with almost ANY LiFePO4 |
| Price | High | Mid | Mid/Low |
| Reliability | Excellent | Excellent | Very good |
| Ideal For | Seamless ecosystem | Balanced system | Power users + DIY |

---

# 🧭 Which One Should YOU Choose?

### Based on your setup (heat pump, Baxi, F520 logger, EV trickle charging, Home Assistant automation):

### ⭐ **If you want the simplest, most robust system → Huawei Sun2000**
- “Apple-like” ecosystem  
- Minimal headaches  
- Superb performance  
- Best long-term support  

### ⭐ **If you want the best value + HA integration → Sungrow SH10RT**
- Cheaper than Huawei  
- Very strong battery and automation support  
- Easy to expand battery to 15 kWh  

### ⭐ **If you want maximum flexibility / DIY battery → GoodWe ET/EH**
- Can use **cheap 48 V LiFePO4 batteries**  
- Very hackable and automatable  
- Great for an HA-heavy home like yours  

---

# 🔧 Recommended Battery Pairings (12–15 kWh)

| Inverter | Recommended Battery |
|----------|---------------------|
| **Huawei Sun2000** | Huawei **LUNA 15 kWh** (most expensive but simplest) |
| **Sungrow SH-RT** | Sungrow **SBR096–SBR160** series (stackable modules) |
| **GoodWe ET** | **Pylontech US5000**, **Dyness BX6.3**, or a DIY **48–51 V LiFePO4** pack |

Your earlier 15 kWh LiFePO4 example (€2,300 battery pack) works perfectly with **GoodWe** and **Sungrow** if compatible BMS is used (common in Portugal).

---

# 🎯 Final Recommendation for You

**Sungrow SH10RT with ~15 kWh Sungrow SBR battery**  
→ Best balance of cost, reliability, Home-Assistant friendliness, and full-house resilience.

But if budget allows and you want “plug-and-forget” stability:

**Huawei Sun2000 + LUNA**  
→ You will *never* regret this one.
