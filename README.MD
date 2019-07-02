ROLE Name    : install_ansible_tower                                                 
ROLE Author  : Ken Hitchcock                                                   
ROLE Purpose : Automate Ansible Tower installation                          


Requirements

Variables required to be set before running the role.

Where to get tower installation files. Will require a predownloaded tower tar gz file. 
This will need to be hosted on a webserver.
   - webserver: "http://webservernameorip/pub"
   - tower_download_file: "ansible-tower-setup-bundle-latest.el7.tar.gz"
   - tower_extracted_dir: "ansible-tower-setup-bundle-3.4.1-1.el7"
   - working_location: "/root/"
   - platform_group_name: "tower"

Password configuration for Tower, defaults is set to password. 
Use Vault or similar for secure storage or manually change password after.
   - admin_password: "password"
   - pg_password: "password"
   - rabbitmq_password: "password"

License file variables for registering tower. 
You will need to generate a license file first and get the values from your email.
   - tower_license_company_name: "Red Hat"
   - tower_license_email: "ken.hitchcock@automateroles.com"
   - tower_license_contact_name: "Ken Hitchcock"
   - tower_license_hostname: "acmeserver0987234759843759"
   - tower_license_instance_count: "10"
   - tower_license_date: "2118064323"
   - tower_license_license_key: "asdf987sd9898sad7f987sda9f87asd8f79sad87f"
   - tower_license_license_type: "basic"
   - tower_license_subscription_name: "Red Hat Ansible Tower, Self-Support (10 Managed Nodes)"



