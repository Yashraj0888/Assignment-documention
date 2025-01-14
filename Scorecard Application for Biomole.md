# Scorecard Application for Biomolecule Analysis - Requirements Document

## 1. Introduction
This document outlines the requirements for a scorecard application designed to assist scientists in analyzing biomolecules, primarily antibodies. The application aims to provide a clear overview of key properties and enable detailed visualization of 3D molecular structures.

## 2. Goals
- Provide a dynamic scorecard of biomolecule properties with visual indicators of acceptable ranges.
- Integrate a 3D molecular visualization component for in-depth analysis.
- Enable users to correlate molecular structure with specific properties.
- Develop a reusable component applicable to various biomolecules.

## 3. Target Users
Scientists and researchers involved in biomolecule development and analysis.

## 4. Functional Requirements
### 4.1. Scorecard Table
- The application shall fetch biomolecule property data from a provided API.
- The application shall display the data in a tabular format, with each row representing a biomolecule and each column representing a property.
- The application shall visually indicate (using color coding: green, amber, red) whether each property falls within predefined acceptable ranges. Green indicates a good range, amber a borderline range, and red a problematic range.
- The table shall be dynamic, updating based on the data retrieved from the API.

### 4.2. 3D Molecular Visualization
- The application shall integrate the Mol* JavaScript library for 3D molecular visualization.
- Each row in the scorecard table shall have a "view structure" button.
- Clicking the "view structure" button shall open a panel displaying the 3D structure of the corresponding biomolecule.
- The application shall retrieve the biomolecule's PDB (Protein Data Bank) file from a provided API.

### 4.3. Property-Based Coloring
- The application shall allow users to color the 3D molecular structure based on different properties.
- The available properties for coloring shall be derived from a provided JSON file containing residue-specific property values.
- The application shall provide a user interface (e.g., dropdown menus) to select the property for coloring.
- The application shall use Mol*'s API to color the 3D structure according to the selected property and its corresponding values for each residue.

### 4.4. API Integration
- The application shall integrate with the following provided APIs:  
  - API for fetching scorecard table data.  
  - API for retrieving biomolecule structures in PDB format.  
  - API for retrieving residue-specific property values in JSON format.
- API documentation will be provided.

## 5. Non-Functional Requirements
- **Performance**: The application shall load and render data efficiently.
- **Usability**: The application shall have a clear and intuitive user interface.
- **Reusability**: The visualization component shall be designed as a reusable component applicable to various biomolecules, not just antibodies.
- **Maintainability**: The codebase shall be well-structured and documented.
- **Technology**: The application shall be developed using appropriate web technologies, including React and the Mol* JavaScript library.
- **Component Repository**: The visualization component will be checked into a specified NPM repository.

## 6. Out of Scope
- Biomolecule optimization. The application provides visualization and data but does not perform any calculations or modifications to the biomolecules themselves.

## 7. Data Format
- **Scorecard Data**: Data will be provided via API in a format suitable for tabular display.
- **Protein Structure**: PDB (Protein Data Bank) format.
- **Residue Properties**: JSON format containing residue indices and their corresponding property values.

## 8. User Interface (UI)
- The UI shall consist of a scorecard table and a visualization panel.
- The visualization panel shall include controls (e.g., dropdown menus) for selecting the property to be used for coloring the 3D structure.

## 9. Open Issues/Questions
- Specific details of the data formats provided by the APIs.
- Exact method of interaction with Mol*'s API for property-based coloring.
- Final decision on team formation and task assignments.

## 10. Future Considerations
- Integration of a sequence visualizer.
- Further enhancements to the visualization capabilities.

## 11. Timeline
- **Initial understanding and experimentation with Mol***: Weekend.
- **Development and implementation**: Following week.
- **Intermediate feedback session**: Mid-week.
- **Target completion**: End of the following week.
