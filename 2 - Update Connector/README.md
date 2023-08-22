# Update steps connector running in Docker

1. Check the connector version deployed in the host
   * Use the following command: `docker exec twingate-connector ./connectord --version`
   * > change _**twingate-connector**_ with connector name deployed (container) in the host
   * ![Check version](Pictures/Update(1).png)
  
     
2. Check connector release notes
   * > [https://www.twingate.com/changelog/connector](https://www.twingate.com/changelog/connector)
     
     
3. Check the upgrade script
   * > curl -s https://binaries.twingate.com/connector/docker-upgrade.sh | sudo nohup sudo bash
   * ![Upgrade script](Pictures/Update(2).png)
   * > Remote connection will temporarily be disconnected if doing this remotely from outside network (via Twingate NAT-T)
     
      
4. Verify the upgraded connector
   * 1.56.0 upgraded to 1.58.0 (released on 13 Aug 2023)
   * > Date of commit to this version / upgrade container : 23 Aug 2023
   * ![Upgraded connectors](Pictures/Update(3).png)

# References:
- https://www.twingate.com/docs/upgrading-connectors
- https://www.twingate.com/docs/docker
