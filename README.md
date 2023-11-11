
# MiniDLNA Docker Compose Configuration

The MiniDLNA Docker Compose configuration file (`docker-compose.yml`) provided here allows you to easily spin up a MiniDLNA media server container with the specified settings.

## Prerequisites

Before deploying the MiniDLNA container, ensure that the following are installed on your system:

- Docker: Install Docker on your system by following the official installation guide for your operating system.

## Usage

To use this Docker Compose configuration, follow these steps:

1. Clone the repository
2. Modify the `volumes` section according to your specific requirements. In the provided example, `/mnt/ext/av/` on the local system is mounted as `/media` inside the container. Adjust this path to match your media directory.
3. Modify environment variables, if necessary, to suit your preferences. In the example, the MiniDLNA media directory, port, and friendly name are specified.
4. Open a terminal or command prompt and navigate to the directory containing `docker-compose.yml`.
5. Run the following command to start the MiniDLNA container:

   ```shell
   docker-compose up -d
   ```

   The `-d` flag runs the containers in detached mode, allowing them to run in the background.

7. The MiniDLNA media server should now be up and running, serving media files from the specified directory.

## Configuration

The provided Docker Compose configuration sets up the MiniDLNA container with the following options:

- `image`: Specifies the MiniDLNA image to use (`cytomich/rpi-docker-minidlna` in this example).
- `volumes`: Maps the local media directory to the container's media directory.
- `environment`: Sets environment variables for MiniDLNA, including the media directory (MINIDLNA_MEDIA_DIR), port (MINIDLNA_PORT), and friendly name (MINIDLNA_FRIENDLY_NAME).
- `network_mode`: Specifies the network mode for the container. In this example, it uses the host network.
- `restart`: Sets the container to automatically restart if it stops or encounters an error.

Feel free to adjust the configuration according to your specific requirements.

## Customization

You can customize the configuration by modifying the following options:

- Use a different MiniDLNA image by changing the `image` field to the desired image name or repository.
- Adjust the mounted volumes to match your media directory structure by modifying the `volumes` field.
- Modify the environment variables to suit your preferences by editing the `environment` field.


## License

This project is licensed under the [MIT License](LICENSE).
