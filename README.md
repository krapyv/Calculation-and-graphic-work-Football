# Java Calculation and Graphics Work

**Football Management Hierarchy System**

## Author
Dmytro Krapyvianskiy

## Overview
A Java Swing desktop application that models a hierarchical football management system with four levels:
- **League** (Level 1)
- **Club** (Level 2)  
- **Amplua/Position** (Level 3)
- **Footballer** (Level 4)

## Features
- **Tree-based hierarchy** visualization using `JTree`
- **CRUD operations** (Add, Edit, Remove) for all entity types
- **Modal dialogs** for data input with validation
- **Serialization** - save/restore tree models to files
- **Event system** with listeners and operation logging
- **Search** - find the most expensive footballer in a subtree
- **Calculate** - count key positions per club
- **Protocol logging** - all operations saved to `RGRLogKrapyvanskyi.txt`

## Technology Stack
- Java (Swing for GUI)
- Serialization for persistence
- Custom event listener pattern

## Project Structure
src/
- model/ # Data entities (League, Club, Amplua, Footballer, AnyData)
- view/ # GUI components (Dialogs, MainGui, Event handling)
- test/ # Test classes

## Key Classes

| Class | Description |
|-------|-------------|
| `AnyData` | Abstract base class for all entities |
| `League` | Top-level node with president, budget, level |
| `Club` | Contains coach, championship position, budget |
| `Amplua` | Football position with main attribute, key position flag |
| `Footballer` | Player details: position, birthday, nationality, transfer value, captain status |
| `MainGui` | Main application window with tree and controls |
| `IDlg` | Interface for all dialog windows |

## Data Validation
- Name fields cannot be empty
- Championship position: 1-16
- Club budget: 5-200 million €
- League budget: 10-800 million €
- Player age: 16-50 years
- Transfer value: 0.4-100 million €
- League level: 1-4

## How to Run
1. Compile all Java files
2. Run `view.MainGui`
3. Use the tree panel to navigate the hierarchy

## Controls
| Button | Action |
|--------|--------|
| Add | Add child node to selected item |
| Edit | Modify selected node |
| Remove | Delete selected node |
| Store | Serialize tree to file |
| Restore | Deserialize tree from file |
| Find/Calculate | Search or calculate statistics |

## Event Logging
All operations are logged to console and `RGRLogKrapyvanskyi.txt` with timestamps.

## Course Context
This project implements a hierarchical data structure with polymorphism, serialization, and event-driven GUI for system modelling coursework.
