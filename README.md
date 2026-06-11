# Lineage2TS
Lineage2TS is an extensible server platform to create a HighFive server. Written in Typescript and Zig, and runs as Node.js applications. Aim of the project is to provide a self-hostable server for L2 HighFive client for protocol versions 267, 268, 271 and 273.

Repository with code and artifacts is available at https://gitlab.com/MrTREX/lineage2ts
Project is open-source using `AGPL-3.0-or-later` license.

Project aims to:
- **Preserve multiplayer functionality** for L2 HighFive client using modern technologies
- **Document decades-old lore and gameplay** that was previously undocumented or poorly understood
- **Empower players** with ownership and control over their gaming infrastructure, servers running on multiple CPU architectures and OS
- **Provide working reference implementation** for researchers and developers interested in exploring login/game/proxy server platform architecture

Project covers the following areas of server development:
- game server where virtual world contains all player interactions along with quests and npcs, supports H5 client
- login server where client verification and authorization is possible to allow player account interactions, supports H5 client
- cli for static asset generation and data provisioning operations (datapack and geopack generation)
- server-testing where programmatic verification of client-server behavior can be codified
- proxy for programmatic MITM proxy, supporting multiple concurrent L2 clients (Interlude or HighFive protocols)
- desktop GUI for managing and interacting with Lineage2TS server infrastructure

Project uses unique MMO testing:
- custom-written **programmatic client for HighFive protocol** for login and game server packets
- running **more than 1000 concurrent end-to-end tests** to simulate game client interactions with game and login servers
- tests cover **player-vs-environment interactions** like creating characters, interacting with various items, character level up progression or even testing quest outcomes
- advanced tests target **player-vs-player interactions** like trading, crafting and player group activities

Standalone Windows or Linux server installation files are available (x64/arm64) in addition to OCI images for x64/arm64 cpu architectures.
