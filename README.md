# BlockPro
Mission: Open, decentralized, permissenless and trustless protocol for energy consumers and suppliers

![Consollino Prosumer Node](./Consollino.png)

# Modules
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
      - shows total amount of produced/consumend KW/h of the meter
      - shows total amount of produced/consumend KW/h in the last hour, today, yesterday, this week, this month, this year, last year, etc.
      - visualizes the data in diagrams
      - shows the balance in DOI
      - shows sold / bought KWH-Token (this hour, last hour, next hour, today, yesterday, tomomrrow, this week, last week, next week, ...)
      - integrates the decentralized "KW-Token" Exchange
      - integrates a hardware wallet to store Doicoin (e.g. Nano-Ledger) and sign KWH-Deals in teh "KW-Tokeen" Exchange
  - BlockPro meter and node certification procudure done by the electrician
      - the electrician signs a Doichain transaction which adds the new BlockPro node as 'valid' by him e.g. through a 'name_doi bp/meterNo' record on Doichain on consumer nodes can verify such a node as they trust the electrician
      - any electrician can form an organization on the Doichain by adding a name_doi transaction on Doichain e.g. via 'name_doi bp_organization/OrganizationName value: ipfs-hash of a file which contains the list of publicKeys of electrician members'
      - Consumer and Producer are accepting an organization which allows them to trustlessly buy and sell KW-Tokens (see exchange)
3. **Meter Reading module**
  - is a software module installed on a RaspberryPi which connects in a defined time to the meteor and reads the produced and consumed KW/h
  - since these data are coming unsigned from the meteor we need to seal the RaspberryPi together with the meter
  - the read data are written into a file on ipfs the resulting hash is to another cumulative file containing the read data from the last hour (or 30 minutes etc.)
4. **The KW-Token**
  - When writing the produces and/or consumend kw/h into IPFS the resulting hash of the latest cumulative file must be writen into blockchain. 
  - this can be done by executing name_doi command with nameId bp-meter/meterNo and as value the amount of produced (e.g. +30 KW/h) or consumed (e.g. -1 KW/h)
  - this transaction also includes the IPFS-hash which contains the detail kw/h meteor proofs
  - listing all name_doi transactions of a meteor by calling name_list bp-meter/meterNo would calculate total balance of kwh
5. **Nano-Ledger App für Doichain**
6. **Decentralized "KW-Token" Exchange**
7. **Other tasks & thoughts**
  - Rebranding Doichain
  - tDOI on Ethereum blockchain and other trojan horses to buy and sell DOI (see and fork: https://tbtc.network/) 
  - Should KWH/Token be possible to directly be sold on other crypto exchanges? Is that at all possible or even useful? 
8. **Attack Scenarios**
  - 51% Blockchain attack
9. Other blockchain based projects
  - EnergyWeb http://energyweb.org/
