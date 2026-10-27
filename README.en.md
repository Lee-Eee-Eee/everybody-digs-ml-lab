# Everybody Digs ML · Interactive Lab

[中文](README.md) · [Open the lab](https://lee-eee-eee.github.io/everybody-digs-ml-lab/interactive/) · [Companion course](https://github.com/Lee-Eee-Eee/everybody-digs-ml)

**Change a parameter and follow the calculation.**

This browser lab accompanies [Everybody Digs ML](https://github.com/Lee-Eee-Eee/everybody-digs-ml). Its 18 lessons start with a small network and progress through forward passes, backpropagation and updates, batch training, Softmax, optimization, convolution and residual connections. Visualizations, numbers and training run in the browser.

The lab interface and explanations are primarily in Chinese; this page provides English navigation. The companion course contains notebooks, derivations and exercises.

## Try it

[Open the first experiment](https://lee-eee-eee.github.io/everybody-digs-ml-lab/interactive/#network). Set `x₁` to 0, change `w₁₁` and observe the output. Repeat with `x₁ = 0.6`; explain what changed by following the displayed multiplication and hidden activation.

## Explore

| Topic | Lessons |
| --- | --- |
| A small network | [Inputs and weights](https://lee-eee-eee.github.io/everybody-digs-ml-lab/interactive/#neuron) · [A hidden neuron](https://lee-eee-eee.github.io/everybody-digs-ml-lab/interactive/#chain) · [Forward pass](https://lee-eee-eee.github.io/everybody-digs-ml-lab/interactive/#paths) |
| Backpropagation | [Output gradient](https://lee-eee-eee.github.io/everybody-digs-ml-lab/interactive/#forward) · [Branch accumulation](https://lee-eee-eee.github.io/everybody-digs-ml-lab/interactive/#output) · [Parameter update](https://lee-eee-eee.github.io/everybody-digs-ml-lab/interactive/#hidden) |
| Batches and probabilities | [Shared weights](https://lee-eee-eee.github.io/everybody-digs-ml-lab/interactive/#matrix) · [Softmax](https://lee-eee-eee.github.io/everybody-digs-ml-lab/interactive/#softmax) |
| Training | [Activation and gradients](https://lee-eee-eee.github.io/everybody-digs-ml-lab/interactive/#activations) · [Initialization](https://lee-eee-eee.github.io/everybody-digs-ml-lab/interactive/#initialization) · [Training](https://lee-eee-eee.github.io/everybody-digs-ml-lab/interactive/#training) · [Optimizers](https://lee-eee-eee.github.io/everybody-digs-ml-lab/interactive/#optimizers) · [Capacity](https://lee-eee-eee.github.io/everybody-digs-ml-lab/interactive/#capacity) |
| Architectures and experiments | [Residuals](https://lee-eee-eee.github.io/everybody-digs-ml-lab/interactive/#residual) · [Deep residuals](https://lee-eee-eee.github.io/everybody-digs-ml-lab/interactive/#deep-residual) · [Convolution](https://lee-eee-eee.github.io/everybody-digs-ml-lab/interactive/#convolution) · [BatchNorm and Dropout](https://lee-eee-eee.github.io/everybody-digs-ml-lab/interactive/#regularization) · [Research](https://lee-eee-eee.github.io/everybody-digs-ml-lab/interactive/#synthesis) |

## Offline use

Clone the repository and open `interactive/index.html` in a browser, retaining the folder structure. Alternatively open the [single-file version](interactive/neural-network-lab.html). JavaScript must be enabled; computations run locally, and progress is stored in the current browser.

```bash
git clone https://github.com/Lee-Eee-Eee/everybody-digs-ml-lab.git
cd everybody-digs-ml-lab
```

Links to course notebooks point to the [companion repository](https://github.com/Lee-Eee-Eee/everybody-digs-ml).

## Maintenance

```bash
node tools/check_interactive.cjs
python interactive/build_standalone.py
```

The first command checks numerical calculations and lesson declarations; the second regenerates the standalone HTML. The companion course keeps a copy for local offline learning.

## Acknowledgments

Thank you to [3Blue1Brown](https://www.3blue1brown.com/lessons/backpropagation/), [Chris Olah](https://colah.github.io/posts/2015-08-Backprop/), and the authors of the cited research. The lab includes [MathJax](https://www.mathjax.org/) for mathematical typesetting; its license is retained in [interactive/vendor/MathJax-LICENSE.txt](interactive/vendor/MathJax-LICENSE.txt).
