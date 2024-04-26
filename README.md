# container-marketplace

Container Marketplace is a Quasarch curated list of public made containers people can use to deploy through [Quasarch Console](#). Please submit a pull request if you want to add any more containers that might be helpful to other developers.

Deployments must be of type:

```json
{
  "name": "name",
  "container": {
    "image": "image:tag",
    "command": "bash script.sh",
    "arguments": ["arg1", "arg2"]
  },
  "resources": {
    "cpu": 1,
    "memory": 512,
    "gpu": {
      "cores": 1,
      "type": "Nvidia h100"
    }
  },
  "ports": [
    {
      "containerPort": 80,
      "ExternalPort": 80
    }
  ],
  "env": [
    {
      "name": "ENV_VAR",
      "value": "value"
    }
  ]
}
```

Join our [Discord](https://discord.gg/gc9X3VhXJ8) to stay in the loop with updates and announcements of Quasarch. Our team is always eager to hear from you.
