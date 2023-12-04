```mermaid
graph TB
  linkStyle default interpolate basis
  subgraph "Trainee/Researcher"
    A1(1. Trainee navigates to BWS)
    A2(2. Browses tutorials and training topics)
    A3(3. Chooses and launches Workshop Environment)
    A4(4. Acquires Bioinformatics/Genomics analysis skills)
    A1-->A2
    A2-->A3
    A3-->A4
  end
  subgraph "Workshop Author"
    B1(1. Workshop author comes to BWS)
    B2(2. Launches Authoring Environment)
    B91{{Has access to data and pre-compiled software packages}}
    B3(3. Authors and tests workshop material)
    B4(4. Publishes training)
    B92>Automatically build Docker container to make workshop deployable]
    B1-->B2
    B2-->B3
    B3-->B4
    B3-.-B91
    B4-.-B92
  end
  subgraph "Package Developer"
    C1(1. Developer comes to BWS)
    C2(2. Launches Developer Environment)
    C91{{Has access to testing data and compute resources: CPUs, high-memory, GPUs}}
    C92{{Can test on all Bioconductor operating systems/chip architectures}}
    C3(3. Creates a new software package)
    C4(4. Publishes software package)
    C1-->C2
    C2-->C3
    C3-->C4
    C3-.-C91
    C3-.-C92
  end
  B4-.->A2
  C4-.->B91
  ```
