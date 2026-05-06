# Spatial Web 2526

[IEEE P2874 March 2025]: https://ieeexplore.ieee.org/document/10929711
[Networks and Distributed Systems Laboratory]: https://dcs.upd.edu.ph/research/labs/ndsl
[Department of Computer Science]: https://dcs.upd.edu.ph/
[College of Engineering]: https://coe.upd.edu.ph/
[University of the Philippines]: https://up.edu.ph/
[Diliman]: https://upd.edu.ph/
[Spatial Web Foundation]: https://spatialwebfoundation.org/

Spatial Web 2526 is a project that adapts the [IEEE P2874 March 2025] Draft Standards that describes the concepts of the Spatial Web framework. It was developed in fulfillment for the attainment of the Bachelor of Science degree in Computer Science under the [Networks and Distributed Systems Laboratory] of the [Department of Computer Science], [College of Engineering], [University of the Philippines] [Diliman].

## Project Overview
This project is composed of three repositories:
1. ESP32 BLE Beacon
2. Android Application
3. Spatial Web Server

The **ESP32** BLE Beacon serves as the "starting point" of the connection. It acts as a spatial anchor, corresponding to a room in a building, broadcasting the room's corresponding Spatial Web ID (SWID) via advertisement data.

The Android Application was created using **Kotlin** and it was used to detect the strongest ESP32 BLE beacon in an area. Once detection is complete, it sends its corresponding queries to a UDG Spatial Web server. The server logs (used for analysis) will be saved within the application and can be uploaded to a cloud database (**Supabase**, in this case) for easier data analysis.

The Spatial Web Server encompasses the code for the **FastAPI** backend service used to facilitate the UDG and HSML code and it was first deployed using DigitalOcean droplets. Environment variables can be set to interface whether the Spatial Web Server will act a UDG, HSML, or LLM server. For a Spatial Web Server to also act as a UDG server, it requires the use of a Neo4j instance to also be installed in the server. As a result, the UDG server requires atleast the minimum system requirements needed for Neo4j to run in a [cloud environment](https://neo4j.com/docs/operations-manual/current/installation/requirements/).

## Acknowledgements
The following researchers were involved in this project:
- [Prince Harry U. Quijano](https://github.com/Harry2166)
- [John Ysaac S. Villamil](https://github.com/LigsQt)

The research conducted in this project would not have been possible if it weren't for their research adviser:
- [Dr. Wilson M. Tan](https://dcs.upd.edu.ph/people/wmtan/)

We would also like to thank the people behind the [Spatial Web Foundation] for being the basis of this research study.
