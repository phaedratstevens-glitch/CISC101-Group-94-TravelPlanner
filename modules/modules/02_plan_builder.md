### **Module 2 – Plan Builder (Options → Days)**

Goal: turn candidate activities into balanced daily plans that respect user inputs from Intake while staying easy to render in the “Daily plan” table.

**1. Build candidate pool**

Create a pool of activities near the destination (attractions, restaurants, parks, events).  
Each activity record should include:

- type (culture, food, nature, shopping, leisure)
- indoor / outdoor
- estimated duration (hours)
- cost band: $, $$, $$$
- distance and approximate travel time from lodging or previous stop
- typical opening hours and closed days
- tags for user interests (e.g., “street food”, “museums”, “hiking”)
- optional accessibility and dietary suitability tags

**2. Interpret user inputs**

Use data from Intake:

- Map pace to target daily active time:
  - relaxed: ~5–6 hours of activities
  - balanced: ~7–8 hours
  - fast: ~9–10 hours
- Use interests to prefer matching activities (aim for at least two per day).
- If lodging is unknown, assume a central area.  
- If budget is unknown, use mid-range ($$).  
- If interests are unspecified, mix culture, food, and nature.

Define proximity:

- “near lodging”: within ~20 minutes by walking or short transit.
- “close by”: within ~20 minutes total travel from the previous stop.

**3. Build each day (simple loop)**

For each trip day:

- **Morning**  
  - pick one core activity near lodging, open in the morning, matching at least one interest tag.  
  - add 15–30 minutes of buffer for breakfast and transfer.

- **Midday**  
  - pick one activity close to the morning stop (same district if possible).  
  - ensure convenient lunch options nearby and keep cumulative cost within a reasonable per-day budget envelope.  
  - avoid repeating the exact same theme as morning when other options exist.

- **Afternoon**  
  - pick one activity with a different category (e.g., if morning was “culture” and midday “food”, choose “nature” or “leisure”).  
  - check that opening hours cover the planned time.  
  - if season or destination suggests rain/cold, add one indoor backup activity for this slot.

- **Evening**  
  - choose a restaurant or optional event near the afternoon stop that fits stated budget and dietary preferences.  
  - avoid long cross-city transfers at night; prefer options in the same general area.  
  - if booking is typically required, flag this for the “Quick checks” section (do not simulate reservations).

**4. Keep days realistic**

After selecting slots for a day:

- Estimate total activity time plus buffers; if it exceeds the pace target, remove or mark some stops as optional.  
- Prefer one core activity per time block and only add short “bonus” stops if time clearly allows.  
- If budget is tight or candidate options are limited, prioritize free or low-cost nearby activities that still match interests.

This module produces a structured list of morning, midday, afternoon, and evening entries (plus any marked backups/optional items) that can be passed to Feasibility & Guardrails and then rendered into the final Daily Plan.

