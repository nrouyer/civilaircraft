# README for Neo4j Component Shortage Management System

## Introduction

This project provides a comprehensive component shortage management system using Neo4j, designed to efficiently track, manage, and mitigate risks associated with component shortages in products. It includes the following components:

* A graph model representing products, components, suppliers, inventory levels, and demand forecasts.
* Datasets for products, components, suppliers, inventory levels, and shortage risk levels.
* Cypher queries for loading the dataset into Neo4j.
* Advanced Cypher queries for identifying shortages, forecasting risks, and recommending mitigation strategies.

## Prerequisites

* Neo4j Desktop or Neo4j Server installed.
* Graph Data Science (GDS) plugin installed in Neo4j.

## Dataset

The dataset consists of the following CSV files:

* `products.csv`: Product details (name, category, demand forecast).
* `components.csv`: Component details (name, type, inventory level).
* `suppliers.csv`: Supplier details (name, reliability, contact information).
* `product_components.csv`: Mapping of components used in products.
* `component_suppliers.csv`: Mapping of suppliers providing components.
* `shortage_risks.csv`: Shortage risk levels for components.

## Graph Model

* Nodes:

  * `Product`: Represents a product with properties (name, category, demandForecast).
  * `Component`: Represents a component with properties (name, type, inventoryLevel).
  * `Supplier`: Represents a supplier with properties (name, reliability).

* Relationships:

  * `(:Product)-[:USES]->(:Component)`: Represents a product using a component.
  * `(:Component)-[:SUPPLIED_BY]->(:Supplier)`: Represents a supplier providing a component.
  * `(:Component)-[:HAS_RISK]->(:Risk)`: Represents the shortage risk of a component.

## Loading Data into Neo4j

1. Copy all CSV files to the Neo4j import directory.
2. Run the Cypher queries from the "Neo4j Cypher Queries For Component Shortage Management" text document in the Neo4j Browser to load the data.

## Advanced Queries

* Identify components with critical shortages.
* Forecast shortage risks using demand forecasts and inventory levels.
* Recommend mitigation strategies (e.g., alternative suppliers).
* Detect critical suppliers using centrality measures.

## How to Use

* Use the advanced queries to proactively manage component shortages.
* Adjust the dataset as needed to match your organization's structure.

## Support

If you encounter any issues, please contact your Neo4j administrator or refer to the Neo4j documentation.

