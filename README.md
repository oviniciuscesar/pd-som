# pd-som
`som` is a Pure Data external implementation of `Kohonen's Self-organized Maps (SOM)` a competitive unsupervised neural network proposed by `Teuvo Kohonen` in the paper [Self-organized formation of topologically correct feature maps](https://link.springer.com/article/10.1007/BF00337288). 
Formally, the SOM algorithm can be described as a process that maps high-dimensional input data to elements arranged in a low-dimensional matrix, thus reducing the dimensionality of complex topological spaces.

The object receives a list of features of up to three dimensions and maps the topology of the input data. Once the network is trained, it receives a list of features and outputs the nearest neuron's weights for each input.
`som` is a partial result of research that aims to creatively appropriate of `machine learning` algorithms and mechanisms in the context of `live-electronic` music. Thus, it presents some features that are not present in the original algorithm (or are not commonly implemented in `Self-organized maps`), such as `negative learning rate` (that allows `som` to "unlearn" the data topology ) and ``probability factor`` (that controls the probability of the choice for the nearest neuron weight). 

Binaries for macOS, Windows, and Linux are provided [here](https://github.com/oviniciuscesar/pd-som/releases/tag/v0.2b) 

If they are not working in some specific architecture or system, please contact me. 
`som` was tested on macOS (Sonoma 14.5), Windows 10 64 bits, and Ubuntu 22.04.2 LTS 64 bits running Pure Data Vanilla 0.54-1).
Binary files are accompanied by a patch that shows the application of some of these functions in the context of music creation.





# Build
> [!NOTE]
`som` uses `pd.build`. To build the external on Linux, Mac, and Windows (using Mingw64):

1. `git clone https://github.com/oviniciuscesar/pd-perceptron/ --recursive`;
2. `cd pd-perceptron`;
4. `cmake . -B build`;
5. `cmake --build build`;




# License

`som` uses `GSL - GNU Scientific Library` licensed under GNU GPL version 3.0. 
