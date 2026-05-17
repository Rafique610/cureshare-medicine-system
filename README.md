# CureShare BMS

## Quickest way to run

### Option 1 — Double-click (Windows)
Double-click `run.bat` inside the CureShare folder.
Requires Maven installed. If Maven is not installed, use Option 2.

### Option 2 — Eclipse (import and run with one click)
1. **File → Import → Maven → Existing Maven Projects** → select `CureShare` folder → Finish
2. Wait for dependencies to download (internet required, ~1 min)
3. Right-click project → **Maven → Update Project** → OK
4. In the top menu: **Run → Run Configurations → Java Application → CureShare → Run**
   - If "CureShare" is not listed, double-click "Java Application" to create new:
     - Main class: `com.cureshare.app.MainApp`
     - Project: `CureShare`
     - Arguments tab → VM Arguments: paste line from ECLIPSE_VM_ARGS.txt

### Option 3 — Terminal
```
cd CureShare
mvn javafx:run
```

---

## Login Credentials

| Role       | Email                   | Password  |
|------------|-------------------------|-----------|
| Admin      | admin@cureshare.pk      | admin123  |
| Household  | ahmad@gmail.com         | pass123   |
| Pharmacy   | medplus@pharmacy.pk     | pharm123  |
| Charity    | hope@ngo.pk             | hope123   |

---

## Connect MySQL (optional)
1. Run: `mysql -u root -p < cureshare_schema.sql`
2. Edit `DatabaseConfig.java` → `USE_DATABASE = true` + your password
3. Run normally
