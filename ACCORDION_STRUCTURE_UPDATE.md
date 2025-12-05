# Accordion Structure Update - December 3, 2025

## 🎯 **MAJOR STRUCTURAL CHANGE**

### **FROM: Company-Wide Processes**
- ❌ Brainstorm ALL processes across the company
- ❌ Select Top 3 processes (company-wide)
- ❌ 3 KPIs total (company-wide)
- ❌ **Total: 5 Activities → 3 Processes → 3 KPIs**

### **TO: Activity-Specific Processes** ✅
- ✅ Each Core Activity has its own 3 processes
- ✅ Each process has 1 dedicated KPI
- ✅ **Total: 5 Activities → 15 Processes (3 per activity) → 15 KPIs (1 per process)**

---

## 📊 **NEW DATA STRUCTURE**

### **Activity Data Model:**
```javascript
const [activityData, setActivityData] = useState([
    {
        isExpanded: true/false,  // Accordion state
        processes: [
            { 
                process: 'Process name', 
                kpi: { 
                    name: 'KPI name', 
                    unit: '%', 
                    target: '85' 
                } 
            },
            // ... 2 more processes
        ]
    },
    // ... 4 more activities
]);
```

### **Mapping:**
- **Activity Index [0-4]** corresponds to the 5 core activities from Page 1
- **Each Activity** → 3 Processes → 3 KPIs
- **Total Fields:** 15 processes + 45 KPI fields (name, unit, target)

---

## 🎨 **ACCORDION UI DESIGN**

### **Layout Pattern:**
```
═══════════════════════════════════════════════════════════
▼ [1] Digital Marketing & Customer Acquisition           [−]
───────────────────────────────────────────────────────────
   ┌─────────────────────────────────────────────────────┐
   │ Process 1                                           │
   │ [Real-time sales tracking and reporting.........]   │
   │ KPI                                                 │
   │ [Sell-through rate] [%] [85]                        │
   └─────────────────────────────────────────────────────┘
   
   ┌─────────────────────────────────────────────────────┐
   │ Process 2                                           │
   │ [Customer feedback collection.................]     │
   │ KPI                                                 │
   │ [Response rate] [%] [75]                            │
   └─────────────────────────────────────────────────────┘
   
   ┌─────────────────────────────────────────────────────┐
   │ Process 3                                           │
   │ [Social media engagement......................]     │
   │ KPI                                                 │
   │ [Engagement score] [score] [4.2]                    │
   └─────────────────────────────────────────────────────┘
───────────────────────────────────────────────────────────

▶ [2] Product Development & Innovation                   [+]

▶ [3] Customer Support Excellence                        [+]

▶ [4] Sales Operations                                   [+]

▶ [5] Strategic Planning                                 [+]
═══════════════════════════════════════════════════════════
```

### **Visual Features:**
1. **Accordion Header:**
   - Clickable full-width button
   - Shows activity number + name
   - Toggle icon (− when expanded, + when collapsed)
   - Hover effect (gray background)

2. **Accordion Content:**
   - Light gray background (`bg-gray-50`)
   - 3 white cards for each process + KPI combo
   - Vertical spacing for clarity
   - Only visible when expanded

3. **Process + KPI Card:**
   - White background with border
   - Process input (full width)
   - KPI grid (Name: 6 cols, Unit: 3 cols, Target: 3 cols)
   - Clear labels for each section

---

## 🔄 **USER INTERACTION FLOW**

### **Page 1: Core Activities**
1. Define Value Proposition
2. Brainstorm Activities
3. Select Top 5 Activities
4. Click "Next →" to proceed

### **Page 2: Processes & KPIs (NEW ACCORDION STRUCTURE)**
1. **See 5 Accordion Headers** - One for each core activity
2. **First activity is expanded by default**
3. **Click to expand/collapse** any activity
4. **Fill in 3 processes per activity** - Directly in each accordion
5. **Fill in 1 KPI per process** - Name, Unit, Target fields
6. **Repeat for all 5 activities**
7. **Export** when complete

### **No More:**
- ❌ No "Brainstorm ALL processes" section
- ❌ No "Select Top 3" workflow
- ❌ No separate KPI section

---

## 💾 **LOCALSTORAGE & EXPORT**

### **Saved Data:**
```json
{
  "valueProposition": "...",
  "brainstormActivities": [...],
  "coreActivities": [...],
  "showBrainstormSelection": true/false,
  "activityData": [
    {
      "isExpanded": true,
      "processes": [
        { "process": "...", "kpi": { "name": "...", "unit": "...", "target": "..." } },
        ...
      ]
    },
    ...
  ]
}
```

### **Export Format:**
```
CORE ACTIVITIES → PROCESSES → KPIs

[1] DIGITAL MARKETING & CUSTOMER ACQUISITION
  → Process 1: Real-time sales tracking
     KPI: Sell-through rate (%): 85
  → Process 2: Customer feedback collection
     KPI: Response rate (%): 75
  → Process 3: Social media engagement
     KPI: Engagement score (score): 4.2

[2] PRODUCT DEVELOPMENT & INNOVATION
  → Process 1: ...
  ...
```

---

## 📏 **COMPARISON: Old vs. New**

| Aspect | **OLD (Company-Wide)** | **NEW (Activity-Specific)** |
|--------|------------------------|----------------------------|
| **Structure** | 5 Activities → 3 Processes → 3 KPIs | 5 Activities → 15 Processes → 15 KPIs |
| **Scope** | 3 processes across entire company | 3 processes per activity |
| **UI Pattern** | Multi-section worksheet | Accordion cards |
| **Brainstorm** | Brainstorm all, then select top 3 | Direct input per activity |
| **KPI Assignment** | 3 KPIs for 3 processes | 1 KPI per process (15 total) |
| **Collaboration** | All sections visible | Focus on one activity at a time |
| **Data Fields** | 21 total fields | 75 total fields |

---

## ✅ **ALIGNMENT WITH FAST TRACK METHODOLOGY**

### **Why This Change Makes Sense:**

1. **Activity-Process Relationship:**
   - Each activity has **specific processes** that enable it
   - Processes are **not generic** across the company
   - Example: "Digital Marketing" has different processes than "Product Development"

2. **KPI Specificity:**
   - Each process needs **its own success metric**
   - 1:1 mapping ensures **clear accountability**
   - Example: "Sales tracking" process → "Sell-through rate" KPI

3. **Scalability:**
   - 90-minute team meeting can cover all 15 processes
   - Accordions allow **focus** on one activity at a time
   - Team can discuss **related processes together**

4. **Excel Tool Parity:**
   - Matches the structure described in `process.txt`
   - Aligns with Zara/Company X examples (3 processes per activity)
   - Maintains the 80/20 principle (5 activities = 20% of all work)

---

## 🎯 **BENEFITS OF ACCORDION LAYOUT**

1. **Visual Simplicity:**
   - Collapsed accordions show **clean overview** of all 5 activities
   - Expanded accordion shows **focused detail** for one activity
   - No overwhelming walls of input fields

2. **Team Collaboration:**
   - Discuss **one activity at a time**
   - All team members can see the **current focus**
   - Natural conversation flow: "Let's talk about Marketing..."

3. **Flexibility:**
   - Can have **multiple accordions open** for comparison
   - Can **collapse completed sections** to reduce clutter
   - Can **jump between activities** easily

4. **Mobile-Friendly:**
   - Accordions stack naturally on small screens
   - No horizontal scrolling required
   - Touch-friendly expand/collapse buttons

---

## 🚀 **NEXT STEPS (IF NEEDED)**

### **Potential Enhancements:**
1. **Expand All / Collapse All** buttons
2. **Progress indicators** per activity (e.g., "2/3 processes filled")
3. **Drag-and-drop reordering** of processes within an activity
4. **Auto-suggest KPIs** based on process keywords
5. **Validation** to ensure all 15 processes + KPIs are filled
6. **Print view** that expands all accordions automatically

### **Alternative Layouts (if accordions don't work):**
- **Tabbed Interface**: One tab per activity, shows 3 processes
- **Wizard Flow**: Step-by-step through each activity sequentially
- **Grid View**: 5 columns (1 per activity) × 3 rows (processes)

---

## 📝 **TECHNICAL NOTES**

### **Key Functions:**
- `toggleAccordion(activityIndex)` - Expand/collapse
- `updateProcess(activityIndex, processIndex, value)` - Update process name
- `updateKPI(activityIndex, processIndex, field, value)` - Update KPI field

### **Removed Code:**
- `brainstormProcesses` state (no longer needed)
- `coreProcesses` state (no longer needed)
- `kpis` state (now nested in `activityData`)
- `showProcessSelection` workflow (no longer needed)
- Brainstorm → Select UI sections

### **Added Code:**
- `activityData` state (new hierarchical structure)
- Accordion component in ProcessesPage
- Process + KPI cards inside accordions
- Updated export and localStorage logic

---

## 🎉 **COMPLETION STATUS**

✅ Data model restructured  
✅ Accordion UI implemented  
✅ localStorage updated  
✅ Export function updated  
✅ No linter errors  
✅ Launched in browser  
✅ Maintains Fast Track branding (Plaak + Riforma fonts, black/white/grey)  

**Ready for user testing!** 🚀


