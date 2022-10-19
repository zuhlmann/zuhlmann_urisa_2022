# Programmatic Geoprocessing Workflows using Pandas Dataframes in ArcGIS Pro Notebooks *Zachary Uhlmann* </br>
Zachary Uhlmann</br>
**ABSTRACT:** Using examples from my job at a mid-sized heavy civil engineering firm and drawing on previous experience in the natural resource field, we will use Python within a Jupyter Notebook in Pro to create, analyze, document, and ultimately publish data to ArcGIS Online. We will set parameters and document metadata from CSVs using Pandas, one of the essential python data analytics libraries.  This workflow will raise the ceiling of geoprocessing efficiency and customization in our GIS workflows while keeping database information accessible to non-GIS people and those with no programming experience.  Hopefully these examples can motivate people to overcome their apprehension, and finally begin the switch from Desktop to Pro. 

## Tutorial Prep</br>

#### 1. <ins>Download reposistory:</ins></br>
- download as zip file</br></br>
![download_git](https://user-images.githubusercontent.com/48263393/196487941-c7fa7bbe-3d3d-4837-82b9-f8c9eebaf599.jpg)
- unzip folder, and change unzipped folder name to: ```notebooks_tutorial```</br>
- NOTE - we will create Pro map here, so ensure directory path isn't too long or special character crazy</br>
  - My full path is this: ```C:\Users\uhlmann\Documents\urisa_conference_2022\notebooks_tutorial```</br>
  - your full path should be: ```path\to\your\notebooks_tutorial```</br></br>
**CONTENTS**</br>
![git_dir](https://user-images.githubusercontent.com/48263393/196567709-a71b9178-c975-4a77-8a52-8b54447a43e2.jpg)

#### 2. <ins>Create new ArcGIS Pro Project</ins></br>
- Create new ArcGIS Pro project within the directory from step 1.</br> 
- **IMPORTANT** Title the new project exactly(!): ```four_corners_morels```</br>

#### 3. <ins>Insert Notebooks from repository directly into Pro Project</ins></br>
- Add **urisa_p1** and **basics** Notebooks to ArcPro Project</br>
_file extensions .IPYNB_ from download</br></br>
![add_notebook](https://user-images.githubusercontent.com/48263393/196487932-8ab562f9-9e34-494b-a852-6ee418aead30.jpg)</br>

## Begin Tutorial</br>
**Open _urisa_p1_ Notebook and begin...** </br>
<ins>Tips to self-guided tutorial via Notebooks</ins></br>
- Comments
  - code in Python is Commented-out using # sign 
  - lines will be rendered in green
  - **READ** - these are line by line instructions and notes
  ![comments](https://user-images.githubusercontent.com/48263393/196494882-f7684b05-87cd-4743-87fe-c405e394f64d.jpg)</br>
  
### Steps Summarized (*Note that Notebook will have more verbose instructions*)</br>
- Cell 1: Load Modules. Imports libraries 
- Cell 2: Canvas.  Follow instructions to populate map with shapfiles and zoom in
- Cell 3: Paths. Set a path or two to a variable for later use
- Cell 4: Load Pandas DataFrame: Read csv into DataFrame and inspect
- Cell 5: Incorrect File Path. Notice this is MY file path, not yours
- Cell 6: Fix File Path the Hard Way. Follow comments, run cell or change path manually and rerun Cell 4
-
 

  


