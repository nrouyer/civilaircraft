# README for Neo4j Obsolescence Management System

## Introduction

This project provides a robust obsolescence management system using Neo4j, designed to efficiently track, manage, and mitigate obsolescence risks in products, components, and skills. It includes the following components:

* A graph model representing products, components, suppliers, and lifecycle stages.
* Datasets for products, components, suppliers, and obsolescence risk levels.
* Cypher queries for loading the dataset into Neo4j.
* Advanced Cypher queries for identifying obsolete components, predicting obsolescence, and recommending alternatives.

## Prerequisites

* Neo4j Desktop or Neo4j Server installed.
* Graph Data Science (GDS) plugin installed in Neo4j.

## Dataset

The dataset consists of the following CSV files:

* `products.csv`: Product details (name, category, launch date, status).
* `components.csv`: Component details (name, type, lifecycle stage).
* `suppliers.csv`: Supplier details (name, reliability, contact information).
* `product_components.csv`: Mapping of components used in products.
* `component_suppliers.csv`: Mapping of suppliers providing components.
* `obsolescence_risks.csv`: Obsolescence risk levels for components.

## Graph Model

* Nodes:

  * `Product`: Represents a product with properties (name, category, launchDate, status).
  * `Component`: Represents a component with properties (name, type, lifecycleStage).
  * `Supplier`: Represents a supplier with properties (name, reliability).

* Relationships:

  * `(:Product)-[:USES]->(:Component)`: Represents a product using a component.
  * `(:Component)-[:SUPPLIED_BY]->(:Supplier)`: Represents a supplier providing a component.
  * `(:Component)-[:HAS_RISK]->(:Risk)`: Represents the obsolescence risk of a component.

## Loading Data into Neo4j

1. Copy all CSV files to the Neo4j import directory.
2. Run the Cypher queries from the "Neo4j Cypher Queries For Obsolescence Management" text document in the Neo4j Browser to load the data.

## Advanced Queries

* Identify obsolete or at-risk components.
* Predict obsolescence using lifecycle stages and supplier reliability.
* Recommend alternative components to avoid obsolescence.
* Detect critical suppliers using centrality measures.

## How to Use

* Use the advanced queries to proactively manage obsolescence.
* Adjust the dataset as needed to match your organization's structure.

## Support

If you encounter any issues, please contact your Neo4j administrator or refer to the Neo4j documentation.

