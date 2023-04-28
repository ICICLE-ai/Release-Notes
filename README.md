# Release-Notes

## ICICLE Release 2023-04

The ICICLE team aims to build the next generation Cyberinfrastructure (CI) to render Artificial Intelligence (AI)
more accessible to everyone and to drive its democratization further in solving larger societal problems. 

It is with great pleasure that we announce the first release of ICICLE CI components version ***2023-04***.

This release includes the following components:

### Intelligent Cyberinfrastructure
#### AI for CI-for-AI
- **HPC Application Runtime Predictor (HARP) v1.0**
    - The HARP framework is used to generate a history of executions with the help of human-in-loop (pre-defined configurations) and train suitable regression models to estimate the approximate execution time for a targeted application.

- **Intelligent Sparse Library (iSipLib) v1.0**
  - iSipLib is an accelerated sparse kernel library with a PyTorch interface. It aims to provide efficient sparse operations for Graph Neural Network implementations. 
  
#### Software Architecture and Design
- **Base ICICLE Tapis Software v1.3.0**
    - Tapis is a hosted, web-based API framework for securely managing computational workloads across infrastructure and institutions so that experts can focus on their research instead of the technology.
  
- **Event Engine v0.2.0**
    - The Event Engine is a framework for edge simulators and for writing event-based applications in *Rust*. The Event Engine utilizes a *plugin* architecture so that they can be written in multiple languages.

- **Hello ICICLE Authentication Clients v0.0.1**
    - Hello ICICLE Authentication consists of two command line interface (CLI) tools to authenticate with the Tapis Pods service. The first tool, ICICONSOLE, is specifically tailored to working with Neo4j databases hosted through the Tapis Pods. The second tool, TapisCL-ICICLE, allows the user to manage, operate, and interactively explore Tapis services.
  
- **Tapis Pods Service v1.3.0**
    - The Tapis Pods Service provides a web service and distributed platform providing Pods-as-a-Service platform via Kubernetes.  The primary use of this service is to provide quick to deploy long-lived services based on Docker images that are exposed via HTTP or TCP endpoints. 

- **CI Components Catalog v0.1.0**
    - Hosted using our Tapis Pods Service, the CI Components Catalog showcases the most up-to-date released ICICLE CI components available to the public.

### Use Inspired Science
#### Animal Ecology
- **Camera-Traps Edge Simulator v0.3.0**
    - Both a simulator and an edge device application for classifying images with the first deployment specializing in wildlife images. The Camera-Traps Edge Simulator utilizes the Event Engine to implement its *plugin* architecture and *event-driven* communication.
  
#### Digital Agriculture
- **SoftwarePilot v1.2.5**
    - SoftwarePilot is an open-source middleware and API that supports aerial applications. It allows users to connect consumer Parrot Anafi drones and access the drone's flight controller, camera, and navigation system via Python scripts. SoftwarePilot can also communicate with applications via a REST API and built-in Docker integration.
  
#### Smart Foodsheds
- **Persons-Projects-Organizations-Datasets (PPOD) Schema v0.9.1**
    - A LinkML schema for a version of the PPOD (Persons-Projects-Organizations-Datasets) data pattern that describes resources being cataloged by the UC Davis Food Systems Lab. These resources are pertinent to California foodsheds and conservation activities and include lists of organizations, people, programs, projects, tools, datasets, guidelines, and mandates.

- **Smart Foodsheds Visual Analytics (VA) Dashboard v0.1**
    - Hosted using our Tapis Pods Service, the Smart Foodsheds VA Dashboard is a visual analytics system built for smart foodsheds that offers a dynamic and engaging way to explore graph data. The dashboard currently has access to PPOD and Cold Chain datasets. 


The ICICLE team is committed to delivering the best software and CI components. We welcome your feedback and suggestions for future releases. 

Please subscribe to [icicle-discuss](https://lists.osu.edu/mailman/listinfo/icicle-discuss) and post to discuss all installation/build problems, performance issues, features and other miscellaneous questions related to the different software and CI components of the ICICLE project. You are welcome to post patches and enhancements to the released components.

Subscribe to our mailing list [icicle-announce](https://lists.osu.edu/mailman/listinfo/icicle-announce) to stay up to date on the latest ICICLE news and releases.

## Acknowledgements
*This release is brought to you by the National Science Foundation (NSF) funded AI institute for Intelligent Cyberinfrastructure with Computational Learning in the Environment (ICICLE) (OAC 2112606)*
