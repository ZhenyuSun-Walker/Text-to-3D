

# Awesome Text-to-3D Plus
Una colección de métodos recientes sobre la generación 3D a partir de descripciones de texto.
Principalmente existen 2 tipos de métodos para la generación de texto a 3D:

- **Generación Directa de Extremo a Extremo**
(Hay múltiples pasos internos, pero son transparentes para el usuario)
    - inicializar una disposición inicial a partir de texto, y luego refinarla/inpainting
    - generar una escena local a partir de texto, y luego expandirla/optimizarla 
- **Generación Secuencial en Múltiples Etapas**
(Cada paso interno tiene una salida independiente que sirve como entrada para la siguiente etapa)
    - reconstrucción basada en modelos de texto a imagen y modelos de estimación de profundidad
    - reconstrucción basada en los modelos de generación multi-vista a partir de texto
    - reconstruir una escena primitiva a partir de un modelo de texto a imagen, y luego expandirla gradualmente y alinear características

Este repositorio se centra en el enfoque de Generación Secuencial en Múltiples Etapas, y en la generación de escenas 3D. Para el otro tema, consulta las colecciones integrales listadas en [Repositorios y Sitios Web Relacionados](##Related-Repos-and-Websites) al final de este archivo. No dudes en enviar una pull request si tienes artículos relevantes para añadir.

Otros repositorios:

-   **[Text-to-3D](https://paperswithcode.com/task/text-to-3d)** para una colección cuidadosamente compilada de artículos de investigación sobre texto a 3D.
-   **[Awesome Text-to-3D](https://github.com/yyeboah/Awesome-Text-to-3D)** para una lista curada de texto a 3D.

> **Acerca de las abreviaturas:** En la lista a continuación: **<span style="color: hsl(20, 100%, 50%);">B</span>** para mejor artículo, **<span style="color: hsl(120, 70%, 50%);">S</span>** para punto destacado, **<span style="color: hsl(190, 100%, 50%);">H</span>** para destacado, **<span style="color: hsl(60, 100%, 50%);">W</span>** para taller.

## Historia

- **2021.06** - **[Text2Mesh: Text-Driven Neural Stylization for Meshes](https://arxiv.org/abs/2112.03221)** **(CVPR 2022) : Este trabajo desarrolla controles intuitivos para editar el estilo de objetos 3D mediante la predicción de color y detalles geométricos locales basados en una indicación de texto objetivo.
- **2021.12** - **[DreamField: Zero-Shot Text-Guided Object Generation with Dream Fields](https://arxiv.org/abs/2112.01455)** **(CVPR 2022) : Este artículo utiliza un marco de optimización de dos etapas para crear modelos de malla 3D de alta calidad en menos tiempo.
- **2022.09** - **[DreamFusion: Text-to-3D using 2D Diffusion](https://arxiv.org/abs/2209.14988)** **(ICLR 2023) : Este artículo introduce un método para generar objetos 3D utilizando modelos de difusión 2D.
- **2022.11** - **[Magic3D: High-Resolution Text-to-3D Content Creation](https://arxiv.org/abs/2211.10440)** **(CVPR 2023) : Este artículo introduce un método para generar objetos 3D utilizando modelos de difusión 2D. 
- **2023.03** - **[Fantasia3D: Disentangling Geometry and Appearance for High-quality Text-to-3D Content Creation](https://arxiv.org/abs/2303.13873)** **(ICCV 2023) : Esta investigación se centra en desentrañar la geometría y la apariencia para una creación de contenido 3D de alta calidad.
- **2023.05** - **[HiFA: High-fidelity Text-to-3D Generation with Advanced Diffusion Guidance](https://arxiv.org/abs/2305.18766)** **(ICLR 2024) : Este artículo propone enfoques de muestreo y suavizado holísticos para lograr una generación de texto a 3D de alta calidad en una única optimización de etapa única.
- **2023.10** - **[GaussianDreamer: Fast Generation from Text to 3D Gaussians by Bridging 2D and 3D Diffusion Models](https://arxiv.org/abs/2310.08529)** **(CVPR 2024) : Este artículo introduce un marco de trabajo novedoso diseñado para producir eficientemente activos 3D de alta calidad a partir de indicaciones textuales.
- **2023.11** - **[LucidDreamer: Towards High-Fidelity Text-to-3D Generation via Interval Score Matching](https://arxiv.org/abs/2311.11284)** **(CVPR 2024) (<span style="color: hsl(190, 100%, 50%);">H</span>) : Esta investigación introduce un método novedoso llamado Matching de Puntuación por Intervalos (ISM) para generar modelos 3D de alta fidelidad.
- **2023.11** - **[LucidDreamer: Domain-free Generation of 3D Gaussian Splatting Scenes](https://arxiv.org/abs/2311.13384)** **(arXiv 2023) (<span style="color: hsl(60, 150%, 50%);">1.3k stars!</span>) : Esta investigación introduce un método novedoso llamado Matching de Puntuación por Intervalos (ISM) para generar modelos 3D de alta fidelidad.
- **2024.02** - **[GALA3D: Towards Text-to-3D Complex Scene Generation via Layout-guided Generative Gaussian Splatting](https://arxiv.org/abs/2402.07207)** **(ICML 2024) : Esta investigación introduce un marco de trabajo novedoso para generar complejas escenas 3D a partir de descripciones textuales.
- **2024.04** - **[RealmDreamer: Text-Driven 3D Scene Generation with Inpainting and Depth Diffusion](https://arxiv.org/abs/2404.07199)** **(arXiv 2024) : Esta investigación introduce un modelo para utilizar priors de inpainting y profundidad preentrenados con una robusta inicialización de un modelo de Gaussian Splatting 3D. 
- **2024.06** - **[GradeADreamer: Enhanced Text-to-3D Generation Using Gaussian Splatting and Multi-View Diffusion](https://arxiv.org/abs/2406.09850)** **(arXiv 2024) : Esta investigación introduce un novedoso canal de tres etapas, llamado GradeADreamer, que tiene como objetivo abordar los desafíos comunes en la generación de texto a 3D, como el problema del Janus multi-rostro y el tiempo extendido de generación para activos de alta calidad.
- **2024.07** - **[PlacidDreamer: Advancing Harmony in Text-to-3D Generation](https://arxiv.org/abs/2407.13976)** **(ACM MM 2024) : Esta investigación explora métodos para la consistencia multi-vista y la optimización de detalles.
- **2024.07** - **[ScaleDreamer: Scalable Text-to-3D Synthesis with Asynchronous Score Distillation](https://arxiv.org/abs/2407.02040)** **(ECCV 2024) : Este artículo introduce un método de distilación de puntuación asíncrona para mejorar la calidad de la generación.
- **2024.08** - **[DreamLCM: Towards High-Quality Text-to-3D Generation via Latent Consistency Model](https://arxiv.org/abs/2408.02993)** **(ACM MM 2024) : Este artículo propone un método para mejorar la calidad de la generación 3D a través de un modelo de consistencia latente.

## Artículos

### **2020**
- **2020.02** - **[CDISN: Deep Implicit Surface Network for High-quality Single-view 3D Reconstruction](https://arxiv.org/abs/1905.10711)** **(CVPR 2020)**
- **2020.03** - **[3D Photography using Context-aware Layered Depth Inpainting](https://arxiv.org/abs/2004.04727)** **(CVPR 2020)** 
- **2020.03** - **[Learning Implicit Fields for Generative Shape Modeling](https://arxiv.org/abs/1905.10711)** **(CVPR 2020)**
- **2020.03** - **[Pix2Vox++: Multi-Scale Context-Aware 3D Object Reconstruction from Single and Multiple Images](https://arxiv.org/abs/1901.11153)** **(CVPR 2020)**
- **2020.03** - **[Neural Mesh Flow: 3D Manifold Mesh Generation via Diffeomorphic Flows](https://arxiv.org/abs/2007.10973)** **(CVPR 2020)**
- **2020.03** - **[Neural Scene Flow Fields for Space-Time View Synthesis of Dynamic Scenes](https://arxiv.org/abs/2011.13084)** **(CVPR 2020)**

### **2021**
- **2021.03** - **[Text2Shape: Generating Shapes from Natural Language by Learning Joint Embedding](https://arxiv.org/abs/1803.08495)** **(CVPR 2021)**
- **2021.06** - **[Text2Mesh: Text-Driven Neural Stylization for Meshes](https://arxiv.org/abs/2112.03221)** **(SIGGRAPH 2021)**
- **2021.09** - **[CLIP-Forge: Towards Zero-Shot Text-to-Shape Generation](https://arxiv.org/abs/2110.02624)** **(NeurIPS 2021)**

### **2022**
- **2022.09** - **[DreamFusion: Text-to-3D using 2D Diffusion](https://arxiv.org/abs/2209.14988)** **(ICLR 2023)**
- **2022.11** - **[Magic3D: High-Resolution Text-to-3D Content Creation](https://arxiv.org/abs/2211.10440)** **(CVPR 2023)**

### **2023**
- **2023.03** - **[Fantasia3D: Disentangling Geometry and Appearance for High-quality Text-to-3D Content Creation](https://arxiv.org/abs/2303.13873)** **(ICCV 2023)**
- **2023.05** - **[HiFA: High-fidelity Text-to-3D Generation with Advanced Diffusion Guidance](https://arxiv.org/abs/2305.18766)** **(ICLR 2024)** 
- **2023.08** - **[IT3D: Improved Text-to-3D Generation with Explicit View Synthesis](https://arxiv.org/abs/2308.11473)** **(AAAI 2024)**
- **2023.10** - **[GaussianDreamer: Fast Generation from Text to 3D Gaussians by Bridging 2D and 3D Diffusion Models](https://arxiv.org/abs/2310.08529)** **(CVPR 2024)**
- **2023.11** - **[LucidDreamer: Towards High-Fidelity Text-to-3D Generation via Interval Score Matching](https://arxiv.org/abs/2311.11284)** **(CVPR 2024) (<span style="color: hsl(190, 100%, 50%);">H</span>) : Esta investigación introduce un método novedoso llamado Matching de Puntuación por Intervalos (ISM) para generar modelos 3D de alta fidelidad.
- **2023.11** - **[LucidDreamer: Domain-free Generation of 3D Gaussian Splatting Scenes](https://arxiv.org/abs/2311.13384)** **(arXiv 2023) (<span style="color: hsl(60, 150%, 50%);">1.3k stars!</span>) : Esta investigación introduce un método novedoso llamado Matching de Puntuación por Intervalos (ISM) para generar modelos 3D de alta fidelidad.
- **2023.12** - **[Sherpa3D: Boosting High-Fidelity Text-to-3D Generation via Coarse 3D Prior](https://arxiv.org/abs/2312.06655)** **(CVPR 2024)** 

### **2024**
- **2024.02** - **[GALA3D: Towards Text-to-3D Complex Scene Generation via Layout-guided Generative Gaussian Splatting](https://arxiv.org/abs/2402.07207)** **(ICML 2024)** 
- **2024.04** - **[RealmDreamer: Text-Driven 3D Scene Generation with Inpainting and Depth Diffusion](https://arxiv.org/abs/2404.07199)** **(arXiv 2024)**
- **2024.04** - **[DreamScene360: Unconstrained Text-to-3D Scene Generation with Panoramic Gaussian Splatting](https://arxiv.org/abs/2404.06903)** **(ECCV 2024)**
- **2024.06** - **[GradeADreamer: Enhanced Text-to-3D Generation Using Gaussian Splatting and Multi-View Diffusion](https://arxiv.org/abs/2406.09850)** **（arXiv 2024)**
- **2024.06** - **[Director3D: Real-world Camera Trajectory and 3D Scene Generation from Text](https://arxiv.org/abs/2406.17601)** **(NeurIPS 2024)**
- **2024.07** - **[PlacidDreamer: Advancing Harmony in Text-to-3D Generation](https://arxiv.org/abs/2407.13976)** **(ACM MM 2024)** 
- **2024.07** - **[HoloDreamer: Holistic 3D Panoramic World  Generation from Text Descriptions](https://arxiv.org/abs/2407.15187)**
- **2024.07** - **[ScaleDreamer: Scalable Text-to-3D Synthesis with Asynchronous Score Distillation](https://arxiv.org/abs/2407.02040)** **(ECCV 2024)** 
- **2024.08** - **[DreamLCM: Towards High-Quality Text-to-3D Generation via Latent Consistency Model](https://arxiv.org/abs/2408.02993)** **(ACM MM 2024)**
- **2024.08** - **[SceneDreamer360: Text-Driven 3D-Consistent Scene Generation with Panoramic Gaussian Splatting](https://arxiv.org/html/2408.13711v1)** **(arXiv 2024)**
- **2024.08** - **[LayerPano3D: Layered 3D Panorama for Hyper-Immersive Scene Generation](https://arxiv.org/abs/2408.13252)** **(arXiv 2024)**


## Trabajos en Campos Relacionados
### Generación de escenas a partir de imágenes
- **2024.02** **[WonderJourney: Going from Anywhere to Everywhere](https://arxiv.org/abs/2312.03884)** **(CVPR 2024)** 

### Generación de escenas a partir de vídeos
- **2024.04** **[PhysDreamer: Physics-Based Interaction with 3D Objects via Video Generation](https://arxiv.org/abs/2404.13026)** **(ECCV 2024)** 

## Repositorios y Sitios Web Relacionados
- **[Awesome Text-to-3D](https://github.com/yyeboah/Awesome-Text-to-3D)**
- **[Text-to-3D](https://paperswithcode.com/task/text-to-3d)**
