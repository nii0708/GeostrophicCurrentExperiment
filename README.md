# GeostrophicCurrentExperiment
Geostrophic currents, driven by a balance between the Coriolis force and pressure gradients, are pivotal in shaping our planet. They act as the ocean's circulatory system, transporting heat from equatorial regions to higher latitudes, influencing global climate patterns. These currents also play a crucial role in marine ecosystems by facilitating nutrient upwelling, supporting biodiversity, and impacting fisheries. Furthermore, they are essential for navigation, offshore operations, and pollution management. In essence, geostrophic currents are the underlying force driving much of the ocean's dynamics, with far-reaching consequences for our planet and human activities

This study investigates the prediction of geostrophic current velocities for the next seven days using three distinct machine learning models: MLP (Multi Layer Perceptrons), a GraphSage-based model, and a Multilayer Perceptron Fourier Neural Operator (MLP-FNO). By comparing the performance of these models, we aim to determine the most effective approach for forecasting geostrophic currents within a week's timeframe.

Methods:

- I constructed a dataset from the CDS [https://cds.climate.copernicus.eu/cdsapp#!/dataset/satellite-sea-level-global] with the following geographical constraints: latitude between 9.125° N and 13.375° S, and longitude between 93.875° E and 142.375° E. The time span covers data from January 1, 2013, to December 31, 2021. Since the datasets were in .nc format, I pickled them after converting them into dictionaries for easier manipulation.   

- I use three models to compare Multi-Layer Perceptrons (MLP), a GraphSage-based model, and a Multilayer Perceptron Fourier Neural Operator (MLP-FNO). Each model is trained with both Mean Squared Error (MSE) and a custom loss function (Gopakumar et al., 2024).

Modified MLP-FNO:
![image](https://github.com/user-attachments/assets/1eb0d9dd-5bcf-41b4-9c7b-d1298d32a968)
Graph based architecture:
![image](https://github.com/user-attachments/assets/195bb700-5aac-4162-9da5-fab4f64f97ed)



References:
Gopakumar, V., Pamela, S., Zanisi, L., Li, Z., Gray, A., Brennand, D., ... & MAST Team. (2024). Plasma surrogate modelling using Fourier neural operators. Nuclear Fusion, 64(5), 056025.

Hamilton, W., Ying, Z., & Leskovec, J. (2017). Inductive representation learning on large graphs. Advances in neural information processing systems, 30.

Li, Z., Kovachki, N., Azizzadenesheli, K., Liu, B., Bhattacharya, K., Stuart, A., & Anandkumar, A. (2020). Fourier neural operator for parametric partial differential equations. arXiv preprint arXiv:2010.08895.

Copernicus Climate Change Service, Climate Data Store, (2018): Sea level gridded data from satellite observations for the global ocean from 1993 to present. Copernicus Climate Change Service (C3S) Climate Data Store (CDS). DOI: 10.24381/cds.4c328c78

Qin, S., Lyu, F., Peng, W., Geng, D., Wang, J., Gao, N., ... & Wang, L. L. (2024). Toward a Better Understanding of Fourier Neural Operators: Analysis and Improvement from a Spectral Perspective. arXiv preprint arXiv:2404.07200.

