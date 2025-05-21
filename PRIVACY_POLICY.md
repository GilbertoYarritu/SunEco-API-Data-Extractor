<!-- PRIVACY_POLICY.md -->

# Privacy Policy

**Last updated:** 2025-05-21

This Privacy Policy governs the use of **SunEco API Data Extractor** (the “App”), provided by **Gilberto Yarritu and Associates** in Monterrey, Mexico.

---

## 1. Deployment & Runtime

- The App is delivered as Google Apps Script code that you install into **your** Google Cloud/Apps Script environment.  
- **No code, data, credentials, or logs ever run or reside on our servers.** We simply provide the script; all execution, credential handling, data writing, and storage happen entirely within your Google account.

---

## 2. Information We Collect

1. **Third-Party API Credentials**  
   - **Growatt & Huawei FusionSolar & SEMS/GoodWe:** account name and password (hashed in memory via MD5 for Growatt/Huawei; plain for SEMS).  
   - **Huawei FusionSolar:** also requires a `systemCode`.  
   - **SMA (OAuth2):** `client_id` and `client_secret`.  
   - Credentials are used only at runtime by your Apps Script and are **not** stored persistently outside your environment.

2. **Solar Data Metrics**  
   - **Growatt & Huawei & SEMS (GoodWe):** daily yield (`eToday` for Growatt; `yieldKWh` for Huawei; `eday` for SEMS), device serials (`sn`), plant IDs, per-plant totals and status flags.  
   - **SMA:** timestamped logs of energy and power per inverter (`Energy Pv`, `Power Pv`) for the previous day.

3. **Spreadsheet Data**  
   - All retrieved records are written directly to your Google Sheets (tabs like `Growatt Daily`, `DailyPower`, `Acumulado Diario`, `Acumulado Diario Planta`, `EnergyLogs`). We do **not** store copies outside your sheet.

4. **Usage & Log Data**  
   - Script execution timestamps, errors/exceptions, and any debug logs within your Apps Script project.

5. **Google Account & Environment Data**  
   - Your Google account ID (read at runtime but not retained), script time zone, and execution context (IP, user agent).

---

## 3. How We Use Your Information

- **Connection & Retrieval:** Use supplied credentials or OAuth2 token to fetch your solar data from each platform.  
- **Data Writing:** Insert fetched data rows into designated Sheets.  
- **Monitoring & Debugging:** Record execution metadata to diagnose failures and improve performance.  
- **Support:** Access your logs when troubleshooting issues you report.

---

## 4. Data Sharing & Disclosure

- **No Selling/Renting:** We never sell or rent your personal or usage data.  
- **Service Providers:** Google (Apps Script platform) and any analytics or error-tracking services you enable.  
- **Legal:** Disclose only if required by law or to protect our legal rights.

---

## 5. Data Retention

- **Credentials:** Held only in memory for each script run—never persisted on our side.  
- **Fetched Data & Logs:** Persist only in your Google Sheets and Apps Script logs. We do **not** store or archive any records on our servers.  
- **Deletion Requests:** Since we hold no records, nothing needs to be erased from our side—but you can delete any data or logs in your own Cloud project at any time.

---

## 6. Your Rights

Depending on your jurisdiction, you may have rights to:  
- Access or export your data from your Google Sheets.  
- Request deletion of any logs we maintain (none held).  
- Object to or restrict processing of your data.  

To exercise these rights, email **gilbertoyarritu@gmail.com**.

---

## 7. Changes to This Policy

We may update this policy. The “Last updated” date will reflect changes. Major updates will be noted in our GitHub repo’s **Releases**.

---

## 8. Contact Us

If you have questions or concerns, please contact:  
- **Email:** gilbertoyarritu@gmail.com  
- **Address:** Monterrey, Nuevo León, Mexico  
