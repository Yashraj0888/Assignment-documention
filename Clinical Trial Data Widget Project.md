## Clinical Trial Data Widget Project 

**Goal:** Build a reusable widget displaying clinical trial data from public APIs.

**Evaluation:**

* **Code:** Well-structured, maintainable, and efficient.
* **UX:** Intuitive interface, easy navigation, and clear data presentation.
* **Reusability:** Easily integrates into other projects.

**Part 1: Core Table (Focus)**

**Data Source:** ClinicalTrials.gov API (RESTful)

**Functionality:**

* Retrieve data for specific diseases (asthma, hydrogenitis operativa, etc.).
* Display data in a table with selectable columns:
    * **Study Title** (linked to ClinicalTrials.gov details)
    * **NCT Number** (unique trial identifier)
    * **Status** (Recruiting, Completed, etc.)
    * **Conditions** (disease studied)
    * **Intervention** (drug/treatment tested)
    * **Sponsor** (funding organization)
* Implement filtering and sorting for:
    * Status
    * Date Posted (e.g., 2021-2023)
    * Phase (e.g., Phase 2) (**Missing feature, desired improvement!**)
* Sticky column headers: Study Title remains fixed when scrolling horizontally.

**Technical Details:**

* API access via RESTful endpoints (e.g., `clinicaltrials.gov/api/v2/query?cond=asthma&count=true`).
* Study Title hyperlinks constructed with NCT ID (`clinicaltrials.gov/study/NCT[NCTID]`).

**UX Emphasis:** Enhance the user experience beyond replicating ClinicalTrials.gov. Explore creative solutions for data visualization and interaction. Table view is a starting point, but other visualizations are welcome.

**Part 2: Enrichment with Open Targets (Future)**

**Data Source:** Open Targets Platform (GraphQL API)

**Goal:** Add three columns to the table:

* **Target** (gene/protein drug interacts with)
* **Modality** (drug type, e.g., small molecule)
* **Mechanism of Action (MOA)** (how the drug works)

**Functionality:**

* Use drug name (from ClinicalTrials.gov) .
* Extract Target, Modality, and MOA from the Open Targets response.
* Integrate these data points into the existing table.

**Technical Details:**

* Open Targets uses a GraphQL API (example query provided by speaker).

**Focus:** Part 1 prioritizes building the core table functionality. Part 2 enhances the table with additional data in the future.

**Overall:** This project focuses on creating a user-friendly and reusable widget that displays clinical trial data effectively. Code quality, usability, and reusability are key, alongside creative UX/UI solutions.
