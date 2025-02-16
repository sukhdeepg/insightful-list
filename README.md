## 2025-02-16
- **Blog**: [Traffic prediction with advanced Graph Neural Networks](https://deepmind.google/discover/blog/traffic-prediction-with-advanced-graph-neural-networks/)
  > * **Supersegments:** Multiple adjacent road segments sharing significant traffic volume.
  > * **Graph Neural Networks:** Machine learning architectures that model network dynamics and information propagation.
  > * **MetaGradients:** A reinforcement learning technique used to dynamically adapt the learning rate during training.
  >  
  > DeepMind partnered with Google Maps to enhance the accuracy of real-time Estimated Times of Arrival (ETAs) for Google Maps, achieving improvements of up to 50% in cities such as Berlin and Jakarta. To predict future traffic, Google Maps uses machine learning to combine live traffic conditions with historical traffic patterns. The collaboration involved using Graph Neural Networks to model road networks as graphs, with road segments as nodes and connections as edges, and dividing road networks into "Supersegments". A key challenge was creating a machine learning system to estimate travel times using Supersegments. To address variability in training, MetaGradients were used to dynamically adapt the learning rate. The system also uses a multi-loss objective, including L_2 and L_1 losses, to avoid overfitting. This collaboration improved the accuracy of ETAs on Google Maps.

## 2025-02-15
- **Blog**: [Title Launch Observability at Netflix Scale - Part 2: Navigating Ambiguity](https://netflixtechblog.com/title-launch-observability-at-netflix-scale-19ea916be1ed)
  > This blog post emphasizes that lasting success in technology requires understanding the broader context before problem-solving. Netflix employs a four-step process: identifying stakeholders like title launch operators and product managers, mapping the current landscape to identify areas for improvement, clarifying the core problem of ensuring fair treatment of every title by the personalization stack, and assessing business priorities such as successful title launches and trust with content creators. To foster clarity, Netflix defines "**Title Health**" using metrics to gauge a title’s discoverability and member engagement by addressing whether a title is visible to any member, to an appropriate audience size, and to all appropriate audiences. Issues are categorized into title setup (metadata and assets), personalization systems, and algorithms, with setup issues being the most common and easiest to fix, while algorithm issues are rare but difficult. Netflix prioritized proactive issue detection to ensure smoother launches and better member experiences, laying the foundation for a scalable system.

## 2025-02-13
- **Blog**: [Title Launch Observability at Netflix Scale](https://netflixtechblog.com/title-launch-observability-at-netflix-scale-c88c586629eb)
  > Netflix invests billions of dollars annually in over a thousand global content launches each month, making the success and discoverability of each title a top priority. The challenge involves tracking title-specific metrics beyond standard system performance indicators. While initially, a manual verification process was used, it became unsustainable as Netflix expanded globally. The company then faced the challenge of answering complex queries about why titles weren't appearing in specific locations or product experiences. To address this, Netflix considered log processing and observability endpoints in personalization systems. Log processing, while imposing a low burden on existing systems, primarily addresses post-launch scenarios and could lead to an exponential increase in logged data. Netflix ultimately adopted a comprehensive observability strategy that includes real-time monitoring and proactive issue detection by introducing observability endpoints across all systems, enabling real-time data flow into a dedicated microservice for title launch observability. While this requires a significant initial investment and carries a synchronization risk, it enhances Netflix's ability to ensure successful title launches and improve the viewing experience.

## 2025-02-12
- **Blog**: [Sequence learning: A paradigm shift for personalized ads recommendations](https://engineering.fb.com/2024/11/19/data-infrastructure/sequence-learning-personalized-ads-recommendations/)

- **Blog**: [Behind the platform: the journey to create the LinkedIn GenAI application tech stack](https://www.linkedin.com/blog/engineering/generative-ai/behind-the-platform-the-journey-to-create-the-linkedin-genai-application-tech-stack)

## 2025-02-07
- **Blog**: [Evolving from Rule-based Classifier: Machine Learning Powered Auto Remediation in Netflix Data Platform](https://netflixtechblog.com/evolving-from-rule-based-classifier-machine-learning-powered-auto-remediation-in-netflix-data-039d5efd115b)
- **Blog**: [Real-time mouse pointers](https://www.canva.dev/blog/engineering/realtime-mouse-pointers/)
- **Blog**: [Netflix’s Distributed Counter Abstraction](https://netflixtechblog.com/netflixs-distributed-counter-abstraction-8d0c45eb66b2)

## 2025-02-04
- **Blog**: [How DoorDash Standardized and Improved Microservices Caching](https://doordash.engineering/2023/10/19/how-doordash-standardized-and-improved-microservices-caching/)
- **Blog**: [Implementing end-to-end encryption for Dropbox teams](https://dropbox.tech/security/end-to-end-encryption-for-dropbox-teams)

## 2025-02-02
- **Blog**: [How Meta built Threads in 5 months](https://engineering.fb.com/2023/11/06/android/how-meta-built-threads-in-5-months/)
- **Blog**: [DoorDash Empowers Engineers with Kafka Self-Serve](https://doordash.engineering/2024/08/13/doordash-engineers-with-kafka-self-serve/)

## 2024-12-30
- **Blog**: [Video annotator: a framework for efficiently building video classifiers using vision-language models and active learning](https://netflixtechblog.com/video-annotator-building-video-classifiers-using-vision-language-models-and-active-learning-8ebdda0b2db4)

## 2024-12-28
- **Blog**: [How We Built Slack AI To Be Secure and Private](https://slack.engineering/how-we-built-slack-ai-to-be-secure-and-private/)

## 2024-12-25
- **Blog**: [Developing Rapidly With Generative AI](https://discord.com/blog/developing-rapidly-with-generative-ai)

## 2024-12-24
- **Blog**: [Building Meta’s GenAI Infrastructure](https://engineering.fb.com/2024/03/12/data-center-engineering/building-metas-genai-infrastructure/)
- **Blog**: [How data is powering skills-based hiring on LinkedIn](https://www.linkedin.com/blog/engineering/talent/how-data-is-powering-skills-based-hiring-on-linkedin)

## 2024-12-22
- **Blog**: [Building Meta’s GenAI Infrastructure](https://engineering.fb.com/2024/03/12/data-center-engineering/building-metas-genai-infrastructure/)

## 2024-12-21
- **Blog**: [Musings on building a Generative AI product](https://www.linkedin.com/blog/engineering/generative-ai/musings-on-building-a-generative-ai-product)
