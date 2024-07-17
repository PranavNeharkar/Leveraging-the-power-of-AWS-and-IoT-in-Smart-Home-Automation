# Leveraging-the-power-of-AWS-and-IoT-in-Smart-Home-Automation
Designed and implemented a smart home automation system using AWS IoT services. 
Integrated various IoT devices for real-time monitoring and control of home appliances.
Implemented MQTT protocol for secure and reliable communication between devices.
Programmed ESP32 devices to control and monitor home appliances via Wi-Fi connectivity.
Hardware Required:
ESP32 Wifi Module
4 Channel Relay
Jumper Wires
Bulbs
PCB
Software Requirements:
Arduino IDE




STEPS:
After successfully signing in, the AWS Management Console window will open. In the services search tab at the top right ‘IoT core’ & hit enter.
You can click on IoT Core, so an AWS IoT Dashboard will appear now.



On the left side of the dashboard, there are so many options. But we need to work with two options here. One is the manage option and the other one is the secure option.

Creating a Thing
Now we need to create a thing associated with our project. For this, follow the following steps:

Specifying thing properties
Configuring device certificate
Attaching policies to certificate
Under the manage option click on Thing. Now we need to create a Thing here. So, click on Create Things here.

You can select whether create a single thing or create many things. But for our applications, select create a single thing. Then click on Next.

Specify Thing Properties
Here we need to specify the Thing properties. First, give a thing name. You can name it anything. For example, I will name it Home_Automation.

Under additional configurations, there is no need to make any changes.

Under the device shadow option, select the first option as No shadow. Then click on Next.

Generate Device Certificate
Now you need to configure device certificate. So here you can auto-generate a new certificate or use your own certificate or upload CSR or skip this.

But the AWS recommendation is to select the Auto Generate New Certificate. Then click on Next.

Create & Attach Policy
Now we need to attach a policy to the Things we created. But no policies are here right now. So we need to create a policy first.

So click on create policy. Here give any name to the policy. For example, I will give it a name as “Automation_Policy“.

Now the add statement part is very important. Under the action, type IoT. So multiple options will pop up. From here we will only need to Subscribe, Connect and Receive.

Now click on create to create the policy. So the policy has been created successfully.

Now go back to Create Thing option. So a policy option will appear. We need to attach the policies to the certificate. So select the appeared policy and click on create a thing.

Downloading Certificates and Keys
Now we need to download the required certificates from this list.

First, download the device certificate and then rename it as a device certificate for identification.

Also, download the public key and rename it as a public key. Then download the private key and rename it as a private key.

In the Root CA Certificates, there are two certificates here. But we just need a Root CA1 certificate, so download it as well.

So we have downloaded all the certificates that we need for our project.

The Source Code/Program for Home automation using Amazon AWS IoT Core & ESP32 is written in Arduino IDE. Before moving to the code part, we need to install few libraries to the Arduino IDE. Download the PubSubClient Library and add it to the Arduino IDE library folder.

Here is the complete code for the project that requires a lot of modifications. Copy it and paste it to your Arduino IDE.
