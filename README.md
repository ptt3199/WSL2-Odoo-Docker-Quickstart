# Odoo Development Environment with Docker on WSL2

Welcome to the repository designed to help you overcome the challenges of setting up an Odoo development environment using Docker on Windows Subsystem for Linux 2 (WSL2). This guide is born out of the difficulties encountered while trying to install PostgreSQL (a prerequisite for Odoo) on WSL2 and the subsequent realization that Docker offers a more streamlined approach.

## Why Docker on WSL2?

WSL2 offers numerous benefits for developers by providing a Linux-like environment on Windows. However, setting up certain services like PostgreSQL for Odoo can be problematic. Docker emerges as a solution by encapsulating the environment needed for Odoo, thus bypassing the complexities of direct installation on WSL2 or Windows.

## Getting Started

This repository serves as a template to kickstart your Odoo development journey on WSL2 using Docker. Follow the steps below to set up your environment:

1. **Run Docker Compose**: Execute `docker compose up -d` to start the Odoo and PostgreSQL containers.
2. **Custom Addons**: Place your custom addons in the `addons` folder to extend Odoo's functionality as you learn.
3. **Configuration**: If necessary, create your configuration files in the `config` folder.

### Docker Compose Details

The `docker-compose.yml` file is structured to ensure that the Odoo container (`web`) depends on the PostgreSQL container (`db`). This setup requires running the database container before Odoo. It's crucial to use the exact environment variables described in the Docker Compose file, as they are configured for initial setup with Odoo.

### Persistence

To retain Odoo and PostgreSQL data even after the containers are deleted, volume setup is included. This ensures your data is safely stored and can be reused or restored.

## Reference

For detailed information on the Docker image for Odoo, visit [Odoo Docker Official Page](https://registry.hub.docker.com/_/odoo).

## Conclusion

This repository aims to simplify the process of setting up an Odoo development environment on WSL2 using Docker. By following the outlined steps, you can quickly start learning and developing with Odoo without the hassle of complex installations.

Happy coding!