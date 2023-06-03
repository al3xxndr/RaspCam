<!DOCTYPE html>
<html>
<head>
  <title>Raspberry Pi SSH and Camera Setup</title>
  <style>
    body {
      font-family: Arial, sans-serif;
      margin: 20px;
    }

    h1 {
      color: #333;
      font-size: 24px;
    }

    h2 {
      color: #666;
      font-size: 20px;
      margin-top: 10px;
    }

    ol {
      margin-top: 10px;
    }

    li {
      margin-bottom: 5px;
    }
  </style>
</head>
<body>
  <h1>Raspberry Pi SSH and Camera Setup</h1>

  <h2>Setting up Raspberry Pi as an SSH server:</h2>
  <ol>
    <li>Install Raspberry Pi OS by flashing the latest version onto an SD card.</li>
    <li>Connect the Raspberry Pi to power and establish a network connection (Ethernet or Wi-Fi).</li>
    <li>Update the system packages by running the following commands:<br>
      <code>sudo apt update<br>
        sudo apt upgrade</code></li>
    <li>Enable SSH by executing the following commands:<br>
      <code>sudo systemctl enable ssh<br>
        sudo systemctl start ssh</code></li>
    <li>Optionally, configure the Raspberry Pi using the <code>raspi-config</code> tool.</li>
    <li>Find the IP address of the Raspberry Pi on the network using the <code>ifconfig</code> command.</li>
    <li>Install the Termius app on your iOS device.</li>
    <li>Open Termius and add a new host using the Raspberry Pi's IP address, SSH as the connection type, and a chosen name.</li>
    <li>Enter the Raspberry Pi's username and password.</li>
    <li>Tap the newly added host in Termius to establish an SSH connection to the Raspberry Pi.</li>
  </ol>

  <h2>Accessing Raspberry Pi camera via fswebcam:</h2>
  <ol>
    <li>Install fswebcam on the Raspberry Pi using the command:<br>
      <code>sudo apt-get install fswebcam</code></li>
    <li>Capture an image using fswebcam with the following command:<br>
      <code>fswebcam image.jpg</code></li>
    <li>Customize the command with options like resolution, delay, and device selection, if desired.</li>
  </ol>

  <h2>Viewing the image on an iPhone:</h2>
  <ol>
    <li>Use the SCP command to securely copy the image file from the Raspberry Pi to the iPhone. For example:<br>
      <code>scp pi@&lt;Raspberry_Pi_IP_Address&gt;:/path/to/image.jpg ~/Documents/</code></li>
    <li>Open an image viewer app on your iPhone and access the copied image.</li>
    <li>Alternatively, set up a web server on the Raspberry Pi and serve the image file. Access the image from your iPhone's web browser using the Pi's IP address and the appropriate URL (e.g., <code>http://&lt;Raspberry_Pi_IP_Address&gt;/image.jpg</code>).</li>
  </ol>

  <p>Remember to ensure the security of your Raspberry Pi and SSH connection by using strong passwords and following network security best practices.</p>
</
