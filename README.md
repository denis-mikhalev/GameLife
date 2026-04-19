# 🧬 Conway's Game of Life

[![C#](https://img.shields.io/badge/C%23-239120?style=for-the-badge&logo=csharp&logoColor=white)](https://learn.microsoft.com/en-us/dotnet/csharp/)
[![.NET Framework](https://img.shields.io/badge/.NET%20Framework-512BD4?style=for-the-badge&logo=dotnet&logoColor=white)](https://dotnet.microsoft.com/)
[![WPF](https://img.shields.io/badge/WPF-0078D4?style=for-the-badge&logo=windows&logoColor=white)](https://learn.microsoft.com/en-us/dotnet/desktop/wpf/)
[![Platform](https://img.shields.io/badge/Platform-Windows-0078D4?style=for-the-badge&logo=windows&logoColor=white)](https://www.microsoft.com/windows)
[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg?style=for-the-badge)](LICENSE)

A desktop implementation of **Conway's Game of Life** built with WPF and C#. Watch emergent complexity arise from three simple rules on a 90×90 interactive grid.

---

## Preview

> 📸 _Add a GIF or screenshot here — record your screen with [ScreenToGif](https://www.screentogif.com/) (free), save as `assets/demo.gif`, then replace this line with:_
> `![Demo](assets/demo.gif)`

---

## Rules of Life

| Rule | Condition | Result |
|------|-----------|--------|
| Birth | Dead cell with exactly **3** live neighbors | Cell becomes **alive** |
| Survival | Live cell with **2 or 3** live neighbors | Cell **stays alive** |
| Death | Any other case | Cell **dies** |

Three rules. Infinite complexity.

---

## Features

- **90 × 90 grid** — 8,100 individually rendered cells
- **Random fill** — populate the board with a random 50/50 alive/dead state
- **Manual drawing** — click any cell to bring it to life
- **Start / Stop** — toggle real-time simulation at 500 ms per generation
- **Clear** — reset the entire grid instantly
- **Async simulation loop** — UI stays fully responsive during evolution (`async/await` + `Task.Delay`)
- **Correct double-buffering** — next generation is computed from a snapshot, preventing mid-frame state corruption

---

## Getting Started

### Prerequisites

- Windows OS
- [Visual Studio 2019 or later](https://visualstudio.microsoft.com/) with **.NET desktop development** workload

### Run

```bash
git clone https://github.com/<your-username>/GameLife.git
cd GameLife
```

1. Open `WpfApp21/WpfApp21.sln` in Visual Studio
2. Press **F5** to build and run

No NuGet packages. No external dependencies. Builds out of the box.

---

## Tech Stack

| Technology | Role |
|------------|------|
| **C#** | Application logic |
| **WPF** | UI framework (XAML + code-behind) |
| **.NET Framework** | Runtime |
| **async / await** | Non-blocking simulation loop |

---

## Project Structure

```
GameLife/
├── WpfApp21/
│   ├── WpfApp21.sln
│   └── WpfApp21/
│       ├── MainWindow.xaml       # Grid UI + toolbar
│       ├── MainWindow.xaml.cs    # Game logic (neighbor counting, simulation loop)
│       ├── App.xaml / App.xaml.cs
│       └── Properties/
├── LICENSE
├── .gitignore
└── README.md
```

---

## License

This project is licensed under the [MIT License](LICENSE).