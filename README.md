```mermaid
graph TB
  subgraph "Trainee/Researcher User Flow"
    A1[User comes to BWS]
    A2[Browse Tutorials and Training Topics]
    A3[Choose Workshop]
    A4[Launch Workshop]
    A1-->A2
    A2-->A3
    A3-->A4
  end
  subgraph "Workshop Author User Flow"
    B1[User comes to BWS]
    B2[Launch Authoring Environment]
    B3[Access Data and Pre-compiled Software Packages]
    B4[Author Workshop Material]
    B5[Publish Training]
    B1-->B2
    B2-->B3
    B3-->B4
    B4-->B5
  end
  subgraph "Package Developer User Flow"
    C1[User comes to BWS]
    C2[Launch Developing Environment]
    C3[Access Data, GPUs, CPUs]
    C4[Create New Software Packages]
    C5[Publish Software Package]
    C1-->C2
    C2-->C3
    C3-->C4
    C4-->C5
  end
  B5-->|Published Workshop Material|A2
  C5-->|Published Software Package|B3
  ```
