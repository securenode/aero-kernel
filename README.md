# AeroLinux Kernel

## Overview

The AeroLinux Kernel is a custom Linux kernel designed to deliver exceptional performance and responsiveness, particularly for Arch-based systems. Leveraging the BORE Scheduler and a suite of under-the-hood optimizations, this kernel aims to provide a superior computing experience tailored specifically for AeroLinux.

**Note:** This project is in its early stages and is currently forked from the CachyOS BORE kernel. We extend our gratitude to the CachyOS team for their foundational work and contributions.

## Features

- **BORE Scheduler**: Utilizes the Burst-Oriented Response Enhancer (BORE) Scheduler for improved task scheduling and system responsiveness.
- **CPU Optimization**: Automatic CPU detection and optimization to ensure the best performance for your specific hardware.
- **Clang LTO**: Supports Clang Link Time Optimization (LTO) for enhanced performance and reduced binary size.
- **Custom Patches**: Includes a variety of patches and improvements from the CachyOS kernel, with plans for further AeroLinux-specific customizations.

## Installation

### Prerequisites

Ensure you have the following dependencies installed:

- `bc`
- `cpio`
- `gettext`
- `libelf`
- `pahole`
- `perl`
- `python`
- `tar`
- `xz`
- `zstd`

### Building the Kernel

1. Clone the repository:
    ```sh
    git clone https://github.com/yourusername/aerolinux-kernel.git
    cd aerolinux-kernel
    ```

2. Configure the build options in the `PKGBUILD` file to suit your needs. Key options include:
    - `_cpusched`: Select the CPU scheduler (`bore`, `bmq`, `hardened`, `cachyos`, etc.).
    - `_use_auto_optimization`: Enable or disable automatic CPU optimization.
    - `_use_llvm_lto`: Set the Clang LTO mode (`none`, `full`, `thin`).

3. Build and install the kernel:
    ```sh
    makepkg -si
    ```

## Configuration

The kernel configuration can be further customized by editing the `config` file. Key configuration options include:

- **Compression Algorithms**: Enable or disable various kernel compression algorithms (e.g., `CONFIG_KERNEL_ZSTD`).
- **Security Features**: Configure security-related options such as `CONFIG_STRICT_KERNEL_RWX` and `CONFIG_AUDIT`.
- **IRQ Subsystem**: Fine-tune IRQ settings for optimal performance.

## Contributing

We welcome contributions from the community. Please fork the repository and submit pull requests for any improvements or bug fixes.

## License

This project is licensed under the MIT License. See the [LICENSE](LICENSE) file for details.

## Contact

For any questions or support, please open an issue on GitHub or contact the maintainers directly.

---

*Note: This project is currently a fork of the CachyOS BORE kernel. Future updates will include AeroLinux-specific modifications and enhancements.*

