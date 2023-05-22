# Deterministic UUID

In the context of UUIDs (Universally Unique Identifiers), "deterministic" means that a UUID generated using a specific namespace and input data will always produce the same UUID.

Versions 3 and 5 of the UUID algorithm are deterministic, as they use a combination of a namespace identifier and a name or input string to generate the UUID. The resulting UUID is always unique and based on the input data and the namespace, which means that if the same input data is used with the same namespace, the resulting UUID will always be the same.

This deterministic behavior is useful in certain applications where it is important to generate unique identifiers that are consistent across different systems and processes. For example, if two systems need to exchange data and use UUIDs as identifiers, they can use the same namespace and input data to generate UUIDs that are guaranteed to be the same, even if they are generated on different systems.

It is worth noting that not all UUID versions are deterministic. For example, version 4 UUIDs are generated using a random number generator, which means that they are not deterministic and will be different every time they are generated.
