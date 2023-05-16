# TP4_Sec_Reseaux
  
![Ubuntu-logo](https://github.com/adilraad2001/TP4_Sec_Reseaux/assets/99618982/3ead7fa6-3cd0-407f-aa5c-6f63b1ea6af8)

Realisé Par : Adil Erraad

# Sommaire:

 1. **Introduction:**
 
    1. *Objectifs de ce TP :*
    
    2. *Outils logiciels :*
    
 2. **Methodology:**
 
 3. **Conclusion:**


## 1. **Introduction:**
  1. *Objectifs de ce TP :*
    IPCop is a Linux-based firewall distribution that provides a secure network infrastructure for small to medium-sized businesses or home networks. It offers a range of features, including firewalling, network address translation (NAT), VPN connectivity, intrusion detection, and traffic shaping  ,And in this TP Will explore the creation and implementation of a firewall using IPCop—an open-source Linux-based firewall distribution—and to provide a comprehensive guide on how to set it up to protect a network. 
  
  2. *Outils logiciels :*
    
      - IpCop
    
    
      - ubuntu
   
## 2.**Methodology:**

  1.1 Installation :
  - First we need to download the image of Ipcop from the officiel website : www.ipcop.org
  - We need to follow the step of installation
    
![2023-05-16 16_59_49-IpCopx  Running  - Oracle VM VirtualBox](https://github.com/adilraad2001/TP4_Sec_Reseaux/assets/99618982/088ce3da-94f4-44a9-add2-1d62ca500b1d)

   keyboard input :

![2023-05-16 17_00_19-TP-Firewall](https://github.com/adilraad2001/TP4_Sec_Reseaux/assets/99618982/593b7ec3-d0b5-4142-a956-732914fa8066)

  And follow this by next :
  
  and well get interface show each interface the machine connected on it and choose for each one color and after give each one an ip address for each zone (GREEN-RED-ORANGE)
  
  ![2023-05-16 17_02_05-IpCopx  Running  - Oracle VM VirtualBox](https://github.com/adilraad2001/TP4_Sec_Reseaux/assets/99618982/f1a4faa5-1d21-4d7b-8f22-f3d9f3bbd4f3)
  
  ![2023-05-16 17_02_29-TP-Firewall](https://github.com/adilraad2001/TP4_Sec_Reseaux/assets/99618982/8b98dcff-76f0-43dc-970d-ff2787ce5fc7)

And now choosing the addresse of the dns and  the configuration of dhcp

![2023-05-16 17_03_29-IpCopx  Running  - Oracle VM VirtualBox](https://github.com/adilraad2001/TP4_Sec_Reseaux/assets/99618982/c6fffa57-7a25-42b0-8f4f-b21fb26b76a2)

![2023-05-16 17_03_01-IpCopx  Running  - Oracle VM VirtualBox](https://github.com/adilraad2001/TP4_Sec_Reseaux/assets/99618982/05d42622-2dc3-4151-8cce-0f841f8ed7af)

After this configuration well get an interface of command line

![2023-05-16 18_05_40-IpCopx  Running  - Oracle VM VirtualBox](https://github.com/adilraad2001/TP4_Sec_Reseaux/assets/99618982/687559bd-190a-4204-acfe-f4bc4164d120)

  Or we can use Machine connected by his DHCP server for get a Graphical interface for administration:

![2023-05-16 17_10_24-Ubuntu 1  Running  - Oracle VM VirtualBox](https://github.com/adilraad2001/TP4_Sec_Reseaux/assets/99618982/108c46ea-f83c-4933-a497-7ed3b70dea94)

This machine get an ip addresse from the dhcp server of ipcop so We have the right to get the control Panel of ipcop from this machine:
Connected in the port 8443

![2023-05-16 17_14_19-Ubuntu 1  Running  - Oracle VM VirtualBox](https://github.com/adilraad2001/TP4_Sec_Reseaux/assets/99618982/e192d765-173d-4e6f-9c74-8a69530ec92c)

We need to use the admin account We set a password for it during installation

![2023-05-16 17_27_24-Ubuntu 1  Running  - Oracle VM VirtualBox](https://github.com/adilraad2001/TP4_Sec_Reseaux/assets/99618982/31c8cfca-6bcb-47ce-ade1-61731347cd32)

2. **Filtreing**

  There's different type for secure your network by using th ipcop firewall therefore, showing how to use them and reviewing them will take a lot of time.
  Thats why we will showing just Proxy filtering & URL Filter & ssh connection
  
  - **_Proxy Filtering :_**
  
      We mean by proxy filtering the capability of the firewall to act as an intermediary between a client device and the internet, allowing for enhanced control and filtering of web traffic. When proxy filtering is enabled in IPCop, web requests from client devices are routed through the IPCop proxy server, which then forwards the requests to the internet on behalf of the client.   
      
      ![2023-05-16 17_28_04-Ubuntu 1  Running  - Oracle VM VirtualBox](https://github.com/adilraad2001/TP4_Sec_Reseaux/assets/99618982/f80fc556-fb0d-4528-badd-75019ab02efa)

      In order to make it work we need to Enable the Web proxy in our Local Network and choose a port for connection
      
![2023-05-16 17_28_04-Ubuntu 1  Running  - Oracle VM VirtualBox](https://github.com/adilraad2001/TP4_Sec_Reseaux/assets/99618982/d4dbfa6c-9b77-4d46-8e41-2a3eea3da9b7)

![2023-05-16 17_12_15-Ubuntu 1  Running  - Oracle VM VirtualBox](https://github.com/adilraad2001/TP4_Sec_Reseaux/assets/99618982/29902d51-5500-4bbb-8d71-d4a52974049f)


  After activiting the web proxy and applied in our browser as we can see we can't connect in this web site because we blocked his domain name in our firewall but we can access to the other
  
  ![2023-05-16 17_44_47-Ubuntu 1  Running  - Oracle VM VirtualBox](https://github.com/adilraad2001/TP4_Sec_Reseaux/assets/99618982/bc3c54c7-782f-4a77-b6f3-e90b58a10cd9)
  
  And we can see this in our Proxy log menu
  
![2023-05-16 17_44_57-Ubuntu 1  Running  - Oracle VM VirtualBox](https://github.com/adilraad2001/TP4_Sec_Reseaux/assets/99618982/aa28e8a6-24fb-45ea-b97b-e65a3f8bc266)

    
  - **_URL Filter :_**
  
      The URL Filter use to involves controlling and restricting access to specific websites based on their URLs (Uniform Resource Locators), which are the addresses used to access web pages or resources on the internet.
     To Block an web site or ip from access without applied the proxy :
     
     ![2023-05-16 17_32_10-Ubuntu 1  Running  - Oracle VM VirtualBox](https://github.com/adilraad2001/TP4_Sec_Reseaux/assets/99618982/0df56d1b-bc0f-407f-9979-9350456640a8)

we need before the acticvation to activate the redirection when someone want to open this website to redirect automaticaly(in proxy menu) to access denied page:

![2023-05-16 17_33_36-Ubuntu 1  Running  - Oracle VM VirtualBox](https://github.com/adilraad2001/TP4_Sec_Reseaux/assets/99618982/9bd87e78-23e6-41ee-89bc-df9251862caa)


As u can see in the image we try to block the access to the address 8.8.8.8


![2023-05-16 17_33_44-Ubuntu 1  Running  - Oracle VM VirtualBox](https://github.com/adilraad2001/TP4_Sec_Reseaux/assets/99618982/8bbf5798-9ef5-421f-8a45-9c698dc5199d)

The connection denied by the filtering and redirect to block page

![2023-05-16 17_33_59-Ubuntu 1  Running  - Oracle VM VirtualBox](https://github.com/adilraad2001/TP4_Sec_Reseaux/assets/99618982/244aecaa-eacd-428d-8cf0-30f25425ea28)
  
  
  - **_shh Access_**:

    In ipcop we use ssh to allows administrators to securely access the firewall's command-line interface (CLI) remotely using SSH. By establishing an SSH connection, administrators can remotely execute commands, configure settings, and manage the IPCop firewall from a trusted location, providing secure administrative access to the firewall.
    And  well try this by check the connection by ssh before activation and when active connection by password and by public key
    
    Before activation we get connection failled and we can see the port using it's not the regular port
    
    ![2023-05-16 17_38_36-Ubuntu 1  Running  - Oracle VM VirtualBox](https://github.com/adilraad2001/TP4_Sec_Reseaux/assets/99618982/99376654-1b3d-40e9-a0d4-c4718006f447)

    After activating and accepting the connection by password
    
    ![2023-05-16 17_38_59-Ubuntu 1  Running  - Oracle VM VirtualBox](https://github.com/adilraad2001/TP4_Sec_Reseaux/assets/99618982/5e13c22f-afa1-4b90-8edd-6bc1306d05fb)
    

    ![2023-05-16 17_40_12-Ubuntu 1  Running  - Oracle VM VirtualBox](https://github.com/adilraad2001/TP4_Sec_Reseaux/assets/99618982/dfcc5422-8ac4-4e4c-ada1-03d2df81d7fd)

and by using the public key

    ![2023-05-16 17_40_29-Ubuntu 1  Running  - Oracle VM VirtualBox](https://github.com/adilraad2001/TP4_Sec_Reseaux/assets/99618982/a48dce0e-aabd-475e-bfa1-3226be882237)
    
    3. **Conclusion:**
 
    of creating a firewall using IPCop and setting it up to protect a network has provided valuable insights into network security and the importance of robust protection measures. The implementation and configuration of IPCop as a firewall solution have demonstrated its effectiveness in safeguarding networks against potential threats and unauthorized access

    
    
  


