# Update steps connector running in Docker

1. Check the connector version deployed in the host
   * Use the following command: `docker exec twingate-connector ./connectord --version`
   * > change _**twingate-connector**_ with connector name deployed (container) in the host
   * ![Check version](Pictures/Update(1).png)
2. Check connector release notes
   * > [https://www.twingate.com/changelog/connector](https://www.twingate.com/changelog/connector)
2. Check the upgrade script
   * > curl -s https://binaries.twingate.com/connector/docker-upgrade.sh | sudo nohup sudo bash
   * * ![Upgrade script](Pictures/Update(2).png)

# References:
- https://www.twingate.com/docs/upgrading-connectors
- https://www.twingate.com/docs/docker
