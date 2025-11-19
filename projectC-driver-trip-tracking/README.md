🛣️ Driver Trip Tracking — AI-Augmented PM Workflow
---------------------------------------------------
A real-world project demonstrating how AI can transform ambiguous field data into structured, actionable project information.

This system takes messy driver trip logs (voice notes, text dumps, shorthand updates) and converts them into a clean, structured trip report — ready for dashboards, task planning, and operations optimization.

This project showcases:

1.Prompt engineering

2.PM workflow design

3.Data structuring

4.AI-assisted requirement extraction

5.Practical business use cases

📌 Problem Statement
---------------------------------------------------
Transportation teams often receive updates in inconsistent formats:

1.Drivers send WhatsApp voice notes

2.Field staff send scattered text messages

3.Trip details are incomplete or unclear

4.PMs waste time manually interpreting and documenting data

This leads to:

1.Poor visibility

2.Errors in billing

3.Miscommunication

4.Missing trip metadata

5.Slow reporting

🎯 Objective
---------------------------------------------------
Create an AI-powered workflow that:

1.Converts unstructured driver input → structured JSON

2.Identifies missing details

3.Estimates unclear values

4.Standardizes trip format

✨ Key Features
---------------------------------------------------
AI-based trip interpretation
Converts messy driver notes into a clean, structured trip report.

Automatic field extraction
Distance, start/end time, locations, issues, delays, expenses.

Error + missing info detection
Flags unclear or incomplete entries.

Standardized JSON output
Ready for dashboards, billing, or PM tools.

Reusable prompt workflow
Consistent outputs across different trip types.

Extendable for future automation
(e.g., auto-logging into Google Sheets, Notion, or dashboards)

🏗️ Technical Architecture
---------------------------------------------------
The system follows a simple but scalable pipeline:

Driver Input (Text/Voice Transcribed)
            ↓
   AI Prompt Processor
            ↓
 Structured Trip JSON
            ↓
 Validation Layer
            ↓
 Final Trip Summary Output


Produces clean outputs for dashboards or downstream tools

Components
---------------------------------------------------
Prompts Folder (/prompts)
Contains the main trip extraction prompt and test inputs.

Notebook (/notebooks/driver_trip_processor.ipynb)

Loads sample driver inputs

Sends them to the AI model

Displays structured output

Validates missing fields

Samples Folder (/samples)
Contains example inputs and processed outputs.

README (this file)
Documentation explaining system, logic, workflows, and usage.

🧩 Installation
-----------------------------------------------------------
1. Clone the Repository
   
   git clone https://github.com/<your-username>/prompt-pm-portfolio.git
cd prompt-pm-portfolio/projectC-driver-trip-tracking

2. Install Python Dependencies

If you run the notebook:

pip install -r requirements.txt

3. Open the Notebook
jupyter notebook notebooks/driver_trip_processor.ipynb

4. Add Your Own Driver Inputs

Place them into:

/samples/inputs/

🔧 How It Works — Processing Pipeline
------------------------------------------------------
1. Input Collection  
   User uploads raw driver trip text files into /samples/inputs/

2. Pre-Processing  
   The notebook cleans text, removes noise, standardizes format.

3. LLM Extraction  
   A structured prompt extracts:
   - Trip start / end  
   - Pickup & dropoff  
   - Distance  
   - Issues / flags  
   - Driver notes

4. Validation Layer  
   Additional prompts verify:
   - Date/time format  
   - Missing fields  
   - Contradicting statements  

5. Output Generation  
   The system produces:
   - Clean JSON  
   - CSV summary  
   - A trip timeline
     
📂 Example Input (from /samples/inputs)
--------------------------------------------------
Driver: Ramesh
Trip: 12 Nov 2025
From: Whitefield
To: Indiranagar
Notes: Traffic heavy, took alternate route.

📂 Example Output (AI-Generated)
---------------------------------------{
  "driver": "Ramesh",
  "date": "2025-11-12",
  "start": "Whitefield",
  "end": "Indiranagar",
  "distance_km": 9.7,
  "issues": ["Heavy traffic"],
  "flags": ["Route deviation"],
  "notes": "Driver took alternate route due to congestion."
}

🧠 Prompt Templates
--------------------------------------
Located in:

/projectC-driver-trip-tracking/prompts/


Includes:

1.extraction.prompt.txt

2.validation.prompt.txt

3.summarisation.prompt.txt

⭐ Why This Project Matters
-----------------------------------------------
This project demonstrates REAL PM + prompt-engineering capability, including:

1.ability to break real workflows into structured systems

2.designing multi-step AI pipelines

3.building validation logic

4.converting messy user input into usable data

5.thinking like a PM while executing like a prompt engineer

6.Recruiters love this because it solves a real business problem with end-to-end technical clarity.
