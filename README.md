
# NestJS Backend Deployment with Ansible

This project automates the deployment of a NestJS backend application using Ansible. It sets up a server with all necessary dependencies, configures the environment, and deploys the application.

## Server Information

- IP Address: 3.93.12.152
- Base URL: http://3.93.12.152

## API Response

When you access the base URL, you should receive the following JSON response:

```json
{
  "status": true,
  "status_code": 200,
  "message": "Welcome to NestJs Backend Endpoint"
}
```

## Project Structure

The main configuration file for this project is `main.yaml`, which contains the Ansible playbook for deploying the application.

## Deployment Steps

The Ansible playbook performs the following main steps:

1. Creates a user named 'hng' with sudo privileges
2. Sets up necessary directories
3. Configures PostgreSQL credentials
4. Updates and installs required packages (including Node.js)
5. Clones the NestJS boilerplate repository
6. Sets up the application environment
7. Installs application dependencies
8. Starts the application
9. Configures Nginx as a reverse proxy
10. Ensures all required services are running


## Running the Deployment

To deploy the application, run the Ansible playbook using the following command:

```
sudo ansible-playbook main.yaml -i inventory.cfg -b
```

Note: Make sure you have Ansible installed and properly configured on your local machine.

## Logging

Application logs are stored in the following locations:

- Error logs: /var/log/stage_5b/error.log
- Output logs: /var/log/stage_5b/out.log


