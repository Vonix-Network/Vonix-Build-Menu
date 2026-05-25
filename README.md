# Vonix Build Menu

A modern, high-performance desktop application interface designed for managing and building multiversion Minecraft server utility mods (Architectury templates). 

The app features a custom frameless desktop wrapper using Python, **FastAPI**, and **PyQt6**, delivering a premium, native-feeling, application-like experience.

---

## 🚀 Key Features

*   **⚡ Modern, Responsive UI/UX**: Built with an elegant, responsive layout optimized for window views (with scroll protection and locked grid layout that prevents UI items from shifting or collapsing).
*   **🔌 Live-Streamed Console**: Standard output streams directly into a customized, scrollable terminal window matching the height of the options pane.
*   **🛠️ Automatic SDK Selection**: Intelligently scans local directories, auto-detects installed Java versions, and configures the exact JDK required for building each Minecraft version (e.g., JDK 17 for `1.18.2` - `1.20.1`, and JDK 21 for `1.21.1`).
*   **📦 Auto-Release Copying**: On a successful build, the app automatically compiles, captures release jars, appends the target Minecraft version to the filename, and organizes them under a unified `releases/` directory.

---

## 🛠️ Tech Stack & Architecture

*   **Core Backend**: Python 3, FastAPI, and WebSocket protocol (for live console logging)
*   **Desktop Wrapper**: PyQt6 & PyQt6-WebEngine (renders local HTML resources inside an elegant, custom-styled titlebar frameless container)
*   **Frontend**: HTML5, Vanilla CSS (CSS Grid, HSL custom palette, and micro-animations), and Vanilla JavaScript
*   **Logger/CLI Formatting**: Rich terminal rendering capabilities (`rich` console integration)

---

## 📦 Installation & Setup

1.  **Clone the Repository**:
    ```bash
    git clone https://github.com/Vonix-Network/Vonix-Build-Menu.git
    cd Vonix-Build-Menu
    ```

2.  **Install Python Dependencies**:
    Make sure you have Python 3.10+ installed. Install the necessary backend and GUI packages using the `requirements.txt` file:
    ```bash
    pip install -r requirements.txt
    ```

3.  **Ensure Java Requirements are Met**:
    Ensure the appropriate Java SDKs are installed on your machine. The build backend automatically scans common installation directories.

---

## 🖥️ Usage

Run the build manager using the native wrapper:
```bash
python gui-build-menu.py
```
*If PyQt6 is not installed, the application will automatically fall back to serving on localhost and launching the menu in your default web browser.*

### Options & Building:
- **Build All**: Automates compiling all versions in series.
- **Specific Version**: Build fabric, forge, or neoforge architectures for a single selected version.
- **Auto-Collector**: Successfully created release jars will be output to a top-level `/releases` directory.
