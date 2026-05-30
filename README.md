# 🖋️ Tattoo Studio — Client Management System

> A C++ OOP project implementing a client management system for a tattoo studio, demonstrating core object-oriented programming concepts.

---

## 📌 Description

A console-based C++ application that models a tattoo studio's client database. It demonstrates class hierarchies, operator overloading, generic templates, and binary file serialization — built as an academic OOP exercise.

---

## 🧩 Class Structure

```
client  (base class)
├── tatuajFinalizat   (completed tattoo)
└── tatuajProgramat   (scheduled tattoo)

listaClienti<T>       (generic template list)
```

### `client` (base class)
| Field | Type | Description |
|---|---|---|
| `nume` | `string` | Client name |
| `idClient` | `int` | Client ID |
| `idTatuaj` | `int` | Tattoo ID |
| `pretTatuaj` | `int` | Tattoo price |

### `tatuajFinalizat` : `client`
Extends `client` with a `bool final` flag indicating whether the tattoo session is completed.

### `tatuajProgramat` : `client`
Extends `client` with a `bool programat` flag indicating whether the appointment is scheduled.

### `listaClienti<T>` (template)
Generic vector-based list supporting `+=`, `-=`, `[]`, and binary serialization.

---

## ⚙️ Features Demonstrated

| Concept | Implementation |
|---|---|
| Constructors | Default, parameterized, copy |
| Inheritance | `tatuajFinalizat`, `tatuajProgramat` extend `client` |
| Polymorphism | `virtual display()` / `virtual read()` overridden in subclasses |
| Operator overloading | `=`, `==`, `<<`, `>>`, `+=`, `-=`, `[]` |
| Templates | `listaClienti<T>` works with any client type |
| STL | `std::vector`, `std::find` |
| File I/O | Binary serialization / deserialization with `fstream` |
| Getters & Setters | Full encapsulation on all private fields |

---

## 🛠️ Build & Run

```bash
g++ -o studio main.cpp
./studio
```

Or open in Visual Studio / any C++ IDE and run directly.

---

## 🗂️ Project Structure

```
📁 tattoo-studio/
├── main.cpp                    # Full source code
└── fisierListaClienti.bin      # Generated binary file (after first run)
```

---

*Academic C++ OOP project*
