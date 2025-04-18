[![claw-text-blue](https://github.com/user-attachments/assets/7add156a-1678-46ca-a0ad-8c11e799f90d)](https://www.clawstudios.com/)

# N8N Local Environment Boilerplate

This repository provides a quick setup for running n8n locally with MongoDB integration using Docker Compose.

## 🚀 Features

- N8N workflow automation platform
- MongoDB database with authentication
- Persistent data storage
- Docker-based setup for easy deployment
- SSL/TLS support with Traefik and Let's Encrypt

## 📋 Prerequisites

- Docker
- Docker Compose
- Git (optional)
- Domain name pointing to your server (for SSL)

## 🛠️ Installation

1. Clone this repository or copy the `docker-compose.yml` file:

```bash
git clone https://github.com/clawstudios/n8n.git
```

2. Ensure acme.json is created and has the right permissions for Traefik:

```bash
chmod 600 traefik-data/acme.json
```

3. Run the Docker Compose setup:

```bash
docker compose up -d
```

4. Access N8N at https://your-domain.com (or http://localhost:5678 for local development).

## 🔧 Configuration

### MongoDB
- Host: `localhost`
- Port: `27017`
- Root Username: `root`
- Root Password: `root`
- Default Database: `n8n`

### N8N
- URL: `https://your-domain.com` or `http://localhost:5678` (local development)
- Default credentials will be created on first launch

### Traefik
- Automatically handles SSL certificates via Let's Encrypt
- Redirects HTTP to HTTPS
- Manages routing to the n8n service

## 📦 Volume Information

The setup uses three Docker volumes:
- `mongo_data`: Stores MongoDB data
- `n8n_data`: Stores n8n configurations and workflows
- Local directory `traefik-data`: Stores Traefik configuration and SSL certificates

## 🔒 Security Notes

- The MongoDB credentials in this setup are for development purposes only
- Change the default credentials before using in a production environment
- Consider implementing additional security measures for production use
- The `chmod 600 traefik-data/acme.json` step is critical for security and proper functioning of SSL

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
- [Traefik Documentation](https://doc.traefik.io/traefik/)