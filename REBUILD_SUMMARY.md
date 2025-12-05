# Core Activities Tool - Complete Rebuild Summary

## 🎯 **WHAT CHANGED**

### **FROM: Individual Survey Tool**
❌ Typeform-style one question at a time  
❌ Sequential flow for solo completion  
❌ 50+ separate screens  
❌ Designed for individual homework  

### **TO: Collaborative Worksheet Tool**
✅ **Excel-style worksheet** - all sections visible  
✅ **Two-page layout** for team meetings  
✅ **Guru-facilitated** 90-minute session  
✅ **Designed for collaborative discussion**  

---

## 📋 **NEW STRUCTURE**

### **Page 1: CORE ACTIVITIES**

**Left Sidebar (Context):**
- WHY (Purpose explanation)
- WHAT (What to identify)
- HOW (Step-by-step instructions)

**Right Worksheet:**
- **[01] Value Proposition** - Single text area
- **[02] Brainstorm Company Activities** - Multiple rows (add/remove)
- **[03] Top 5 Company Core Activities** - 5 fixed rows

### **Page 2: CORE PROCESSES AND KPIS**

**Left Sidebar (Context):**
- WHY (Purpose explanation)
- WHAT (What to identify)
- HOW (Step-by-step instructions)

**Right Worksheet:**
- **[01] Top 5 Core Activities** - Display from Page 1 (read-only)
- **[02] Brainstorm Processes** - Multiple rows (add/remove)
- **[03] Top 3 Company Core Processes** - 3 fixed rows
- **[04] KPIs** - 3 rows (Name | Unit | Target)

---

## 🎓 **HOW IT'S USED (From Guru Guide)**

### **90-Minute Team Meeting:**

**1. Do Better Than Last Time (10 min)**
- Reflect on previous sprint

**2. Topic Presentation by Guru (15 min)**
- Guru presents Brain Juice highlights
- Uses Zara/Company X examples

**3. Discussion Per Topic (30 min)**
- Team discusses together
- **"Work directly on the team tool"**
- Guru facilitates, team fills worksheet
- All sections visible for context

**4. Decision Per Topic (20 min)**
- Agree on Top 5 Activities & Top 3 Processes
- Finalize inputs together
- Assign accountability

**5. Reflection Time (15 min)**
- Close with clarity
- Ensure alignment

---

## ✅ **KEY FEATURES**

### **Collaborative Design**
- Guru **projects tool** on screen during meeting
- Team discusses and **fills it out together**
- All sections visible at once for context
- No sequential locks - open editing

### **Matches Excel Tool Exactly**
- Same two-page structure
- Same numbered sections [01] [02] [03]
- Same WHY/WHAT/HOW context
- Same add/remove row functionality

### **Fast Track Branding**
- Plaak font for headings (bold, impactful)
- Riforma font for body (clean, readable)
- Black/white/grey color scheme
- Clean, professional worksheet aesthetic

### **Auto-Save**
- Saves to localStorage automatically
- Team can take breaks and resume
- Data persists across sessions

### **Export Functionality**
- Export button generates text summary
- Can be printed for distribution
- Can be shared with team members

---

## 🎨 **VISUAL LAYOUT**

```
┌─────────────────────────────────────────────────────────┐
│  CORE ACTIVITIES          [Core Activities] [Processes] │
│  [MODULE 06 → SPRINT 01]                      [Export]  │
├─────────────────────────────────────────────────────────┤
│                                                         │
│  ┌───────────┐  ┌──────────────────────────────────┐  │
│  │           │  │ [01] Value proposition           │  │
│  │   WHY     │  │ [_____________________________]  │  │
│  │   WHAT    │  │                                  │  │
│  │   HOW     │  │ [02] Brainstorm activities       │  │
│  │           │  │ → [__________________________]   │  │
│  │ (Context) │  │ → [__________________________]   │  │
│  │           │  │ + Add more                       │  │
│  │           │  │                                  │  │
│  │           │  │ [03] Top 5 core activities       │  │
│  │           │  │ → [__________________________]   │  │
│  │           │  │ → [__________________________]   │  │
│  │           │  │ → [__________________________]   │  │
│  │           │  │ → [__________________________]   │  │
│  │           │  │ → [__________________________]   │  │
│  └───────────┘  └──────────────────────────────────┘  │
│                                                         │
└─────────────────────────────────────────────────────────┘
```

---

## 🔄 **COMPARISON**

| Aspect | Old (Typeform) | New (Worksheet) |
|--------|----------------|-----------------|
| **Style** | One question at a time | All sections visible |
| **Use Case** | Individual survey | Team collaboration |
| **Meeting Type** | Pre-work homework | Live facilitated session |
| **Navigation** | Sequential with locks | Tab-based, open editing |
| **Context** | Hidden until step | Always visible (sidebar) |
| **Guru Role** | None (individual tool) | Central (facilitates meeting) |
| **Questions** | 50+ screens | 2 pages |
| **Time** | 30-40 min alone | 90 min team meeting |

---

## 🎯 **WORKFLOW**

### **Before Meeting (Preparation):**
1. Guru shares link to tool
2. Team reviews Brain Juice materials
3. Team thinks about their business

### **During Meeting (90 minutes):**
1. Guru projects tool on screen
2. Guru presents Brain Juice (15 min)
3. Team discusses on **Page 1: Activities**
   - Enter value proposition together
   - Brainstorm activities (all ideas welcome)
   - Discuss and select top 5
4. Team discusses on **Page 2: Processes**
   - Review selected activities
   - Brainstorm processes together
   - Discuss and select top 3
   - Define KPIs together
5. Export final version

### **After Meeting:**
1. Guru exports and shares with team
2. Team uses as reference for execution
3. KPIs tracked in following sprints

---

## 📊 **DATA STRUCTURE**

```javascript
{
  // Page 1
  valueProposition: "string",
  brainstormActivities: ["...", "...", "..."],  // Dynamic array
  coreActivities: ["...", "...", "...", "...", "..."],  // Fixed 5
  
  // Page 2
  brainstormProcesses: ["...", "...", "..."],  // Dynamic array
  coreProcesses: ["...", "...", "..."],  // Fixed 3
  kpis: [
    { name: "...", unit: "%", target: "85" },
    { name: "...", unit: "$", target: "1000" },
    { name: "...", unit: "days", target: "7" }
  ]
}
```

---

## ✅ **WHAT'S WORKING NOW**

1. ✅ **Collaborative worksheet** matches Excel tool
2. ✅ **Two-page structure** (Activities | Processes & KPIs)
3. ✅ **WHY/WHAT/HOW context** always visible
4. ✅ **Add/remove rows** dynamically
5. ✅ **Auto-save** to localStorage
6. ✅ **Export functionality**
7. ✅ **Fast Track branding** (Plaak/Riforma fonts)
8. ✅ **Clean, professional** aesthetic
9. ✅ **Guru-friendly** for facilitation
10. ✅ **Team-friendly** for collaboration

---

## 🎓 **KEY PRINCIPLES FROM GURU GUIDE**

### **Guru Role:**
- **Be the Catalyst** - Ignite sharp thinking
- **Facilitate, Don't Dominate** - Create space for input
- **Stay on Track** - Own the agenda
- **Engage Relentlessly** - Pull in quiet ones, challenge vague answers

### **Tool Usage:**
- Work **directly on the team tool** during discussion
- Keep conversations **laser-focused**
- Push for **specificity** (not vague answers)
- Use **80/20 principle** (if everything is core, nothing is)
- Focus on **customer value**, not internal politics

### **Success Criteria:**
- Team knows which activities matter most - and why
- Understands how activities support value proposition
- Understands difference between activity and process
- Co-created the map together
- Ready to measure what matters

---

## 🚀 **NEXT STEPS**

### **For Testing:**
1. Open tool in browser
2. Fill out Page 1 as a team would
3. Switch to Page 2
4. Verify data flows correctly
5. Test export functionality
6. Try adding/removing rows

### **For Guru Training:**
1. Review Guru Guide PDF
2. Practice facilitating with tool
3. Prepare Zara example presentation
4. Test projection setup
5. Practice keeping team on track

### **For Deployment:**
1. Host on web server
2. Share link with Gurus
3. Use in actual team meetings
4. Collect feedback
5. Iterate based on usage

---

## 💡 **WHY THIS IS BETTER**

### **For Participants:**
- ✅ Can see all sections (not lost in sequential flow)
- ✅ Can refer back to previous sections
- ✅ Context always visible (WHY/WHAT/HOW)
- ✅ Natural discussion flow during meeting
- ✅ Team collaboration, not individual work

### **For Gurus:**
- ✅ Easy to project and facilitate
- ✅ Can see team's progress at a glance
- ✅ Can guide discussion section by section
- ✅ Matches familiar Excel tool structure
- ✅ Export for documentation

### **For Fast Track:**
- ✅ Matches proven workshop methodology
- ✅ Enables collaborative decision-making
- ✅ Follows 80/20 principle correctly
- ✅ Creates team alignment (not individual answers)
- ✅ Professional, premium aesthetic

---

## 🎯 **FINAL VERIFICATION**

Open the tool and verify:
- ✅ Two tabs: "Core Activities" and "Processes & KPIs"
- ✅ Left sidebar shows WHY/WHAT/HOW context
- ✅ Right side shows numbered sections [01] [02] [03]
- ✅ Can add/remove rows in brainstorm sections
- ✅ Data persists when switching tabs
- ✅ Export button generates summary
- ✅ Clean, professional worksheet appearance
- ✅ Plaak font for headings
- ✅ Black/white/grey aesthetic

---

**This is now a proper collaborative team meeting tool! 🎯**


