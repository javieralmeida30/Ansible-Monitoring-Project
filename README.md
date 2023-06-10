# Monitoring Setup Project

This project is aimed at helping us implement a monitoring setup for an organization using open-source tools like Prometheus, Grafana, Alertmanager, etc. The goal is to install and configure these tools on the target system and create a complete and automated monitoring environment.

## Architecture

The monitoring setup consists of two EC2 instances:

- **Monitoring Server**: This instance will host the monitoring tools such as Prometheus, Grafana, and Alertmanager. It will collect and display metrics from the monitored nodes.
- **Monitored Nodes**: These instances represent the nodes within the organization's infrastructure that need to be monitored. They will have the Node Exporter installed to expose system-level metrics to Prometheus.

## Getting Started

To get started with the monitoring setup, follow the instructions below.

### Prerequisites

- Two EC2 instances set up, one for the Monitoring Server and the other for the Monitored Nodes.
- Ansible installed on your local machine.

### Installation and Configuration

1. Clone this repository to your local machine:
git clone <repository-url>
  
2. Navigate to the project directory:


Sure! Here's an updated version of the README, taking into account that you have two EC2 instances, one for the monitoring setup and the other for the nodes being monitored:

markdown
Copy code
# Monitoring Setup Project

This project is aimed at helping us implement a monitoring setup for an organization using open-source tools like Prometheus, Grafana, Alertmanager, etc. The goal is to install and configure these tools on the target system and create a complete and automated monitoring environment.

## Architecture

The monitoring setup consists of two EC2 instances:

- **Monitoring Server**: This instance will host the monitoring tools such as Prometheus, Grafana, and Alertmanager. It will collect and display metrics from the monitored nodes.
- **Monitored Nodes**: These instances represent the nodes within the organization's infrastructure that need to be monitored. They will have the Node Exporter installed to expose system-level metrics to Prometheus.

## Getting Started

To get started with the monitoring setup, follow the instructions below.

### Prerequisites

- Two EC2 instances set up, one for the Monitoring Server and the other for the Monitored Nodes.
- Ansible installed on your local machine.

### Installation and Configuration

1. Clone this repository to your local machine:
git clone <repository-url>


2Navigate to the project directory:
cd Monitoring-Setup-Project
  
3. Update the `inventory` file with the IP addresses or hostnames of your EC2 instances. Specify the Monitoring Server under the `[monitoring]` group and the Monitored Nodes under the `[nodes]` group.

4. Review and update the `playbook.yml` file with the desired configuration settings for your monitoring setup.

5. Run the Ansible playbook to install and configure the monitoring tools:
ansible-playbook -i inventory playbook.yml
  
  
6. The monitoring setup will be installed and configured on the respective EC2 instances.

## Accessing Monitoring Tools

- Prometheus: Access Prometheus by navigating to `http://<monitoring-server-ip>:9090` in your web browser.
- Grafana: Access Grafana by navigating to `http://<monitoring-server-ip>:3000` in your web browser. The default credentials are `admin/admin`.
- Alertmanager: Access Alertmanager by navigating to `http://<monitoring-server-ip>:9093` in your web browser.

## Contributing

Contributions are welcome! If you have any suggestions, improvements, or bug fixes, please open an issue or submit a pull request.

## License

This project is licensed under the [MIT License](LICENSE).



