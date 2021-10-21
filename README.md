# Matplotlib analysis
##  Create visual charts with Matplotlib

- The purpose of this study was to compare the performance of Pymaceuticals' drug of interest vs the other treatment regimens.

## Data Visualizations:
(![image](https://user-images.githubusercontent.com/81592631/138198572-1a685cd8-3e27-457f-9479-4d66204610ad.png)


Sample Drug Quartiles


- Tools used:
pandas
matplotlib.pyplot
scipy.stats
numpy
sklearn



#####For Loops: cols = []
count = 1
for column in new_df.columns:
            if column == "Tumor Volume (mm3)":
                        cols.append(f"Tumor Volume (mm3)_{count}")
                         count+=1
                        continue
            cols.append(column)
new_df.columns = cols

#####Groupbys:

mouse_group = cleaned_df.groupby("Mouse ID")
max_timepoint = mouse_group["Timepoint"].max()
max_timepoint_df = max_timepoint.to_frame().reset_index()
new_df = pd.merge(max_timepoint_df,
            cleaned_df, on=["Mouse ID","Timepoint"])
            [["Drug Regimen", "Tumor Volume (mm3)"]]

#####and many others!:

Observations
The Drug Regimen Ramicane produced the smallest average tumor sizes overall (40.22)
The Drug Regimen Ketapril produced the largest average tumor sizes overall (55.24)
The Drug Ketapril also had the highest variance of results (68.55)
Infubinol had one giant outlier in the quartile box plot data
For Capomulin, the longer the mouse was on the drug - the more the tumor was reduced
There is a corelation to the size in volume to the weight of the mouse - the bigger the mouse, the bigger the tumor.
Status


