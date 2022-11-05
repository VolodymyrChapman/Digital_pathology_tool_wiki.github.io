# Digital_pathology_tool_wiki
A collection of links to useful digital pathology tools to summarise, simplify and better communicate the plethora of tools available.

![image](https://user-images.githubusercontent.com/44582194/144881375-98a61b2b-5d1a-4063-acd0-fe2fc30e0671.png)

## All contributions, forks, pull requests, suggestions etc. welcome! Don't be a stranger :-) 


| Task To Achieve                | Tool Name                | Tool Description                                                                                                      | Publication Link (if Any)                                                                                                                                                 | Tool Link                                                                                                          | Notes                                                                                                                                                                                                                                                                                                                                                                                                |
|--------------------------------|--------------------------|-----------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Registration Of Related Images | HistoReg                 | An ITK Tool For Rapid Registration Achieving High Registration Accuracy In ANHIR Challenge.                           | Https://arxiv.org/abs/1904.11929 ; Https://ieeexplore.ieee.org/document/9058666                                                                                           | Https://github.com/CBICA/HistoReg                                                                                  | I Encountered Some Difficulties Building ITK As Described In Installation Instructions. Issues Were Resolved On Ubuntu 20.04 With Local Installation Of ITK 4.13.2 Using  Apt Package.                                                                                                                                                                                                               |
|                                | ANHIR_MW                 | A Python Tool That Trials Multiple Registration Methods To Achieve High Registration Accuracy In ANHIR Challenge.     | Https://ieeexplore.ieee.org/document/9058666                                                                                                                              | Https://github.com/MWod/ANHIR_MW                                                                                   | Due To Brute Force Approach, Tool Is Slower Than HistoReg. Installation And Use Is Simple.                                                                                                                                                                                                                                                                                                           |
| Nuclear Segmentation           | HoverNet                 | Simultaneous Segmentation And Classification Using A Multibranch CNN.                                                 | Https://www.sciencedirect.com/science/article/pii/S1361841519301045?via%3Dihub                                                                                            | Https://github.com/vqdang/hover_net                                                                                | Empirically, Appears To Be A Good Middle Ground Between StarDist And CellPose In That Segmentations Are Not Confined To Star-Convex Polygons (StarDist) But Do Not Overshoot The Nucleus (CellPose).                                                                                                                                                                                                 |
|                                | StarDist                 | Unet For Segmentation Of Rounded Objects, I.e. Nuclei.                                                                | Https://link.springer.com/chapter/10.1007%2F978-3-030-00934-2_30                                                                                                          | Https://github.com/stardist/stardist                                                                               | All Detected Objects Will Take Rounded, Star-Convex Polygon Structure. Tool Is Therefore Valid On Rounded Nuclei But Not So Much On Other Objects That May Take Elongated Or ‘sharp’ Shapes.                                                                                                                                                                                                         |
|                                | CellPose                 | Unet For Segmentation Of Objects – No Assumptions Of Object Shape.                                                    | Https://www.nature.com/articles/s41592-020-01018-X                                                                                                                        | Https://github.com/MouseLand/cellpose                                                                              | Experience Has Shown That Predicted Boundaries Extend Past The Nucleus Reflecting The Tool Objective Of Predicting Cell Structure. Beware Use In Situations With Little Tolerance For Extension Past The Nuclear Membrane.                                                                                                                                                                           |
| Preprocessing                  | Staintools               | Tools For Processing Stains Of Digital Pathology Images (i.e. Stain Normalisation, Noise Reduction, Stain Separation) | Documentation: Https://staintools.readthedocs.io/en/latest/normalization.html#module-Staintools.normalization.macenko                                                     | Https://github.com/Peter554/StainTools                                                                             | The Pip Package Recommended Is A Bit Aged And Does Not Follow The Structure Of The GitHub Repo. Advised To Test Both Pip And GitHub Versions To Determine Preference.                                                                                                                                                                                                                                |
|                                | DigiPathAI               | WSI Segmentation To Separate Tissue From Background In H&E Images                                                     | Https://www.nature.com/articles/s41598-021-90444-8                                                                                                                        | Https://github.com/haranrk/DigiPathAI                                                                              | Requirements Include TensorFlow Version 1, Which Is Not Compatible With Newest Python Versions. This Can Be Fixed With Adjustments To GitHub Code.                                                                                                                                                                                                                                                   |
|                                | HistoQC                  | WSI Processing Tools (segmentation Of Background, Artifact Detection)                                                 | Https://pubmed.ncbi.nlm.nih.gov/30990737/                                                                                                                                 | Https://github.com/choosehappy/HistoQC                                                                             | Experience Shows This Is Easy To Implement, Runs Fairly Quickly, And Is Successful In Removing Artefacts From Regions Of Interest. Has Support For IHC Stains As Well As The Default H&E.                                                                                                                                                                                                            |
| Stain Separation               | Staintools               | Vahadane And Macenko Stain Separation Methods                                                                         | Macenko Et Al., 2009: Http://wwwx.cs.unc.edu/~mn/sites/default/files/macenko2009.pdf Vahadane Et Al., 2016: Https://pubmed.ncbi.nlm.nih.gov/27164577/                     | Https://github.com/Peter554/StainTools/tree/master/staintools/stain_extraction                                     | Separation Into Two Stains I.e. H&E Into H And E Or H-DAB Into H And DAB.                                                                                                                                                                                                                                                                                                                            |
|                                | Geijs Et Al., 2018       |                                                                                                                       | Https://www.spiedigitallibrary.org/conference-Proceedings-Of-Spie/10581/2293734/Automatic-Color-Unmixing-Of-IHC-Stained-Whole-Slide-Images/10.1117/12.2293734.short?SSO=1 | Https://github.com/VolodymyrChapman/AutomaticColorUnmixing_VC_branch                                               | Separation Into Three Stains I.e. H, E (residual) And DAB; GitHub Repo Is A Public Fork Of An Internal One Developed By Geijs Et Al. Repo Editing To Increase Dependency On Openly Accessible, Stable Libraries (scikit-Image Etc.) Ongoing – Contributions Welcome                                                                                                                                  |
|                                | Ruifrok & Johnston, 2001 |                                                                                                                       | Https://europepmc.org/article/MED/11531144                                                                                                                                | Https://scikit-Image.org/docs/stable/api/skimage.color.html#skimage.color.rgb2hed                                  | Separation Into Three Stains I.e. H, E (residual) And DAB.                                                                                                                                                                                                                                                                                                                                           |
| Parsing Images / WSIs          | Openslide-Python         | Python Library Of Openslide Tool – Allows Parsing Of WSIs Into Python (.svs Etc. )                                    | Python API Guide: Https://openslide.org/api/python/                                                                                                                       | Openslide: Https://openslide.org/download/   Openslide-Python:   Https://anaconda.org/conda-Forge/openslide-Python | Requires Installation Of Openslide To Work. Especially Useful Functions Are .read_region() To Extract Specific Regions Of WSIs And .get_thumbnail() With A Desired Output Size To Downsample WSIs By Any Value. Beware The Dreaded Pixman ‘missing Sections’ Issue – Ensure That Pixman 0.38 Is Not In Use (https://github.com/openslide/openslide/issues/291) And Update To 0.40+ Or 0.36 If It Is. |
|                                | Skimage.io               | Easiest Way To Parse An Image (.png, .jpeg, .tiff Etc.) Into Python As A Numpy Array                                  | Https://scikit-Image.org/docs/stable/api/skimage.io.html#skimage.io.imread                                                                                                | Https://anaconda.org/anaconda/scikit-Image                                                                         |
