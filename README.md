# **Dockerizing a Laravel Application with Docker Compose** 

## **Overview**
I focused on containerizing a Laravel application using Docker Compose. The project involved orchestrating multiple services, making the setup efficient for development and production environments. By integrating both application and utility containers, I ensured live updates and seamless application functionality.

---

## **Key Features**
- **Multi-Container Setup**: Utilized Docker Compose to run multiple services required for the Laravel application.  
- **Custom Dockerfiles**: Wrote Dockerfiles for Composer, NGINX, and PHP to customize the environment.  
- **Database Connectivity**: Configured MySQL with environment variables for secure and seamless interaction.  
- **Live Updates**: Integrated utility containers to enable real-time source code updates during development.  

---

## **Step-by-Step Setup**

### **1. Set Up Docker Compose**
- Created a `docker-compose.yml` file to define and orchestrate services, including:
  - **NGINX**: As the web server for serving the Laravel application.
  - **PHP**: To run the Laravel backend.
  - **MySQL**: As the database for the application.
  - **Composer**: To manage Laravel dependencies.
  - **Node.js**: For compiling front-end assets.
  - **Artisan**: To execute Laravel-specific commands like migrations.

---

### **2. Write Dockerfiles**
- **NGINX Dockerfile**: Defined custom configurations for the web server.  
- **PHP Dockerfile**: Set up PHP with the necessary extensions for Laravel.  
- **Composer Dockerfile**: Enabled dependency management for Laravel.  

---

### **3. Configure Environment Variables**
- Created a `.env` file to store MySQL environment variables such as:
  - Database name, user, and password.
  - Port mapping to ensure secure database connectivity.  

---

### **4. Enable Live Source Code Updates**
- Leveraged Docker’s volume mapping to sync local source code with the container, enabling real-time updates without rebuilding containers.  
- Integrated utility containers for tasks like running Composer commands and Laravel migrations.

---

### **Directory Structure**
```plaintext
project-root/
├── docker-compose.yml
├── .env
├── NGINX/
│   ├── Dockerfile
│   ├── default.conf
├── PHP/
│   ├── Dockerfile
│   ├── php.ini
├── Laravel/
│   ├── app/
│   ├── public/
│   ├── composer.json
│   └── .env
└── MySQL/
    └── data/




