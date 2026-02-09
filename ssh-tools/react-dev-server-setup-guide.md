# Setting Up a React TypeScript Development Server Accessible from External Machines

This guide explains how to set up a React TypeScript development server on a VPS that can be accessed from your local machine for testing purposes.

## Prerequisites

- A VPS (Virtual Private Server) with Node.js and npm installed
- Basic knowledge of terminal commands
- Your VPS IP address

## Steps

### 1. Create a New React TypeScript Application

If you don't have an existing React TypeScript app, create one using:

```bash
npx create-react-app your-app-name --template typescript
```

### 2. Navigate to Your Project Directory

```bash
cd your-app-name
```

### 3. Configure the Development Server to Bind to All Network Interfaces

There are two ways to do this:

#### Method 1: Modify package.json

Update the start script in your `package.json` file:

```json
{
  "scripts": {
    "start": "HOST=0.0.0.0 react-scripts start",
    // ... other scripts
  }
}
```

#### Method 2: Create a .env File (Recommended)

Create a `.env` file in your project root directory:

```bash
touch .env
```

Add the following content to the `.env` file:

```
HOST=0.0.0.0
PORT=3000
```

This tells the development server to listen on all network interfaces (0.0.0.0) instead of just localhost (127.0.0.1).

### 4. Start the Development Server

```bash
npm start
```

The server will now be accessible on port 3000 of your VPS IP address.

### 5. Check Firewall Settings

Make sure your VPS firewall allows connections on port 3000:

```bash
# Check UFW status
ufw status

# If UFW is active and blocking port 3000, allow it:
ufw allow 3000

# Or check iptables rules
iptables -L
```

### 6. Find Your VPS IP Address

You can find your external IP address using:

```bash
curl ipinfo.io/ip
```

### 7. Access Your App from Local Machine

Open your browser on your local machine and navigate to:

```
http://YOUR_VPS_IP_ADDRESS:3000
```

For example: `http://185.231.59.46:3000`

## Additional Notes

- The React development server will automatically reload when you make changes to your code.
- Remember that this setup is intended for development/testing purposes only. Do not use this configuration for production.
- If you're using a cloud provider like AWS, Azure, or Google Cloud, make sure to configure their security groups/firewall settings to allow inbound traffic on port 3000.
- For security reasons, consider stopping the development server when you're not actively using it.

## Troubleshooting

### Server Not Accessible?

1. Verify the server is running: `ps aux | grep react-scripts`
2. Check if the server is listening on the correct port: `netstat -tuln | grep :3000` or `ss -tuln | grep :3000`
3. Ensure your VPS firewall allows connections on port 3000
4. Check your cloud provider's security group settings
5. Verify your IP address hasn't changed

### Stopping the Server

To stop the development server, use:

```bash
pkill -f react-scripts
```

## Alternative Port

If port 3000 is already in use or blocked, you can use a different port by modifying the PORT value in your `.env` file:

```
HOST=0.0.0.0
PORT=8080
```

Then access your app at `http://YOUR_VPS_IP_ADDRESS:8080`.