P-Mut is a training and prediction engine that works with a random forest machine learning algorithm trained on 12 predictive feature. Its prediction engine (PyMut) is developed as python 3 module. It utilizes several well-known libraries for high-performance computation and data handling including NumPy (Oliphant, 2015) and SciPy (Virtanen et al., 2020) for numerical processing, Pandas for data management, Scikit-learn for machine learning, Metplotlib and Seaborn for visualization.

It uses physical properties, protein interactome information, and sequence conservation features derived from UniRef 90 and UniRef 100 cluster databases, along with the physio-chemical properties of amino acids to build neural networks. In its repository, there are graphical and numerical predictions available for 12,141 proteins and on 27,203 diseases. 

The prediction output ranges from 0 to 1, with a threshold of 0.5. A score above or equals to 0.5 indicates disease causing effect, while score below 0.5 indicates a neutral variant. (López-Ferrando et al., 2017).

References:


Oliphant, T. E. (2015). Guide to NUMPY. In CreateSpace Independent Publishing Platform eBooks. https://dl.acm.org/citation.cfm?id=2886196


Virtanen, P., Gommers, R., Oliphant, T. E., Haberland, M., Reddy, T., Cournapeau, D., Burovski, E., Peterson, P., Weckesser, W., Bright, J., Van Der Walt, S. J., Brett, M., Wilson, J., Millman, K. J., Mayorov, N., Nelson, A. R. J., Jones, E., Kern, R., Larson, E., . . . Vázquez-Baeza, Y. (2020). SciPy 1.0: fundamental algorithms for scientific computing in Python. Nature Methods, 17(3), 261–272. https://doi.org/10.1038/s41592-019-0686-2

López-Ferrando, V., Gazzo, A., De La Cruz, X., Orozco, M., & Gelpí, J. L. (2017). PMut: a web-based tool for the annotation of pathological variants on proteins, 2017 update. Nucleic Acids Research, 45(W1), W222–W228. https://doi.org/10.1093/nar/gkx313


