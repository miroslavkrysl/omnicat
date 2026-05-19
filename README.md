# omnicat

Note-oriented life organizer: **note-taking**, **calendar** and **chat**, with an emphasis on effortless search and organization, security, decentralization, and collaboration.

> [!CAUTION]
> WIP - this project is in very early work-in-progress, see [project roadmap](#project-roadmap) for list of implemented and planned features. 

## Vision & Principles

- Main purpose of this application:
  1. **Note-taking**
  2. **Calendar events/reminders**
  3. **Chat**
- _Note-oriented_
  - The main domain concept is a note - called **Note** - whether it is a note, event or chat message
  - Every **Note** is a part of a continuous stream - called **Channel**
  - There is no other structure or hierarchy
- _Powerful searching_
  - Fulltext search
  - Tag-based categorization by topics
  - Searching presets
- _Decentralized_
  - The data can live on multiple clients
  - There is no central server or authority
  - Every client is independent and can act on its own
  - Clients synchronize data between themselves to be up to date
  - Potential conflicts are resolved deterministically or manually by user
- _Local-first_
  - The application works regardless of network connectivity
  - Every client possesses all the data including history
- _Collaborative_
  - Data of one user can be shared with others for reading as well as for modification
- _Encrypted_
  - All data stored on client devices are encrypted
  - All communication between clients is end-to-end encrypted
- _Multiplatform_
  - Desktop & mobile
- _Simple & Intuitive_
  - Simple and understandable concepts
  - Clean and intuitive UI
  - [Less is more](https://en.wikipedia.org/wiki/Less_is_more), [worse is better](https://en.wikipedia.org/wiki/Worse_is_better)

## Architecture

This outlines the architecture used for this project, viewed from multiple levels.

### Code

The code adheres the principles of [clean architecture](https://blog.cleancoder.com/uncle-bob/2012/08/13/the-clean-architecture.html) while maintaining the Java/Spring-like component oriented design for services and their interfaces.
This enables a decent level of complexity, modularity and testability.

## Technology Stack

- Rust language for everything possible
- Dioxus for UI ([https://dioxuslabs.com](https://dioxuslabs.com))
- Iroh for P2P networking ([https://www.iroh.computer](https://www.iroh.computer))
- Automerge for [CFRD structures](https://en.wikipedia.org/wiki/Conflict-free_replicated_data_type) ([https://automerge.org/](https://automerge.org/))
- Turso for local data storage, indexing and searching ([https://github.com/tursodatabase/turso](https://github.com/tursodatabase/turso)) 
    - Encryption at rest
    - Indexing, searching, fulltext searching by [using Tantivy](https://github.com/tursodatabase/turso/blob/main/docs/fts.md) internally

- age for file + network messages encryption ([https://github.com/C2SP/C2SP/blob/main/age.md](https://github.com/C2SP/C2SP/blob/main/age.md), [https://github.com/str4d/rage](https://github.com/str4d/rage))

## Project Roadmap

This roadmap outlines the planned and completed features for **omnicat** life organizer.

### **Done**
![nothing](https://www.meme-arsenal.com/memes/c087580f123e0dbcd96faf1aec85e9b2.jpg)

### **WIP**
- Channels with plain text notes
- Local storage for channels and notes
- Desktop application for Linux with GUI

## License

Copyright © 2026 Miroslav Krýsl <mkrysl@proton.me>.

This project is licensed exclusively under the GNU Affero General Public License v3.0 (AGPL-3.0-only).

The full license text is available in the [`LICENSE`](LICENSE) file included in this repository.
