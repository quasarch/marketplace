# marketplace

Marketplace is a Quasarch curated list of public made containers, lambdas, and VMs people can use to deploy through [Quasarch Console](#). Please submit a pull request if you want to add any more containers that might be helpful to other developers.

Deployments must be of type:

```json
{
  "name": "name",
  "container": {
    "image": "image",
    "tag": "tag",
    "command": "bash script.sh",
    "arguments": ["arg1", "arg2"]
  },
  "resources": {
    "cpu": 1,
    "memory": "512Mi",
    "ephemeralStorage": "10Gi",
    "gpu": {
      "cores": 1,
      "type": "Nvidia h100"
    }
  },
  "ports": [
    {
      "container": 80,
      "external": 80,
      "protocol": "udp"
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

## Contributing

We are always looking for more contributions to our marketplace. If you have a container, lambda, or VM that you think would be helpful to other developers, please submit a pull request following the format above.

We support Metadata for each deployment. This is an additional JSON parameter that can be added to the deployment to provide more information about the deployment. This is optional, but we encourage you to add metadata to your deployments.

```json
{
  ...<other deployment parameters>
  "metadata": {
    "version": "1.0.0"
    "tags": ["tag", "tag2"],
    "description": "Description of the deployment.",
  }
}
```

Add a logo with the filename `logo.png` to the root of the deployment folder. This will be displayed in the Quasarch Console.

Join our [Discord](https://discord.gg/gc9X3VhXJ8) to stay in the loop with updates and announcements of Quasarch. Our team is always eager to hear from you.
