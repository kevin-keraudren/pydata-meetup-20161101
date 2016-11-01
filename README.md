Slides for 28th London PyData Meetup (01/11/2016)
=================================================

<p><a href="https://github.com/kevin-keraudren">Kevin Keraudren</a> on&nbsp;<b>Medical Imaging in Python: from morphological operations to machine learning</b></p> 
<p><i>In this talk, I will present how to leverage the Python ecosystem to build complex analysis pipelines for medical image analysis. Examples will be drawn from my time at Imperial College, working on <a href="http://www.slideshare.net/kevinkeraudren/segmenting-epithelial-cells-in-highthroughput-rnai-screens-miaab-2011">microscopy images</a>&nbsp;and <a href="https://www.youtube.com/watch?v=t1pIh_TOVLM">fetal MRI</a>, as well as the work we are currently doing at <a href="https://klarismo.com/">Klarismo</a> on quantitative analysis of whole body MRI. This talk will involve scikit-image for image processing, scikit-learn for machine learning, SimpleITK for algorithms specific to medical images, and VTK for 3D visualisation. And because medical images tend to have lots of voxels, it will surely require some Cython code to speed things up.</i>  <br /></p> 

https://www.meetup.com/PyData-London-Meetup/events/234828438/

You can view this notebook online with nbviewer, <a href="http://nbviewer.jupyter.org/github/kevin-keraudren/pydata-meetup-20161101/blob/0f0b1fab4ef3b7f861bb2dba6d5268538fe00b23/PyData.ipynb">here as a notebook</a> 
or <a href="http://nbviewer.jupyter.org/format/slides/github/kevin-keraudren/pydata-meetup-20161101/blob/0f0b1fab4ef3b7f861bb2dba6d5268538fe00b23/PyData.ipynb">here as slides</a>.

Otherwise there is a static version on <a href="http://www.slideshare.net/kevinkeraudren/medical-imaging-in-python-from-morphological-operations-to-machine-learning-and-visualisation">SlideShare</a>.


Installation
------------

    brew install node npm
    
    pip install matplotlib jupyter --upgrade --force
    
    git clone https://github.com/kevin-keraudren/RISE.git -b klarismo-chrome-changes
    cd RISE
    pip install -e .
    npm install
    npm run build
    npm run watch-less
    jupyter-nbextension install rise --py --sys-prefix --symlink
    jupyter-nbextension enable rise --py --sys-prefix
    
    jupyter nbextension enable --py --sys-prefix widgetsnbextension

Customising the CSS for RISE (`~/.jupyter/custom/custom.css`):

    div#notebook-container {height:100% !important;}
    
    .widget-hslider {
        width:75% !important;
    }
    .my-outer-container {
        width:100%;
        height:100%;
        position:absolute;
        display:table;
    }
    .my-center-container {
        display:table-cell;
        vertical-align:middle;
        width:100%;
        height:100%:
    }

Notes
-----

I considered using this `hide-code` notebook extension:

    pip install git+https://github.com/kirbs-/hide_code

But in the end it's simpler to just skip cells, and if necessary save matplotlib's output as PNG.