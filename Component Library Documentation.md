# Component Library Documentation

## Introduction
The Component Library is designed to provide a modular and extensible framework for visualizing and annotating data in web applications. It aims to facilitate collaboration between AI tools and human users by allowing for interactive data exploration and annotation.

## Architecture Overview
The architecture of the Component Library is based on the following key principles:

- **Modularity**: Each component is self-contained and can be used independently or in combination with others.
- **Extensibility**: New components can be added without modifying existing code.
- **Configurability**: Components can be configured through JSON metadata to accommodate various use cases.

## Components

### Authentication Components
The library includes authentication components to manage user access and sessions:

- **Username and Password Authentication**: Standard login mechanism.
- **OTP Authentication**: One-time password authentication via email for enhanced security.

### Generic Component System
This system allows developers to create and manage visual components:

- **Data Types**: Support for various data types including: 
  - CSV
  - JSON
  - Text
  - Graphs
- **Display Types**: Components can render data in multiple formats: 
  - **Table**: Displays data in a tabular format.
  - **Card List**: Displays data as a list of cards.
  - **Graph/Chart**: Visualizes data as graphs or charts.
- **Composite Widgets**: Ability to combine multiple components into a single widget for complex visualizations.

### Annotation Support
The library supports annotation features, allowing users to:

- Comment on specific data points or visualizations.
- Add tags or notes to annotations.
- Edit or delete existing annotations.
- Store annotations persistently on the server.

## Usage

### Installation
To install the Component Library, run the following command:

```bash
npm install component-library
```

### Configuration
To configure the library, you will need to set up the following:

- **Authentication**: Configure the authentication method (username/password or OTP) in the application settings.
- **Data Sources**: Define the data sources that the components will consume.
- **Component Registration**: Register components in your application using the provided API.

### Example Usage
Here’s a simple example of how to use the library in a React application:

```javascript
import React from 'react';
import { TableComponent, CardListComponent, AuthComponent } from 'component-library';

const App = () => {
    return (
        <div>
            <AuthComponent />
            <TableComponent data={tableData} />
            <CardListComponent data={cardData} />
        </div>
    );
};

export default App;
```

## Guidelines for New Components
When adding new components to the library, please adhere to the following guidelines:

- Ensure the component is modular and reusable.
- Provide clear documentation for the component, including usage examples.
- Write unit tests to cover the functionality of the component.
- Follow the existing code style and conventions used in the library.

