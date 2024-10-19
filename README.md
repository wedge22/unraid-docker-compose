# Unraid Docker Compose Projects

![License](https://img.shields.io/github/license/wedge22/unraid-docker-compose)
![Docker](https://img.shields.io/badge/docker-compose-1.29.2-blue)
![Unraid](https://img.shields.io/badge/unraid-6.9.2-brightgreen)

## Table of Contents

- [Introduction](#introduction)
- [Features](#features)
- [Prerequisites](#prerequisites)
- [Installation](#installation)
- [Usage](#usage)
- [Configuration](#configuration)
- [Contributing](#contributing)
- [License](#license)
- [Contact](#contact)

## Introduction

Welcome to the **Unraid Docker Compose** repository! This project provides a collection of Docker Compose files tailored for deploying various containers on [Unraid](https://unraid.net/), a popular NAS operating system. Whether you're looking to set up media servers, development environments, or other services, these Docker Compose configurations simplify the deployment process.

## Features

- **Modular Docker Compose Files:** Organized and easy-to-understand configurations for multiple containers.
- **Optimized for Unraid:** Tailored settings and volume mappings compatible with Unraid's directory structure.
- **Customizable:** Easily modify environment variables and settings to suit your needs.
- **Documentation:** Detailed instructions and comments within the Docker Compose files.

## Prerequisites

Before getting started, ensure you have the following:

- **Unraid Server:** Running [Unraid OS](https://unraid.net/download) (version 6.9.2 or later recommended).
- **Docker & Docker Compose:** Docker is built into Unraid, but you may need to install Docker Compose via the Unraid Community Applications plugin.
- **Git:** To clone this repository, you can use the Git client available on Unraid or install it on your local machine.

## Installation

1. **Clone the Repository**

   Navigate to the directory where you want to store your Docker Compose files and clone the repository:

   ```bash
   git clone https://github.com/wedge22/unraid-docker-compose.git
   cd your-repo-name
   ```

2. **Customize `.env` File (Optional)**

   Some Docker Compose files may use environment variables. Create a `.env` file based on the provided example:

   ```bash
   cp .env.example .env
   ```

   Edit the `.env` file to set your desired configurations.

3. **Deploy Containers**

   Use Docker Compose to deploy the containers:

   ```bash
   docker-compose up -d
   ```

   This command will pull the necessary Docker images and start the containers in detached mode.

## Usage

After installation, you can manage your Docker containers using Docker Compose commands:

- **Start Services**

  ```bash
  docker-compose start
  ```

- **Stop Services**

  ```bash
  docker-compose stop
  ```

- **View Logs**

  ```bash
  docker-compose logs -f
  ```

- **Restart Services**

  ```bash
  docker-compose restart
  ```

## Configuration

Each service in the Docker Compose files may have its own set of configurations. Below is a general guide:

1. **Environment Variables**

   Modify the `.env` file to set environment-specific variables like ports, volumes, and other service-specific settings.

2. **Volumes**

   Ensure that the volume paths in the Docker Compose files match your Unraid server's directory structure. For example:

   ```yaml
   volumes:
     - /mnt/user/appdata/service-name:/config
     - /mnt/user/media:/media
   ```

3. **Ports**

   Adjust the ports in the `docker-compose.yml` if there are conflicts or to match your network configuration.

   ```yaml
   ports:
     - "8080:80"
   ```

4. **Networks**

   If you have specific network requirements, configure the `networks` section accordingly.

## Contributing

Contributions are welcome! If you'd like to contribute to this project, please follow these steps:

1. **Fork the Repository**

2. **Create a Feature Branch**

   ```bash
   git checkout -b feature/YourFeature
   ```

3. **Commit Your Changes**

   ```bash
   git commit -m "Add your feature"
   ```

4. **Push to the Branch**

   ```bash
   git push origin feature/YourFeature
   ```

5. **Open a Pull Request**

Please ensure your contributions adhere to the following guidelines:

- Follow the existing code style.
- Provide clear commit messages.
- Update the documentation if necessary.

## License

This project is licensed under the [MIT License](LICENSE).

## Contact

For any questions or suggestions, feel free to [open an issue](https://github.com/wedge22/unraid-docker-compose/issues) or reach out to me directly at [ksh78@pm.me](mailto:ksh78@pm.me).
