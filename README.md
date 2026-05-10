# Universal Studios Colombia — NoSQL Data Base

Names: Miguel Camargo, Nicolas Cardenas, Camilo Hernandez

## Project Overview

This project was developed as part of a practical MongoDB workshop focused on NoSQL database modeling and data lake construction for an online music store managed by Universal Studios Colombia.

The objective of the project was to design and implement a document-oriented database using MongoDB, where each music album is represented as an independent collection and each song is stored as a document within its corresponding album collection.

The database includes albums and songs from international and Latin American artists from different musical genres.

Artists included in the project:

- Lady Gaga
- Diomedes Díaz
- BTS
- Michael Jackson
- Queen
- Ivy Queen

---

# Data Model Structure

## Database Design

The project follows the following NoSQL modeling rules:

- Each album is represented as a MongoDB collection.
- Each song is stored as a MongoDB document.
- Every song document contains a unique `_id`.
- Album information is additionally identified using `album_id` and `album` fields.

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

