# Ansible
**Monitoring Solution with Prometheus and Grafana**
This project automates the deployment of Prometheus and Grafana for monitoring system and application metrics, along with custom alerting rules. The solution is implemented using Ansible.

**Running the Ansible Playbook**
Ensure you have Ansible installed on your local machine.

Update the inventory.ini file with the IP address or hostname of your monitoring server and Grafana server.

Run the following command to execute the Ansible playbook:

bash
Copy code
**ansible-playbook -i inventory.ini prometheus_grafana_setup.yml**
**Ansible Playbook Structure**
prometheus_grafana_setup.yml: Main Ansible playbook that orchestrates the deployment of Prometheus and Grafana.
Installs Prometheus and Grafana packages.
**Configures Prometheus and Grafana services.**
Sets up Prometheus scraping targets and alerting rules.
grafana.ini: Grafana configuration file specifying predefined data sources, authentication settings, and dashboard provisioning.
dashboard.json: Custom Grafana dashboard JSON file containing visualizations for Prometheus metrics.
Accessing the Grafana Dashboard
Open a web browser and navigate to http://<grafana_server_ip>:3000.
Log in using the default credentials (username: admin, password: admin).
Navigate to the predefined custom dashboard to view visualized metrics collected by Prometheus.
Customize the dashboard or create additional dashboards as needed.
Comments in the Code
The Ansible playbook (prometheus_grafana_setup.yml) contains comments to provide clarity and explain the purpose of each task, ensuring ease of understanding and maintenance.

Version Control (Optional)
This project can be version-controlled using Git to track changes, collaborate with team members, and maintain a history of modifications. Initialize a Git repository in the project directory and commit the code:

bash
Copy code
git init
git add .
git commit -m "Initial commit"
Consider pushing the code to a remote repository on platforms like GitHub or GitLab for better collaboration and version control management.


# variable file installation.
Prometheus variables:

prometheus_version: The version of Prometheus to install.

prometheus_config_dir: The directory where Prometheus configuration files will be stored.

prometheus_data_dir: The directory where Prometheus will store its data.

prometheus_web_listen_address: The address and port on which Prometheus will listen for web requests.

Grafana variables:

grafana_version: The version of Grafana to install.

grafana_data_dir: The directory where Grafana will store its data.

grafana_install_path: The path where Grafana will be installed.

grafana_port: The port on which Grafana will listen for web requests.

grafana_admin_user: The default username for the Grafana admin user.

grafana_admin_password: The default password for the Grafana admin user.

Node Exporter variables:

node_exporter_version: The version of the Node Exporter to install (optional, if you want to monitor node metrics).
