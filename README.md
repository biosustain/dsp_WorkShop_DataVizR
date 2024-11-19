# Data Visualization with R Workshop: Data Science Platform

Welcome to the **Data Visualization with R Workshop**! Below are two setup options:  

- Run the workshop **in the cloud** (no need to install anything).
- Run the workshop **locally** on your machine.  
---

## **Option 1: Run in the Cloud**

1. Register at this link to access the cloud environment:  
 **I'll share the link tomorrow, look at your email.**
   
2. Once logged in, **accept to join the workspace**. After that, you'll see the workspace called `Workshop_DataViz_R_DTU_2024`; click to enter and go to the following `Introduction`

3. In the bottom right menu, open the `01_workshop_codes.html` file from the provided workspace in your favorite browser (preferable Google Chrome).

4. Read in the HTML file to understand the workshop.

5. Open the `01_workshop_codes.Rmd` file from the provided workspace and wait for instructions.

---
## **Option 2: Run Locally**

1. Clone the repository:
   ```bash
   git clone https://github.com/biosustain/dsp_workshop_datavizR
   ```

2. Navigate to the repository:
   ```bash
   cd dsp_workshop_datavizR
   ```

3. Open the workshop instructions:  
   Open this file in your browser:  
   [01_Code/workshop_R.html](https://github.com/biosustain/dsp_workshop_datavizR/blob/main/01_Code/workshop_R.html)

4. Read in the HTML file to understand the workshop.

5. Open the RStudio and load the `01_workshop_codes.Rmd` file

6. Inside the Rmd file, Run the chunks `r install packages` file to install all required R packages (lines 72 to 89)
   
7. Load the libraries `r libraries` chuncks (line 117 to 139) and wait for instructions.

### **Option 2: You can also copy and paste the code in your Rstudio**
Steps 6 and 7:
```{r install packages, eval=FALSE, echo=TRUE, include=TRUE, message=FALSE, highlight=TRUE, code_folding="show"}
# List of packages to install
packages <- c("ggpubr", "grid", "tidyr", "reshape2", "reshape", "ggrepel", "ggh4x", "pheatmap", "RColorBrewer", "patchwork","DT", "kableExtra", "plotly", "bookdown", "heatmaply", "gganimate", "gifski")

# Install missing packages
new_packages <- packages[!(packages %in% installed.packages()[,"Package"])]
if(length(new_packages)) install.packages(new_packages)

# Load the libraries
lapply(packages, library, character.only = TRUE)

# BiocManager
if (!require("BiocManager", quietly = TRUE))
    install.packages("BiocManager")

BiocManager::install("ComplexHeatmap")

```

```{r libraries, include=TRUE, message=FALSE}
library(ggplot2)
library(ggpubr)
library(grid)
library(tidyr)
library(reshape2)
library(ggrepel)
library(ggh4x)
library(pheatmap)
library(RColorBrewer)
library(patchwork)
library(DT)
library(dplyr)
library(kableExtra)
library(ComplexHeatmap)
library(plotly)
library(bookdown)
library(heatmaply)
library(circlize) 
#Extra
library(gganimate)
library(gifski)
```



