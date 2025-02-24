### The following list gets rendered on this page: [sukhdeep.tech/list](http://sukhdeep.tech/list)

---
## 2025-02-23
- **Blog** **[Uber]**: [Engineering Uber Predictions in Real Time with ELK](https://www.uber.com/en-IN/blog/elk/)
  > Uber enhanced its user experience across its product portfolio by creating a **custom prediction system** using the open-source ELK stack (Elasticsearch, Logstash, and Kibana) to provide precise and interpretable forecasting for engineering and operations. This system uses an **online k-nearest neighbors algorithm (KNN)**, leveraging both historical and real-time trip data to predict patterns like trip density and match rate. The architecture includes data pipelines using Kafka and Hive for real-time queries and analytics, a training service for parameter selection, and a configuration service to serve actionable parameters to the prediction service. To handle Uber's scale, the system was optimized for horizontal scalability, incorporating hexagonal queries to reduce query size and virtual clusters to overcome limitations of single cluster architecture. Key lessons learned include the importance of provisioning sufficient resources, organizing data logically, and ordering Elasticsearch queries efficiently. The real-time prediction system has been implemented across **400 cities worldwide**.

## 2025-02-21
- **Blog** **[Uber]**: [H3: Uber's Hexagonal Hierarchical Spatial Index](https://www.uber.com/en-IN/blog/h3/)
  > Uber developed **H3, a hexagonal, hierarchical spatial index**, a system that uses hexagons to divide up maps, helping them analyze location data for things like setting ride prices and understanding city-wide trends. Instead of using traditional squares or irregular shapes like zip codes, H3 uses hexagons because they better represent movement and distance. This system helps Uber understand where demand is high and optimize services. H3 combines a **hexagonal grid** with a **hierarchical system** that divides the world into 122 base cells, also including twelve pentagons to make the system work on a sphere. It offers **sixteen levels of detail**, allowing Uber to zoom in or out as needed. The H3 system is available for anyone to use and can convert locations into a special code for easy analysis.

## 2025-02-20
- **Blog** **[Meta]**: [Revolutionizing software testing: Introducing LLM-powered bug catchers](https://engineering.fb.com/2025/02/05/security/revolutionizing-software-testing-llm-powered-bug-catchers-meta-ach/)
  > Meta's Automated Compliance Hardening (ACH) tool utilizes LLMs to improve software testing by generating mutants (undetected faults) in source code and creating tests to catch these specific faults, thereby hardening platforms against regressions. Unlike traditional methods that focus on increasing code coverage, ACH targets specific faults described in plain text, even if the descriptions are incomplete or contradictory. This approach combines LLM-based test generation and mutant generation, which had previously been difficult to scale, to efficiently convert concerns from various sources into actionable tests. ACH has been applied to platforms like Facebook Feed, Instagram, Messenger, and WhatsApp, proving useful for hardening code against specific concerns and providing additional benefits even when tests don't directly tackle a specific concern. **This system simplifies risk assessments, reduces cognitive load for developers, and enhances the safety of the online ecosystem by automating complex technical organizational workflows**.

## 2025-02-19
- **Blog** **[Netflix]**: [Introducing Impressions at Netflix](https://netflixtechblog.com/introducing-impressions-at-netflix-e2b67c88c9fb)
  > Netflix utilizes a system that processes billions of impressions daily to personalize content discovery, tracking each movie poster or promotional banner a user hovers over. The system captures raw events from user interactions and relays them to servers, where a custom event extractor identifies and routes impression events to both an Apache Kafka topic for immediate processing and an Apache Iceberg table for long-term storage. An Apache Flink job filters and enriches this data with metadata such as show/movie titles and page/row location, structuring it using an Avro schema to create a definitive source of truth. Netflix processes **1 to 1.5 million impression events every second**, each approximately 1.2KB in size, using Flink with a configuration of 8 task managers per region, each having 8 CPU cores and 32GB of memory, and a parallelism of 48. This system ensures high availability through an 'island model' where dependencies reside within a single region, allowing traffic to shift between regions if one degrades.

## 2025-02-18
- **Blog** **[Farnam Street]**: [The Map Is Not the Territory](https://fs.blog/map-and-territory/)
  > This post emphasizes that **maps, or models, are simplifications of reality and not reality itself**. These maps simplify complexity, such as financial statements or policy documents, to guide us. However, relying solely on maps can lead to errors because they don't capture every detail. **Maps are subjective creations** that reflect the values and limitations of their creators. **Updating maps based on experience is crucial** because territories change, and maps must adapt to remain useful. The post cautions against mistaking the map for the territory, which can lead to inflexibility and poor adaptation to change. **It advises choosing mapmakers wisely** and recognizing that maps can influence the territories they represent.

## 2025-02-16
- **Blog** **[DeepMind]**: [Traffic prediction with advanced Graph Neural Networks](https://deepmind.google/discover/blog/traffic-prediction-with-advanced-graph-neural-networks/)
  > **Supersegments:** Multiple adjacent road segments sharing significant traffic volume. **Graph Neural Networks:** Machine learning architectures that model network dynamics and information propagation. **MetaGradients:** A reinforcement learning technique used to dynamically adapt the learning rate during training. DeepMind partnered with Google Maps to enhance the accuracy of real-time Estimated Times of Arrival (ETAs) for Google Maps, achieving improvements of up to 50% in cities such as Berlin and Jakarta. To predict future traffic, Google Maps uses machine learning to combine live traffic conditions with historical traffic patterns. The collaboration involved using Graph Neural Networks to model road networks as graphs, with road segments as nodes and connections as edges, and dividing road networks into "Supersegments". A key challenge was creating a machine learning system to estimate travel times using Supersegments. To address variability in training, MetaGradients were used to dynamically adapt the learning rate. The system also uses a multi-loss objective, including L_2 and L_1 losses, to avoid overfitting. This collaboration improved the accuracy of ETAs on Google Maps.

## 2025-02-15
- **Blog** **[Netflix]**: [Title Launch Observability at Netflix Scale - Part 2: Navigating Ambiguity](https://netflixtechblog.com/title-launch-observability-at-netflix-scale-19ea916be1ed)
  > This blog post emphasizes that lasting success in technology requires understanding the broader context before problem-solving. Netflix employs a four-step process: identifying stakeholders like title launch operators and product managers, mapping the current landscape to identify areas for improvement, clarifying the core problem of ensuring fair treatment of every title by the personalization stack, and assessing business priorities such as successful title launches and trust with content creators. To foster clarity, Netflix defines "**Title Health**" using metrics to gauge a title's discoverability and member engagement by addressing whether a title is visible to any member, to an appropriate audience size, and to all appropriate audiences. Issues are categorized into title setup (metadata and assets), personalization systems, and algorithms, with setup issues being the most common and easiest to fix, while algorithm issues are rare but difficult. Netflix prioritized proactive issue detection to ensure smoother launches and better member experiences, laying the foundation for a scalable system.

## 2025-02-13
- **Blog** **[Netflix]**: [Title Launch Observability at Netflix Scale](https://netflixtechblog.com/title-launch-observability-at-netflix-scale-c88c586629eb)
  > Netflix invests billions of dollars annually in over a thousand global content launches each month, making the success and discoverability of each title a top priority. The challenge involves tracking title-specific metrics beyond standard system performance indicators. While initially, a manual verification process was used, it became unsustainable as Netflix expanded globally. The company then faced the challenge of answering complex queries about why titles weren't appearing in specific locations or product experiences. To address this, Netflix considered log processing and observability endpoints in personalization systems. Log processing, while imposing a low burden on existing systems, primarily addresses post-launch scenarios and could lead to an exponential increase in logged data. Netflix ultimately adopted a comprehensive observability strategy that includes real-time monitoring and proactive issue detection by introducing observability endpoints across all systems, enabling real-time data flow into a dedicated microservice for title launch observability. While this requires a significant initial investment and carries a synchronization risk, it enhances Netflix's ability to ensure successful title launches and improve the viewing experience.

## 2025-02-12
- **Blog** **[Meta]**: [Sequence learning: A paradigm shift for personalized ads recommendations](https://engineering.fb.com/2024/11/19/data-infrastructure/sequence-learning-personalized-ads-recommendations/)
  > Meta's ad recommendation engine has undergone a transformation from Deep Learning Recommendation Models (DLRMs) that relied on human-engineered features to a system using **sequence learning** with **event-based features (EBFs)** to improve personalized ad delivery. The shift addresses the limitations of DLRMs, such as the loss of sequential and granular information, reliance on human intuition, and redundant feature spaces. The new system uses EBFs, which standardize heterogeneous inputs, incorporate rich information about events (like ad categories and timestamps), and replace legacy sparse features. **Event models** synthesize event embeddings, and **sequence models** use attention mechanisms to understand a person's behavior over time. This new approach has led to improved ad prediction accuracy, resulting in **2-4% more conversions on select segments**. The focus going forward involves scaling event sequences, developing more efficient sequence modeling architectures, and multimodal enrichment of event sequences.

- **Blog** **[LinkedIn]**: [Behind the platform: the journey to create the LinkedIn GenAI application tech stack](https://www.linkedin.com/blog/engineering/generative-ai/behind-the-platform-the-journey-to-create-the-linkedin-genai-application-tech-stack)

## 2025-02-07
- **Blog** **[Netflix]**: [Evolving from Rule-based Classifier: Machine Learning Powered Auto Remediation in Netflix Data Platform](https://netflixtechblog.com/evolving-from-rule-based-classifier-machine-learning-powered-auto-remediation-in-netflix-data-039d5efd115b)
- **Blog** **[Canva]**: [Real-time mouse pointers](https://www.canva.dev/blog/engineering/realtime-mouse-pointers/)
- **Blog** **[Netflix]**: [Netflix's Distributed Counter Abstraction](https://netflixtechblog.com/netflixs-distributed-counter-abstraction-8d0c45eb66b2)

## 2025-02-04
- **Blog** **[DoorDash]**: [How DoorDash Standardized and Improved Microservices Caching](https://doordash.engineering/2023/10/19/how-doordash-standardized-and-improved-microservices-caching/)
- **Blog** **[Dropbox]**: [Implementing end-to-end encryption for Dropbox teams](https://dropbox.tech/security/end-to-end-encryption-for-dropbox-teams)

## 2025-02-02
- **Blog** **[Meta]**: [How Meta built Threads in 5 months](https://engineering.fb.com/2023/11/06/android/how-meta-built-threads-in-5-months/)
- **Blog** **[DoorDash]**: [DoorDash Empowers Engineers with Kafka Self-Serve](https://doordash.engineering/2024/08/13/doordash-engineers-with-kafka-self-serve/)

## 2024-12-30
- **Blog** **[Netflix]**: [Video annotator: a framework for efficiently building video classifiers using vision-language models and active learning](https://netflixtechblog.com/video-annotator-building-video-classifiers-using-vision-language-models-and-active-learning-8ebdda0b2db4)

## 2024-12-28
- **Blog** **[Slack]**: [How We Built Slack AI To Be Secure and Private](https://slack.engineering/how-we-built-slack-ai-to-be-secure-and-private/)

## 2024-12-25
- **Blog** **[Discord]**: [Developing Rapidly With Generative AI](https://discord.com/blog/developing-rapidly-with-generative-ai)

## 2024-12-24
- **Blog** **[LinkedIn]**: [How data is powering skills-based hiring on LinkedIn](https://www.linkedin.com/blog/engineering/talent/how-data-is-powering-skills-based-hiring-on-linkedin)

## 2024-12-22
- **Blog** **[Meta]**: [Building Meta's GenAI Infrastructure](https://engineering.fb.com/2024/03/12/data-center-engineering/building-metas-genai-infrastructure/)

## 2024-12-21
- **Blog** **[LinkedIn]**: [Musings on building a Generative AI product](https://www.linkedin.com/blog/engineering/generative-ai/musings-on-building-a-generative-ai-product)
