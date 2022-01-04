
## :chart_with_upwards_trend: [An answer for programmable GPU graph anaytics.](https://github.com/gunrock/gunrock)
Gunrock is a GPU Graph Analytics library developed by our research group at University of California, Davis. Originated from a DARPA project, Gunrock has become a fully featured library with extensive support for variety of different graph applications on the GPU[^1].

- [RAPIDS](https://rapids.ai/)
- [NVIDIA Accelerated Libraries](https://developer.nvidia.com/gpu-accelerated-libraries)

## 🤓 Understanding gunrock.
A simple way to understand Gunrock's programming model is to understand its *frontier* abstraction. A frontier in gunrock is just a group of vertices or edges in a graph, which you can operate on in parallel using operators provided within the library. Gunrock does a great job at abstracting away the complexity of programming fast-performing graph algorithms on the GPU from the actual algorithm you are trying to express.

## 🎉 My contributions to gunrock.
I have been part of the gunrock team since I joined the research group in 2015, and I have learned a lot since then. As a gunrock developer, I will divide my contributions up into different layers library development;

* Project management and infrastructure
* Gunrock's core contributions
* Application-level contributions
* External interface contributions

#### (1) Project management and infrastructure
- Responsible for gunrock major **v1.0** release and other minor releases [[2](#references)]
- Introduced git-forking workflow and code-review using pull requests to the project
- Jenkins central integration
- Google's unit testing framework
- Performance profiling with the help of John
- Gunrock's docs website, and developers documentation
- Addressing github issues (debugging) and code-reviews

#### (2) Gunrock's core contributions
- Helped refactor code along with Yuechao Pan (v1.x)[^2]
- [Gunrock/Essentials](https://github.com/gunrock/essentials): modern C++ based refactor
- Improved load-balancing schemes, more on that later
- Profiling of some of the core kernels
- NVIDIA's architecture tuning for Pascal, Volta and Turing

#### (3) Application-level contributions
- Graph Coloring[^3]
- Geolocation
- Shared-Nearest Neighbors
- K-Nearest Neighbors
- Single-Source Shortest Path (essentials/sssp)
- Advised and code-reviewed several other graph primitives

#### (4) External interface contributions
- Example C/C++ and Python bindings for v1.x
- Unit testing framework

[^1]: Yangzihao Wang, Yuechao Pan, Andrew Davidson, Yuduo Wu, Carl Yang, Leyuan Wang, **Muhammad Osama**, Chenshan Yuan, Weitang Liu, Andy T. Riffel, and John D. Owens. **Gunrock: GPU Graph Analytics.** ACM Transactions on Parallel Computing, 4(1):3:1–3:49, August 2017.
[^2]: Gunrock: GPU Graph Analytics (url: https://github.com/gunrock/gunrock/releases)
[^3]: **Muhammad Osama**, Minh Truong, Carl Yang, Aydin Buluç and John D. Owens. **Graph Coloring on the GPU.** In Proceedings of the 33rd IEEE International Parallel and Distributed Processing Symposium Workshops, IPDPSW '19, pages 231–240, May 2019.
