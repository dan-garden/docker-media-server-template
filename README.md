# Docker Media Server Template

Welcome to the Docker Media Server Template! This guide will help you get started with spinning up the docker-compose.yml file using Docker to create a comprehensive media server setup.

## Prerequisites

Before getting started, make sure you have the following installed on your system:

- Docker: [Installation Guide](https://docs.docker.com/get-docker/)
- Docker Compose: [Installation Guide](https://docs.docker.com/compose/install/)

## Getting Started

1. Clone the repository:

```shell
git clone https://github.com/dan-garden/docker-media-server-template.git
```

2. Create a `.env` file in the root directory of the project and add the following environment variables:

```plaintext
TIMEZONE=Etc/UTC
PUID=1000
PGID=1000
MOVIES_PATH=/path/to/movies
TVSHOWS_PATH=/path/to/tvshows
CONFIGS_PATH=/path/to/configs
DOWNLOADS_PATH=/path/to/downloads
PLEX_CLAIM=claim-xxxxxx
```

Make sure to replace `/path/to/movies`, `/path/to/tvshows`, `/path/to/configs`, and `/path/to/downloads` with the actual paths on your system.

3. Start the containers:

```shell
docker-compose up -d
```

This command will start the containers in detached mode.

4. Access the Media Server:

Once the containers are up and running, you can access your media server by opening your browser and navigating to `http://localhost`.

## Included Services

This template includes the following services:

- **Plex Media Server**: Organize and stream your movies, TV shows, music, and photos.
- **Radarr**: A movie collection manager that makes it easy to download and manage movies via Usenet and BitTorrent.
- **Sonarr**: A TV show collection manager that allows you to download and manage TV series.
- **qBittorrent**: An open-source BitTorrent client that is fast and efficient.
- **Prowlarr**: Manages your indexers for Radarr, Sonarr, and other media automation tools.
- **Overseerr**: A request management and media discovery tool for your media server.
- **Bazarr**: Manages subtitles for your movies and TV shows.
- **Tautulli**: A monitoring and tracking tool for Plex Media Server.

## Configuration

If you need to customize any settings, you can modify the `docker-compose.yml` file or the individual service configuration files located in the `configs` directory.

## Troubleshooting

If you encounter any issues or have questions, please refer to the [FAQ](https://github.com/dan-garden/docker-media-server-template/wiki/FAQ) or open an issue on the [GitHub repository](https://github.com/dan-garden/docker-media-server-template/issues).

## Contributing

Contributions are welcome! If you find a bug or have an idea for an improvement, please open an issue or submit a pull request.

## License

This project is licensed under the [MIT License](LICENSE).
