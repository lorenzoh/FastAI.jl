# FastAI
[![Stable](https://img.shields.io/badge/docs-stable-blue.svg)](https://FluxML.github.io/FastAI.jl/stable)
[![Dev](https://img.shields.io/badge/docs-dev-blue.svg)](https://FluxML.github.io/FastAI.jl/dev)
[![Build Status](https://github.com/FluxML/FastAI.jl/workflows/CI/badge.svg)](https://github.com/FluxML/FastAI.jl/actions)

FastAI.jl is inspired by [fastai](https://github.com/fastai/fastai/blob/master/fastai/), and is a repository of best practices for deep learning in Julia. Its goal is to easily enable creating state-of-the-art models. FastAI enables the design, training, and delivery of deep learning models that compete with the best in class, using few lines of code.

As an example, training an image classification model from scratch is as simple as

```julia
data = Datasets.loadtaskdata(Datasets.datasetpath("imagenette2-160"), ImageClassificationTask)
method = ImageClassification(Datasets.loadclassesclassification("imagenette2-160"), (160, 160))
learner = methodlearner(method, data, Models.xresnet18(), ToGPU(), Metrics(accuracy))
fitonecycle!(learner, 5)
```

Please read [the documentation](https://fluxml.github.io/FastAI.jl/dev) for more information and see the [setup instructions](docs/setup.md)
