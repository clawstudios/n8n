# N8N Local Environment Boilerplate

This repository provides a quick setup for running n8n locally with MongoDB integration using Docker Compose.

## 🚀 Features

- N8N workflow automation platform
- MongoDB database with authentication
- Persistent data storage
- Docker-based setup for easy deployment

## 📋 Prerequisites

- Docker
- Docker Compose
- Git (optional)

## 🛠️ Installation

1. Clone this repository or copy the `docker-compose.yml` file:

```bash
git clone https://github.com/clawstudios/n8n.git
```

2. Create the external volume for n8n:

```bash
docker volume create n8n_data
```

3. Run the Docker Compose setup:

```bash
docker compose up -d
```

4. Access N8N at http://localhost:5678.

## 🔧 Configuration

### MongoDB
- Host: `localhost`
- Port: `27017`
- Root Username: `root`
- Root Password: `root`
- Default Database: `n8n`

### N8N
- URL: `http://localhost:5678`
- Default credentials will be created on first launch

## 📦 Volume Information

The setup uses two Docker volumes:
- `dbdata6`: Stores MongoDB data
- `n8n_data`: Stores n8n configurations and workflows (external volume)

## 🔒 Security Notes

- The MongoDB credentials in this setup are for development purposes only
- Change the default credentials before using in a production environment
- Consider implementing additional security measures for production use

## 🤝 Contributing

Feel free to submit issues, fork the repository, and create pull requests for any improvements.

## 📝 License

[Your chosen license]

## ⚠️ Disclaimer

This is a development setup and should be properly secured before using in a production environment.

## 🔗 Useful Links

- [N8N Documentation](https://docs.n8n.io/)
- [MongoDB Documentation](https://docs.mongodb.com/)
- [Docker Documentation](https://docs.docker.com/)