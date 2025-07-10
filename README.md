# Telephone Simulation System

A Java-based GUI application that simulates telephone switching operations, including lost call and delay call scenarios. This system provides a visual representation of telephone lines, links, and active connections with real-time simulation capabilities.

## 📋 Table of Contents

- [Features](#features)
- [System Requirements](#system-requirements)
- [Installation](#installation)
- [Usage](#usage)
- [System Architecture](#system-architecture)
- [Simulation Types](#simulation-types)
- [User Interface](#user-interface)
- [Technical Details](#technical-details)
- [Troubleshooting](#troubleshooting)
- [Author](#author)

## ✨ Features

- **Real-time Visual Simulation**: Graphical representation of telephone lines and switching links
- **Two Simulation Modes**:
  - Lost Call Simulation (Erlang-B model)
  - Delay Call Simulation (Erlang-C model)
- **Interactive GUI**: User-friendly interface built with Java Swing
- **Live Connection Tracking**: Real-time display of active connections with color coding
- **Statistical Analysis**: Tracks processed calls, completed calls, blocked calls, and busy signals
- **Multi-line Support**: Simulates up to 8 telephone lines with 3 switching links

## 🖥️ System Requirements

- **Java**: JDK 8 or higher
- **Operating System**: Windows, macOS, or Linux with GUI support
- **Memory**: Minimum 256MB RAM
- **Display**: Minimum 800x600 resolution

## 🚀 Installation

1. **Clone or Download** the project files to your local machine
2. **Navigate** to the project directory:
   ```bash
   cd "Telephone Simulation System"
   ```
3. **Compile** the Java files:
   ```bash
   javac -cp . *.java
   ```
4. **Create** the package structure:
   ```bash
   mkdir -p com/mycompany/tsm
   move *.class com/mycompany/tsm/
   ```
5. **Run** the application:
   ```bash
   java -cp . com.mycompany.tsm.Tsm
   ```

## 🎯 Usage

### Starting the Application

1. Run the main class `Tsm.java`
2. The welcome screen will appear with two simulation options

### Lost Call Simulation

1. Click **"Lost Call"** button from the welcome screen
2. Enter simulation parameters:
   - **From Line**: Source telephone line (1-8)
   - **To Line**: Destination telephone line (1-8)
   - **Call Length**: Duration of the call
   - **Arrival Time**: When the call arrives
3. Click **"Simulate"** to process the call
4. Observe the visual representation and statistics

### Delay Call Simulation

1. Click **"Delay Call"** button from the welcome screen
2. Configure delay simulation parameters
3. Run the simulation to see delay-based call handling

## 🏗️ System Architecture

### File Structure

```
Telephone Simulation System/
├── Tsm.java                 # Main entry point
├── welcome.java             # Welcome screen GUI
├── MainTSM.java            # Lost call simulation
├── Delay.java              # Delay call simulation
├── welcome.form            # Welcome screen form layout
├── MainTSM.form           # Main simulation form layout
├── Delay.form             # Delay simulation form layout
└── README.md              # This documentation
```

### Class Hierarchy

- **`Tsm`**: Main class that launches the application
- **`welcome`**: Welcome screen with simulation mode selection
- **`MainTSM`**: Implements lost call simulation with visual display
- **`Delay`**: Handles delay call simulation scenarios

## 📊 Simulation Types

### Lost Call Simulation (Erlang-B)

- Models telephone systems where blocked calls are lost
- Simulates up to 3 simultaneous connections
- Tracks call statistics: processed, completed, blocked, busy
- Visual representation of active connections

### Delay Call Simulation (Erlang-C)

- Models systems where calls wait in queue when all lines are busy
- Handles call delays and queue management
- Provides delay statistics and performance metrics

## 🎨 User Interface

### Welcome Screen

- **Title**: "Telephone Simulation System"
- **Author**: Nabin Khadka
- **CRN**: 021-342
- **Navigation**: Two buttons for simulation mode selection

### Main Simulation Window

- **Input Panel**: Parameter entry fields
- **Visual Display**: Real-time graphical representation
- **Statistics Panel**: Live call statistics
- **Control Buttons**: Simulation execution controls

### Visual Elements

- **Lines 1-8**: Horizontal telephone lines
- **Links 1-3**: Vertical switching links
- **Active Connections**: Color-coded connection display
  - 🟢 Green: Link 1 connections
  - 🔵 Blue: Link 2 connections
  - 🔴 Red: Link 3 connections

## 🔧 Technical Details

### Key Components

- **Connection Management**: Tracks active calls and link utilization
- **Call Processing**: Handles call arrival, processing, and completion
- **Statistics Engine**: Real-time calculation of system performance
- **Graphics Engine**: Custom paint method for visual representation

### Data Structures

- **`used[][]`**: 2D array tracking active connections
- **`line[]`**: Array representing telephone line status
- **Call Statistics**: Counters for various call states

### Algorithms

- **Call Routing**: Determines available links for connections
- **State Management**: Tracks system state and transitions
- **Collision Detection**: Handles busy lines and blocked calls

## 🛠️ Troubleshooting

### Common Issues

**"Could not find or load main class" Error**

```bash
# Solution: Ensure proper package structure
mkdir -p com/mycompany/tsm
move *.class com/mycompany/tsm/
java -cp . com.mycompany.tsm.Tsm
```

**GUI Not Displaying**

- Ensure Java GUI libraries are available
- Check display settings and resolution
- Verify Java version compatibility

**Paint Method Not Working**

- Ensure graphics are drawn in visible area
- Check color constants (use `Color.GREEN` not `Color.green`)
- Verify component layering and overlap

### Performance Tips

- Use reasonable call lengths to avoid system overload
- Monitor system resources during long simulations
- Restart application if GUI becomes unresponsive

## 📈 Statistics Explained

- **Processed**: Total number of calls that entered the system
- **Completed**: Successfully connected and completed calls
- **Blocked**: Calls rejected due to no available links
- **Busy**: Calls rejected due to busy lines
- **Clock**: Current simulation time
- **In Use**: Number of currently active connections

## 🎓 Educational Use

This simulation system is designed for educational purposes to demonstrate:

- Telephone switching concepts
- Queueing theory (Erlang-B and Erlang-C models)
- Real-time system simulation
- GUI application development in Java
- Statistical analysis of communication systems

## 👨‍💻 Author

**Nabin Khadka**  
CRN: 021-342

## 📝 License

This project is created for educational purposes. Please refer to the license file for usage terms.

## 🤝 Contributing

This is an educational project. If you find issues or have suggestions for improvements, please feel free to contribute by:

1. Reporting bugs
2. Suggesting enhancements
3. Submitting pull requests
4. Improving documentation

## 📞 Support

For technical support or questions about the simulation system, please refer to the course materials or contact the development team.

---

_This Telephone Simulation System provides a comprehensive platform for understanding telecommunication switching concepts through interactive visualization and real-time simulation._
