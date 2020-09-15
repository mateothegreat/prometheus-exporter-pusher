# Create AWS VPC

Features:

* Creates (optional) peering connection(s).
* Supports tagging for ALL resources.


This role will create a new AWS VPC including:

* Peering Connection(s)
* Internet Gateway
* NAT Gateway(s)
* Route Table(s)
* Subnet(s)

## Requirements

```bash
pip install ansible boto3 boto
```
## Variables

```yaml
prometheus_exporter_pusher:
  gateway_server_url: "http://monitoring.com:9091"
  user: "prometheuspusher"
  group: "prometheuspusher"
```

## Example Usage

Add the following to a file like `playbook.yaml`:

```yaml
- hosts: monitoring
  roles:
    - role: "mateothegreat.prometheus_exporter_pusher"
      vars:
        prometheus_exporter_pusher:
          gateway_server_url: "http://monitoring.com:9091"
          user: "prometheuspusher"
          group: "prometheuspusher"

```

Run with `ansible-playbook -i <your inventory file> playbook.yaml`.

# Contact

You can reach out to me at https://matthewdavis.io.
