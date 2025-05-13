# System Patterns

This document outlines the system architecture and key technical decisions for the Full-Stack Developer Training project.

**Architecture:** The project follows a modular structure, with distinct directories for course content (`curso_full_stack`) and agent memory (`memory_bank`).

**Key Technical Decisions:**
- Utilize Markdown files for course content and memory bank for ease of reading and editing.
- Use a JSON file (`cursos.json`) as a structured index for available courses.
- Leverage available tools for file manipulation, command execution, and information retrieval.

**Design Patterns in Use:**
- **Modular Design:** Organizing content and memory into distinct, manageable units.

**Component Relationships:**
- The agent (`Roo`) interacts with the file system to read/write content and manage the memory bank.
- The `guia.md` file provides core instructions for the agent.
- The `cursos.json` file provides metadata about the available courses.
- The `curso_full_stack` directory contains the actual training materials.
- The `memory_bank` directory stores the agent's operational memory.

**Critical Implementation Paths:**
- Reading and interpreting the `guia.md` and memory bank files at the start of each task.
- Accurately updating the `progress.md` file to track student progress.
- Correctly locating and utilizing course content within the `curso_full_stack` directory.
