# README for Neo4j Knowledge Management System

## Introduction

This project provides a comprehensive knowledge management system using Neo4j, designed to efficiently capture, manage, and transfer knowledge within an organization. It includes the following components:

* A graph model representing employees, skills, projects, and training sessions.
* Datasets for employees, their skills, projects, and required skills.
* Cypher queries for loading the dataset into Neo4j.
* Advanced Cypher queries for identifying knowledge gaps, recommending skill transfers, and analyzing project success.

## Prerequisites

* Neo4j Desktop or Neo4j Server installed.
* Graph Data Science (GDS) plugin installed in Neo4j.

## Dataset

The dataset consists of the following CSV files:

* `employees.csv`: Employee details (first name, last name, email, experience).
* `employee_skills.csv`: Employee skills and their proficiency levels.
* `projects.csv`: Project details (name, start date, end date, required skills, success).
* `project_participation.csv`: Employee participation in projects.
* `project_required_skills.csv`: Skills required for each project.
* `skill_recommendations.csv`: Skill recommendations between employees.

## Graph Model

* Nodes:

  * `Employee`: Represents an employee with properties (firstName, lastName, email, experience).
  * `Skill`: Represents a skill with the name property.
  * `Project`: Represents a project with properties (name, startDate, endDate, success).

* Relationships:

  * `(:Employee)-[:HAS_SKILL]->(:Skill)`: Represents an employee possessing a skill.
  * `(:Employee)-[:WORKED_ON]->(:Project)`: Represents an employee working on a project.
  * `(:Project)-[:REQUIRES]->(:Skill)`: Represents skills required for a project.
  * `(:Employee)-[:RECOMMENDS_SKILL]->(:Employee)`: Represents a skill recommendation from one employee to another.

## Loading Data into Neo4j

1. Copy all CSV files to the Neo4j import directory.
2. Run the Cypher queries from the "Neo4j Cypher Queries For Knowledge Management" text document in the Neo4j Browser to load the data.

## Advanced Queries

* Identify knowledge gaps in projects.
* Recommend skill transfers between employees.
* Analyze project success based on skill coverage.
* Detect key employees using PageRank (Graph Data Science).

## How to Use

* Use the advanced queries to gain insights into your knowledge graph.
* Adjust the dataset as needed to match your organization's structure.

## Support

If you encounter any issues, please contact your Neo4j administrator or refer to the Neo4j documentation.

