## Highlights

- Start with higher level protocol design
    - Think in terms of integrating with SCION
    - Also think about what fields would be required inside packet header

- TCP would be need special care
    - Associating APNA session with TCP session
    - EphIDs flow based

- Socket API design
    - Think about users could express EphIDs ex: per-flow based, per-packet based
    - Also thinks about how users could express what sort of EphIDs they want?

- Privacy Implication
    - Compare per-flow based vs per-packet based EphIDs
    - Building some concrete mathematical models

