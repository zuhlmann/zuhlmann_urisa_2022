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
**CONTENTS** (_note that we will add_ ```four_corners_morels``` _directory (Pro project) in next step and_ ```.git``` _will not be present in your download_ dir</br>
![git_dir](https://user-images.githubusercontent.com/48263393/196567709-a71b9178-c975-4a77-8a52-8b54447a43e2.jpg)

#### 2. <ins>Create new ArcGIS Pro Project</ins></br>
- Create new ArcGIS Pro project within the directory from step 1.</br> 
![new_project](https://user-images.githubusercontent.com/48263393/196758715-11043927-70cd-4f04-8017-6ac8a0e1dbb6.jpg)</br>
- **IMPORTANT** Title the new project exactly(!): ```four_corners_morels```</br>
- _Notice the directory in above screenshot_</br>

#### 3. <ins>Add Folder Connection and open both Notebooks</ins></br>
- In ArcGIS Pro with project open, Add Folder Connection to ```notebooks_tutorial``` directory</br>
- Open **urisa_p1** and **basics** Notebooks from within ```notebooks_tutorial``` directory</br>

## Begin Tutorial</br>
<ins>Tips to self-guided tutorial via Notebooks</ins></br>
- All cells except those that are entirely commented out (i.e. no black non-commented code) will be run in order.  Note that you can run the cells that are pure comments to no consequence - nothing will happen... :)
- Comments
  - code in Python is Commented-out using # sign 
  - lines will be rendered in green
  - **READ** - these are line by line instructions and notes to compliment below cell by cell instructions</br>
  ![comments](https://user-images.githubusercontent.com/48263393/196494882-f7684b05-87cd-4743-87fe-c405e394f64d.jpg)</br>
  
### Steps Summarized (*Note that Notebook will have more verbose instructions*)
**Open _urisa_p1_ Notebook and begin...** 
- Cell 1: Load Modules. Imports libraries 
- Cell 2: Canvas.  Follow instructions to populate map with shapfiles and zoom in
- Cell 3: Paths. Replace string within single quotes with ```path/to/your/notebooks_tutorial``` directory
- Cell 4: Load Pandas DataFrame: Read csv into DataFrame and inspect
- Cell 5: Incorrect File Path. Notice this is MY file path, not yours
- Cell 6: Fix File Path the Hard Way. Follow comments, run cell or change path manually and rerun Cell 4
- Cell 7: Dictionary.  Not necessary, but makes later code more readable.  I like dictionaries
- Cell 8: Arguments for Copy FC.  Create and pull from DataFrame (df) all arguments to copy Four Corners Fire Perim
- Cell 9: Create Datasets.  Go to ```basics``` Notebook (open it) and run all three cells in order
- Cell 10: Create new FC.  Copy selected fire perimeter into new feature class in agency dataset within project gdb.
**DON'T FORGET** to select four corners fire from attribute table prior to running
- Cell 11: Clean up map.  A reminder to remove redundant FC
- Cell 12: Set values to DataFrame. Record data location of ```four_corners_fire_perim```
- Cell 13: Arguments for Copy Roads FC.  Same thing as fire boundaries, but passing full path of roads dataset location from DataFrame directly to function (Cell 14) as opposed to from Table of Contents (TOC)
- Cell 14: Copy roads FC to Pro gdb.  Run function, copy into database - should appear in map depending on user's Pro settings
- Cell 15: Set values to DataFrame.  New data location and original.
- Cell 16: Clip contour polygons to fire boundary. NOTE that we combined the assimilating of arguments AND running of function (Clip_analysis) into a single cell in this instance as opposed to assigning variables (arguments) in one cell and calling function in next cell. Output clipped contour polygons for use in final map
- Cell 17: Set values to DataFrame. LOOK(!)  Added a couple more metadata attributes that can be saved to csv and later used to populate Item Description (a different tutorial!)
- Cell 18: Clean up map.  
- Cell 19: Inpsect DataFrame prior to saving.  Also notice the Abstract we added - just for fun!
- Cell 20: Save updated csv.  Retained original for repeated runs of tutorial, as updated csv now has updated file paths.  You can find the updated csv in ```notebooks_tutorial``` directory.

## Conclusions
- Notebooks are a nice way to organize programmic workflows
- Pandas offer nice alternatives to databases if project is being utilized by non-technical users.  Metadata-ish components are contained in the csv
- Same with all coding, Notebooks are simply text documents (.ipynb) that can be reused.  
- Code can be incorporated into more complicated object-oriented modules as functions and shared amongst colleagues.
- For projects with logs of intermediary data or just lots of data copying, creating, etc., information about data provenance or geoprocessing steps can be added to dataframe concurrently for future reference.
- Covered in the actual presentation at URISA - Pandas is both a core geospatial data analytics library but also originated and developed  across disciplines and industries.  It's an essentialy Python library to learn.
- <ins>Not Covered Today:</ins> 
  - I use the data inventory csv (```four_corners_morels.csv```) to populate Item Descriptions via the shapefile's ```xml```.  I imagine it can be parsed into a ```xslt``` as well.
  - Ditto for cleaning databases periodically and once projects are complete.  I **delete, move, rename, copy** feature classes via the inventory.csv to cleanup the geodatabase.

  


