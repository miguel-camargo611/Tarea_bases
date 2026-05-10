# Universal Studios Colombia — NoSQL Data Lake

Names: Miguel Camargo, Nicolas Cardenas and Camilo Hernandez

## Project Overview

This project was developed as part of a practical workshop focused on NoSQL databases using MongoDB. The objective was to design and implement a Data Lake for an online music store managed by Universal Studios Colombia.

The database was modeled using a document-oriented approach where each music album is represented as an independent MongoDB collection and each song is stored as a document inside its corresponding collection.

The project includes albums and songs from the following artists:

- Lady Gaga
- Diomedes Díaz
- BTS
- Michael Jackson
- Queen
- Ivy Queen

---

# Repository Branches

## `main`
Contains the deliverables for Task 1:

- Initial database creation
- Album collections
- Song documents
- BSON exports
- CSV exports
- Album cover images

## `actualizaciones`
Contains the deliverables for Task 2:

- Additional songs inserted into album collections
- Updated BSON exports
- Updated CSV exports

## `eliminaciones`
Contains the deliverables for Task 3:

- Deletion of songs from collections
- Deletion of one complete artist collection
- Final BSON and CSV exports

---

# Tasks Summary

## Task 1 — Initial Database Creation

For the first task, a MongoDB database was created containing at least one album for each required artist. Each album was represented as a collection and each song was stored as a document with a unique identifier.

The following required fields were included:

- `_id`
- `titulo`
- `anio_salida`
- `autor`
- `id_imagen_portada`

Additional optional fields were also added to improve the structure of the data model, including:

- `album`
- `album_id`
- `genero`

The task also included exporting the database into CSV and BSON formats and organizing album cover images inside the repository.

---

## Task 2 — Album Updates

In the second task, additional less-known songs were inserted into each album collection.

After updating the collections:

- Data integrity was verified
- BSON files were updated
- CSV exports were regenerated

This task demonstrated how MongoDB collections can be easily expanded without modifying rigid relational schemas.

---

## Task 3 — Record Deletion

In the third task, at least two songs were deleted from each album collection. Additionally, one complete artist collection was removed from the database.

After the deletions:

- Database integrity was verified
- Final BSON exports were generated
- Updated CSV exports were created

This task helped demonstrate document deletion operations and collection management in MongoDB.

---

# Data Model Structure

## Database Design

The project follows the following NoSQL modeling rules:

- Each album is represented as a MongoDB collection
- Each song is represented as a MongoDB document
- Each song document contains a unique `_id`
- Album information is identified using `album_id` and `album`

---

## Example Document Structure

```json
{
  "_id": 1,
  "album_id": "queen_opera_1975",
  "album": "A Night at the Opera",
  "titulo": "Bohemian Rhapsody",
  "anio_salida": 1975,
  "autor": "Queen",
  "genero": "Rock",
  "id_imagen_portada": "img/opera.jpg"
}
```

---

# Repository Structure

```plaintext
Tarea_bases/
│
├── BSON_Coleccion/
├── BSON_documentos/
├── img/
├── csv_global.csv
└── README.md
```

---

# Design Decisions

The team decided to model each album as an independent MongoDB collection to follow the workshop requirements and better understand document-oriented database structures.

Additional fields such as `album_id`, `album`, and `genero` were included to improve data organization and simplify global CSV exports.

Album cover images were stored separately inside the `img/` folder while the database only stores the relative path to each image.

---

# Findings and Learning Outcomes

During the development of the project, the team learned several important concepts related to NoSQL databases and MongoDB.

Some interesting findings include:

- MongoDB allows flexible document structures without requiring rigid schemas
- BSON exports preserve MongoDB-specific data formats
- Collections can be expanded easily by adding new documents
- CSV exports are useful for data visualization and interoperability
- GitHub branch management helps organize project stages efficiently

Some difficulties encountered during the project included:

- Organizing BSON exports for individual documents
- Structuring global CSV exports
- Managing consistent identifiers across collections

---

# How to Replicate the Project

## Requirements

- MongoDB
- MongoDB Compass
- Git
- GitHub account

---

## Basic Steps

1. Clone the repository:

```bash
git clone <repository-url>
```

2. Open MongoDB Compass.

3. Import the BSON collection files into MongoDB.

4. Verify the collections and documents.

5. Explore the database structure and exported files.

---

# Technologies Used

- MongoDB
- MongoDB Compass
- GitHub
- CSV
- BSON

---

# Final Notes

This project was created for educational purposes as part of the Universal Studios Colombia NoSQL workshop. The main objective was to understand NoSQL database modeling, document-oriented structures, and data management using MongoDB.
