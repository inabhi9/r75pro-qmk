# RK R75 Pro QMK Firmware

## Description

This project manages the QMK firmware for the RK R75 Pro keyboard. It provides a streamlined development environment using [Devbox](https://www.jetify.com/devbox) for easy setup and compilation of the firmware with all required dependencies.

The firmware is built on top of [QMK Firmware](https://qmk.fm), which is a keyboard firmware based on the TMK keyboard firmware with support for various microcontrollers and advanced features.

## Quick Start

### Prerequisites

- [Devbox](https://www.jetify.com/devbox) installed on your system

### Setup

To set up the development environment and initialize the QMK firmware:

```bash
devbox run setup
```

This command will:
1. Clone the QMK firmware repository from `hangshengkeji/qmk_firmware`
2. Initialize the QMK environment
3. Link the RK R75 Pro keyboard configuration from `src/keyboards/rk/r75_pro` into the QMK firmware directory

### Compile Firmware

To compile the firmware for the RK R75 Pro keyboard:

```bash
devbox run qmk-compile
```

This will compile the firmware using the default keymap and output the compiled binary.

## Project Structure

```
.
├── devbox.json              # Devbox configuration with setup and build scripts
├── README.md               # This file
├── qmk_firmware/           # QMK firmware repository (generated during setup)
└── src/keyboards/          # Custom keyboard configurations
    └── rk/r75_pro/         # RK R75 Pro keyboard files
```

## Available Commands

The following commands are available through Devbox:

- **`devbox run setup`** - Initialize the development environment and clone QMK firmware
- **`devbox run qmk-compile`** - Compile the firmware for the RK R75 Pro keyboard
- **`devbox run ln-keyboard`** - Link the keyboard configuration (automatically run during setup)

## Development

### Modifying the Keyboard Configuration

The RK R75 Pro keyboard configuration is located in `src/keyboards/rk/r75_pro/`. Make your changes here, and they will be reflected in the firmware compilation.

### Using the Devbox Shell

To enter the Devbox development shell with all dependencies available:

```bash
devbox shell
```

From within the shell, you can run QMK commands directly:

```bash
qmk compile -kb rk/r75_pro -km default
```

## Documentation

For more information about QMK firmware development, visit:
- [Official QMK Documentation](https://docs.qmk.fm)
- [QMK GitHub Repository](https://github.com/qmk/qmk_firmware)

## License

This project uses QMK Firmware, which is licensed under multiple licenses. See the `qmk_firmware/` directory for license details.
