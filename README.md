# Release-Notes

# ICICLE Release 2023-06

The ICICLE team aims to build the next generation Cyberinfrastructure (CI) to render Artificial Intelligence (AI)
more accessible to everyone and to drive its democratization further in solving larger societal problems. 

It is with great pleasure that we announce ***2023-06*** release of ICICLE CI components.

This release includes the following components:

# New to ICICLE CI Catalog
## Intelligent Cyberinfrastructure
### AI Foundations
- **ICICLE Foodshed Parser v0.1**
    - A Conversational AI model, which users can interact with it regarding food insecurity queries. The model responds with a list of commands in which an agent-based model can be run to simulate food insecurity levels in a given region.

- **Species Classification using Multimodal Heterogeneous Context v0.1.0**
    - A species classification model that utilizes heterogeneous image contexts organized in a multimodal knowledge graph. The multimodal knowledge graph may include diverse forms of heterogeneous contexts that pertain to different modalities, such as numerical information for locations and time, categorical data for species/taxon IDs, and visual content such as images.

- **Region2vec v1.0**
    - Region2vec is a Community Detection algorithm on Spatial Networks that uses graph embeddings with node attributes and spatial interactions. Region2vec first generates node embeddings for regions that share common attributes and have intense spatial interactions, and then applies clustering algorithms to detect communities based on their embedding similarity and geographic adjacency.

### Software Architecture and Design
- **Tapis Federated Authentication Service v1.3.4**
    - The Tapis Federated Authentication Service provides OAuth2-based authentication module that allows third-party applications to authenticate users from different identity providers. Including university credentials, HPC center accounts (e.g., TACC accounts), and web and social login (e.g., GitHub, Google, etc).

- **ICICONSOLE v0.0.10**
    - First a part of Hello ICICLE Authentication Clients v0.0.1, ICICONSOLE is now a PyPI package. The command line interface (CLI) tool to authenticate with the Tapis Pods service. The tool allows the user to manage, operate, and interactively explore Tapis services.

- **TapisCL-ICICLE v0.1.4**
    - The ICICLE CLI tool to interact with Tapis is officially its own component coming from Hello ICICLE Authentication Clients v0.0.1. TapisCL-ICICLE now utilizes the Tapis Federated Authentication Service.

## Use Inspired Science
### Digital Agriculture
- **ICICLE Digital Agriculture Hub v1.0**
    - The Digital Agriculture Hub is the source for end users to access data-driven, edge services such as aerial scouting and sprayer control, and to initiate cloud jobs for agricultural workloads.

- **Far-Edge Edge Simulator v1.0**
    - This tool is used to simulate power demands, cpu usage and other far-edge metrics for aerial missions. You can use Far-Edge Edge Simulator by visiting the Digital Agriculture Hub and selecting the "Far-Edge Edge Simulator" tab.

- **In-Field Helper for Crop Scouts v1.0**
    - Given (1) a set of agricultural images labeled by a neural network and (2) a set of images on a new field, this tool explains to scouts if the images of the new field fully vet the neural network. Go to the Digital Agriculture Hub and select the "In-Field Helper for Crop Scouts" tab to use this tool.

### Smart Foodsheds
- **Persons-Projects-Organizations-Datasets California (PPOD_CA) Knowledge Graph v23.06**
    - PPOD_CA is a knowledge graph of PPOD information describing connections between environmental conservation and the food system in California.

- **Kroger Store Closure  v0.1**
    - This prototype web application provides users with an engaging and interactive platform to explore an agent-based model. The model allows for dynamic simulations and captures the complex interactions between different types of households and markets. By utilizing this model, users can gain valuable insights into the food insecurity levels experienced by various types of households.

# ICICLE CI Components Changelog
## Intelligent Cyberinfrastructure

### Software Architecture and Design
- **Tapis Pods Service v1.3.2**
    - New features:
      1. Added volume and snapshot support/utils/models/etc. Using nfs pvc storage to volume mount block storage to running pods. Users can share volumes and collaborate live on the same storage. Snapshots allow users to take copies of volumes for data versioning purposes.
      2. Traefik proxying now automatically creates certificates at runtime for each subdomain (meaning each pod).
      3. Service no longer requires initial, or any, manual certificate creation.
      4. Some edits for Neo4j as it requires a injected cert.
      5. Changes for local dev as it's now different from deployment.
   
- **TapisCL-ICICLE v0.1.4**
    - Changes:
      1.  Added Tapis federated authentication, and device code authentication grant types to allow for more flexible access to Tapis resources. Full revamp of the whole authentication workflow.
      2. Overhaul of user interface and command entry to provide better interactivity with commands that previously required config files to execute properly
      3. More effective command line argument validation to sanitize data input
      4. Overhaul of files and systems to grant user access to additional Tapis resources (WIP). Files and systems strive to emulate linux bash command line, using commands like cd and ls.
      5. Support for Tapis postits added
    - Planned Changes:
      1. Finish upgrading system authentication to fully complete system access
      2. Upgrade app commands and eventually implement intuitive job submission
      3. Refactor help generation code
   
- **ICICONSOLE v0.0.10**
    - Changes:
      1. Improved user interface for select queries. Now, the user can select a query from a list of available queries (help command), and the query will be executed automatically. This works toward an automated process for querying Knowledge Graphs.
      2. For Knowledge Graph queries that return entire node(s), a separate view will be opened to display the node in a more readable format. In this view, scrolling is enabled to see the complete data in the confined space of the terminal.
      3. Minor bug fixes
    - Planned Changes:
      1. Add support for Knowledge Graph queries that return edges
      2. Add automation for creation and deletion within Knowledge Graphs, past read-only operations.
      3. Integrate Tapis federated authentication
      4. Create a natural language interface for querying Knowledge Graphs, which would automate the automation process itself. This would be a long-term goal, and would require a lot of research and development.

## Use Inspired Science
### Animal Ecology
- **Camera-Traps Edge Simulator v0.3.1**
    - Changes:
      1. Support for 2 new power monitoring events
      2. Removal of image_uuid field from ImageLabelScore type used in ImageScoredEvent.
      3. MonitorPowerStartEvent and MonitorPowerStopEvent implemented in Rust (Python support in progress).
      4. The image_store_plugin deletes files of all types associated with an image when that image is deleted.
   
### Visual Analytics
- **Smart Foodsheds Visual Analytics (VA) Dashboard v0.2**
    - New Features:
      1. Added save/load functionalities, allowing users to bring their own data and share data in the future.
    - Changes:
      1. Default graph animation is set to static, providing better placement of the graph within the panel.
      2. Implemented automatic coloring scheme to differentiate between different node types.
      3. Replaced the reset graph function with an undo function, providing a more intuitive experience for users.
      4. Fixed various minor UI issues.
   
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


The ICICLE team is committed to delivering the best software and CI components. We welcome your feedback and suggestions for future releases. A list of all ICICLE components can be found on our website under [CI & Software](https://icicle.ai/cyberinfrastructure/software)

Please subscribe to [icicle-discuss](https://lists.osu.edu/mailman/listinfo/icicle-discuss) and post to discuss all installation/build problems, performance issues, features and other miscellaneous questions related to the different software and CI components of the ICICLE project. You are welcome to post patches and enhancements to the released components.

Subscribe to our mailing list [icicle-announce](https://lists.osu.edu/mailman/listinfo/icicle-announce) to stay up to date on the latest ICICLE news and releases.

## Acknowledgements
*This release is brought to you by the National Science Foundation (NSF) funded AI institute for Intelligent Cyberinfrastructure with Computational Learning in the Environment (ICICLE) (OAC 2112606)*
