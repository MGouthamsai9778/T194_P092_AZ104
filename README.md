# Azure Blob Index Tags for Large-Scale Data Organisation

## Abstract

This project focuses on using Azure Blob Index Tags to efficiently organise and discover large volumes of data stored in Azure Blob Storage.

Traditional methods require scanning of entire files and storage, which becomes time-consuming and inefficient as the amount of data increases. The proposed system uses metadata-based index tags to classify blobs based on attributes such as file type, department, category, or status.

This enables fast and targeted blob discovery without performing full storage file searches. Overall, the solution improves data organisation, search efficiency, and scalability for large-scale storage environments.

## Problem Statement

Managing and searching a large number of blobs in Azure Blob Storage can become difficult and time-consuming.

Traditional methods may require scanning the entire storage space to locate specific files. This project uses Azure Blob Index Tags to organise blobs using metadata and enable fast and efficient data discovery without scanning the complete files.

## Objectives

- To organise large-scale blob data using index tags.
- To enable metadata-based searching and filtering of blobs.
- To reduce the need for full container enumeration.
- To improve the speed and efficiency of data discovery.
- To study the limitations of Azure Blob Index Tags.
- To understand the performance challenges when applying tags to existing blobs.

## Use Cases

- Enterprise data management
- Financial systems
- Healthcare systems
- E-commerce
- Backup systems

## Requirements

- Azure account with Azure Blob Storage
- Storage account with a Blob Container
- Azure Portal
- Web browser for managing and searching blobs

## Project Architecture

```text
                 +----------------------+
                 |      USER / ADMIN    |
                 +----------+-----------+
                            |
                            | Upload / Search Request
                            v
                 +----------------------+
                 |  Web Application /   |
                 |        API           |
                 +----------+-----------+
                            |
                            v
             +----------------------------------+
             |       AZURE BLOB STORAGE          |
             |                                  |
             |    +--------------------------+  |
             |    |    STORAGE CONTAINER     |  |
             |    |                          |  |
             |    |  Documents               |  |
             |    |  Images                  |  |
             |    |  Videos                  |  |
             |    |  Reports                 |  |
             |    +------------+-------------+  |
             |                 |                |
             |                 v                |
             |    +--------------------------+  |
             |    |     BLOB INDEX TAGS      |  |
             |    |                          |  |
             |    | Type       = PDF         |  |
             |    | Department = CSE         |  |
             |    | Year       = 2026        |  |
             |    | Status     = Active      |  |
             |    +------------+-------------+  |
             +-----------------+----------------+
                               |
                               v
                 +----------------------+
                 |   TAG-BASED SEARCH   |
                 |     & FILTERING      |
                 +----------+-----------+
                            |
                            v
                 +----------------------+
                 |   MATCHING BLOBS /   |
                 |    SEARCH RESULTS    |
                 +----------------------+
