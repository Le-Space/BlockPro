# BlockPro
Mission: Open, decentralized, permissenless and trustless protocol for energy consumers and suppliers

![Consollino Prosumer Node](./Consollino.png)

# Module
1. **Blockpro Hardware** (both under one physical seal)
  - BlockPro Prosumer meter
  - BlockPro Light Node (on RaspberryPi)
    - OS and packages
    - Image and installation
2. **BlockPro dApp**
  - BlockPro node & meter onboarding procedure
    - First start scenario and procedure
      - As BlockPro meter and prosumer node are started first time, the dApp generates a private key which mustn't shown to anybody at anytime
      - Meter and node must be sealed together after onboarding procedure from the electrician
      - The dApp's web frontend is available over HTTPS (!) on LAN. official SSL wildcard certificate is needed
      - In parallel the client, the BlockPro meter & node operator is installing the decentralized BlockPro wallet appp on his smartphone or tablet and generates his seed phrase. The wallet connects directly to the meters dApp.
      - The resulting public key can be entered to the BlockPro dApp which produces a 1/2 multisig address between client and BlockPro node address. Produced or consumend energy will be stored on that address from the BlockPro node and can be transfered then via the dencentralized exchange to possible consumers.
      - After physically seeling both BlockPro dervices, the technician has to sign the multisig address on a blockchain
  - BlockPro decentralized wallet (hosted on IPFS)
  - BlockPro meter and node certification procudure done by the electrician
      - the electrician signs a Doichain transaction which adds the new BlockPro node as 'valid' by him e.g. through a 'name_doi bp/meterNo' record on Doichain on consumer nodes can verify such a node as they trust the electrician
      - any electrician can form an organization on the Doichain by adding a name_doi transaction on Doichain e.g. via 'name_doi bp_organization/OrganizationName value: ipfs-hash of a file which contains the list of publicKeys of electrician members'
      - Consumer and Producer are accepting an organization which allows them to trustlessly buy and sell KW-Tokens
 
3. **The KW-Token**
4. **Meter Reading module**
5. **Nano-Ledger App für Doichain**
6. **Decentralized "KW-Token" Exchange**
7. **Other tasks & thoughts**
  - Rebranding Doichain
8. **Attack Scenarios**
  - 51% Blockchain attack
9. Other blockchain based projects
  - EnergyWeb http://energyweb.org/
