[![status](https://img.shields.io/badge/status-Open-blue?style=for-the-badge&logo=appveyor)](https://img.shields.io/badge/status-Open-blue)

A preliminary diagram for the components and the flow of data around them was shared in the [introduction](https://satyarat.github.io/home). Let me reuse it here.

![](https://satyarat.github.io/assets/images/diagram.png)

As a list this would be:

- An immutable data storage system
- CLC/Server (serving API, encrypt, decrypt, DB interaction)
- Queue (decoupling between server and agent)
- Agent (peer connection, sync operations)
- UI (based on API)
- Forge (provide binaries, maintain list of valid nodes)
