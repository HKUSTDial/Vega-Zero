# Vega-Zero

Vega-Zero is a visualization grammar by simplifying Vega-Lite, with the main purpose to ﬂatten a hierarchical Vega-Lite speciﬁcation to a sequence-based speciﬁcation. 

Thus, it is much easier to use Vega-Zero to train a sequence-to-sequence model for generating a sequence output. 
Vega-Zero can be used to support some learning tasks, e.g., translating a natural language query to visualization.

## Definition 

Vega-Zero keeps most of the keywords of the Vega-Lite about the mapping between visual encoding channels and (transformed) data variables. It ﬂattens a JSON object into a sequence of keywords by removing structure-aware symbols such as brackets, colons, and quotation marks. Formally, a unit speciﬁcation in Vega-Zero is a four tuple (similar to Vega-Lite but with each tuple being a sequence) as:

**unit** = (**mark**, **data**, **encoding**, **transform**)

Naturally, as a simpliﬁcation of Vega-Lite: 
1. **mark** denotes the chart type, including *bar*, *line*, *point* (for scatter chart), *arc* (for pie chart); 
2. **data** speciﬁes the source data; 
3. **encoding** contains *x*/*y*-axis, *aggregate* function, and *color* based on which column; 
4. **transform** deﬁnes some data transformation functions: *ﬁlter*, *bin*, *group*, *sort*, and *top-k*.

<img src="./vega-zero.png" width="600">

## Example

Below is an example to show the connection between Vega-Zero and Vega-Lite.


<img src="./example.png" width="600">

## Convert Vega-Zero to Vega-Lite specification

In this repository, we provide a Python script to convert a Vega-Zero specification to a Vega-Lite specification.
 
Below is an example to run this Python script in the Jupyter Notebook.

<img src="./example-jupyter.png" width="600">

## How to use?

Please follow the examples in the ```examples.ipynb```, if you want to render the visualization result in Jupyter Notebook (or Lab), please follow the instruction of [IPython Vega](https://github.com/vega/ipyvega).

## Citing Vega-Zero

```bibTeX
@inproceedings{ncnet,
author    = {Yuyu Luo and Nan Tang and Guoliang Li and Jiewei Tang and Chengliang Chai and Xuedi Qin},
title     = {Natural Language to Visualization by Neural Machine Translation},
booktitle = {{IEEE IEEE Visualization Conference (VIS)}},
year      = {2021},
}
```

## License
The software is available under the [MIT License](https://github.com/Thanksyy/Vega-Zero/blob/main/README.md).

## Contact
If you have any questions, feel free contact Yuyu Luo (luoyy18 at mails.tsinghua.edu.cn).