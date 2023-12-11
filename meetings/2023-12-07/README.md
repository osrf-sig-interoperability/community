# 07 December 2023
[Meeting Recording](https://drive.google.com/file/d/1BU5qDUPzS9jNvdCX3A-Gvh7Q30xlEgKx/view?usp=drive_link)

## Agenda

- Andrei Ionescu: ISO/WD 21423 Introduction [Slides Here](https://docs.google.com/presentation/d/1e5HNCG2qqzCX6pwG_i5tqlUYqB4KJHWPQVC0wqrEGlY/edit?usp=drive_link)
- Grey: Rust for System Integration [Slides Here](https://docs.google.com/presentation/d/1H--iwOXAMW7HdA5tUOGx5TkNJiq6clEcmohb37ECKZs/edit?usp=drive_link)

## Discussion

- Bainian asks about using Rust-implemented code inside of a C++ program
- Grey refers Bainian to [corrosion](https://corrosion-rs.github.io/corrosion/)
- Bainian asks about how Open-RMF will be transitioning to Rust
- Grey explains some details about the migration plans that
  - Some nodes/components, such as the Reservation System, could be migrated over to Rust entirely
  - The `rmf_fleet_adapter` C++ API will remain available and its implementation will be replaced with a Rust implementation
  - New (hopefully better) SDKs for all supported languages (Rust, C++, Python) will become available based on the new Rust implementation
- Bainian asks about how the migration will affect traffic negotiation in RMF
- Grey explains that the negotiation implementation has never been stable and is not exposed to the `rmf_fleet_adapter` API, so changes to negotiation will not impact existing fleet integrations
- Bainian asks about stability within the Rust community, e.g. drama related to the Rust Foundation
- Grey responds that he is aware of these events but does not find it concerning overall
  - Drama is not unusual in large open source communities, but the communities generally still thrive
  - All core Rust language software is permissive and open source so no one can pull the rug on the community
  - In the worst case scenario, the language and its tools can be maintained or forked off into something new regardless of the Rust Foundation
