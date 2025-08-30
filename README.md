# Bridge Configuration Generator

A professional network bridge configuration tool for enterprise server infrastructure. This React application helps system administrators generate accurate network bridge configuration commands for various Linux distributions.

# Features

* Multi-OS Support: Generate configurations for CentOS 7, AlmaLinux 8.x/9.x, Ubuntu (16.04, 18.04+, 20.04), and generic Linux systems.
* Smart Configuration Parser: Automatically extract and parse settings from existing network configuration files.
* Hetzner Server Detection: Identifies Hetzner environments and applies the correct configuration methods.
* IPv6 Compatibility: Optional IPv6 configuration with built-in validation.
* Bonding Support: High-availability bonding with bridge support for resilient networking.
* Command Generator: Create ready-to-use configuration commands and files.
* Export Options: Copy generated commands to clipboard or export them as executable scripts.

# Prerequisites

* Node.js (v16 or later)
* npm or yarn
* React environment

# Setup Instructions

1. Clone the repository:


git clone https://github.com/yourusername/bridge-config-generator.git
cd bridge-config-generator


2. Install dependencies:


npm install


3. Start the development server:


npm run dev


4. Open [http://localhost:3000](http://localhost:3000) in your browser.

# Usage Guide

1. Select OS: Choose the Linux distribution you want to configure.
2. Bridge Settings: Define bridge name, interface, IP, netmask, and gateway. Configure optional STP, MTU, DNS, and IPv6 if required.
3. Auto-Fill Option: Paste existing configuration into the parser to auto-populate fields.
4. Generate Configurations: Click to generate commands and configuration files. Copy or download as needed.

# Supported Operating Systems

* CentOS 7: Traditional network-scripts configuration.
* AlmaLinux 8.x/9.x: NetworkManager-based setup.
* Ubuntu 16.04/20.04: `/etc/network/interfaces` configuration.
* Ubuntu 18.04+: Netplan configuration (special handling for Hetzner).
* Bond Server: Bonded high-availability bridge configuration.
* Generic Linux: Manual bridge configuration commands.

# Configuration Options

| Option             | Description                               | Required                 |
| ------------------ | ----------------------------------------- | ------------------------ |
| Operating System   | Target Linux distribution                 | Yes                      |
| Bridge Name        | Bridge interface name                     | Yes                      |
| IP Address         | IPv4 address for the bridge               | Yes                      |
| Netmask            | Subnet mask (CIDR or dotted decimal)      | Yes                      |
| Gateway            | Default gateway IP                        | Yes                      |
| Physical Interface | Interface to attach to bridge             | Yes                      |
| Enable STP         | Enable Spanning Tree Protocol             | No                       |
| MTU                | Maximum Transmission Unit (default: 1500) | No                       |
| Enable IPv6        | Enable IPv6 configuration                 | No                       |
| IPv6 Address       | Bridge IPv6 address                       | Required if IPv6 enabled |
| IPv6 Gateway       | IPv6 default gateway                      | Required if IPv6 enabled |
| DNS Servers        | List of DNS servers (comma-separated)     | No                       |

# Technologies Used

* React (frontend framework)
* TypeScript (type safety)
* Tailwind CSS (styling)
* shadcn/ui (UI components)
* Lucide React (icons)
* Radix UI (UI primitives)

# Project Structure


src/
├── components/
│   ├── ui/          # shadcn/ui components
│   └── hooks/       # Custom React hooks
├── lib/             # Utility functions
├── types/           # TypeScript type definitions
└── App.tsx          # Main application component


# Contribution Guidelines

1. Fork the repository.
2. Create a feature branch (`git checkout -b feature/new-feature`).
3. Commit changes (`git commit -m 'Add new feature'`).
4. Push to the branch (`git push origin feature/new-feature`).
5. Submit a Pull Request.

# License

This project is licensed under the MIT License. See the [LICENSE](LICENSE) file for details.

# Support

For questions or issues, please open a ticket on the GitHub repository.
