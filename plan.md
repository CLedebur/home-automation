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

If you want, I can also generate:

✔ A **“diagram” version** (ASCII schematic)  
✔ A **system bill of materials** (recommended models)  
✔ Home Assistant **automation templates** for HP + DHW + EV + battery orchestration
