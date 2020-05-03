# ![](https://ga-dash.s3.amazonaws.com/production/assets/logo-9f88ae6c9c3871690e33280fcf557f33.png) Project 2: Kaggle Challenge - Ames Iowa Housing Data Set

##### by: Lin Junyuan, SG-DSI-14

## Introduction
SAT introduced a new format in 2016. Being an employee of the College Board, my role is to track statewide participation rates and score results. Using the data collected, the objective is to recommend where to invest money to improve SAT participation rates.

## Problem Statement

What is the best regression model, with an **upper limit of 30 variables**, that can predict house sale price in Ames Iowa to a **RMSE of less than $40,000** and what are its **top 3 influencing factors**.

## Executive Summary

The objective of this project is to create the best regression model to predict housing sale price in Ames, with the goals as stated in the problem statement. The data provided are one set of training data, one set of test data and one set of submission example.

Within the training data and test data are 80 variables of different types and datatypes. The training data has one extra column of `Saleprice` for training purposes. Both data require data cleaning and imputation for missing data.

After a careful process of selection and modelling, the **lasso** model is found to be the most suitable model which fits our objectives. The top 3 influencing factors are **Overall material and finish quality** (overall_qual), **Above grade (ground) living area in square feet** (gr_liv_area) and **Size of garage in square feet** (garage_area).

 ## Conclusions and Recommendations

Through this exercise, it can be observed that though there are many variables available, a number of them are found to be collinear and quite a significant amount could not meet our selection criteria. On the other hand, this helps us to be able to narrow down in order to meet our objective.

In conclusion, the lasso model was able to fulfil the criteria set out in the problem statement. Its number of predictors are 26, which is less than 30. The Kaggle submission results indicate that the RMSE target is met.

The top three predictors are:

1. Overall material and finish quality (overall_qual)
2. Above grade (ground) living area in square feet (gr_liv_area)
3. Size of garage in square feet (garage_area) are the top three influencing factors

Therefore, homeowners seeking to increase their house value can improve its overall quality, expand the above ground living area or the size of the garage.

On the other hand, the predictors with the top three negative variables can also provide interesting insight. First of all, they are all drawn from nominal variables, 1. land_contour: Banked, which means that there is a `Quick and significant rise from street grade to building`, 2. garage_type:2Types, which means there is `More than one type of garage` and 3. ms_zoning_:RM, which means its zoning classification is `Residential Medium Density`. Homebuyers seeking lower priced units or people seeking to resell their house should take these factors into consideration.



## Data dictionary

|     Column      |  Type  | Description                                                  |
| :-------------: | :----: | :----------------------------------------------------------- |
|       id        |  int   | **ID**                                                       |
|       pid       | object | **Property ID Number**                                       |
|   ms_subclass   | object | **The building class** <br> 20 : 1-STORY 1946 & NEWER ALL STYLES <br>30 : 1-STORY 1945 & OLDER<br>40 : 1-STORY W/FINISHED ATTIC ALL AGES<br>45 : 1-1/2 STORY - UNFINISHED ALL AGES<br>50 : 1-1/2 STORY FINISHED ALL AGES<br>60 : 2-STORY 1946 & NEWER<br>70 : 2-STORY 1945 & OLDER<br>75 : 2-1/2 STORY ALL AGES<br>80 : SPLIT OR MULTI-LEVEL<br>85 : SPLIT FOYER<br>90 : DUPLEX - ALL STYLES AND AGES<br>120 : 1-STORY PUD (Planned Unit Development) - 1946 & NEWER<br>150 : 1-1/2 STORY PUD - ALL AGES<br>160 : 2-STORY PUD - 1946 & NEWER<br>180 : PUD - MULTILEVEL - INCL SPLIT LEV/FOYER<br>190 : 2 FAMILY CONVERSION - ALL STYLES AND AGES |
|    ms_zoning    | object | **Identifies the general zoning classification of the sale.**<br>A : Agriculture<br>C : Commercial<br>FV : Floating Village Residential<br>I : Industrial<br>RH : Residential High Density<br>RL : Residential Low Density<br>RP : Residential Low Density Park<br>RM : Residential Medium Density |
|  lot_frontage   | float  | **Linear feet of street connected to property**              |
|    lot_area     |  int   | **Lot size in square feet**                                  |
|     street      | object | **Type of road access to property**<br>Grvl : Gravel<br>Pave : Paved |
|      alley      | object | **Type of alley access to property**<br>Grvl : Gravel<br>Pave : Paved<br>NA : No alley access |
|    lot_shape    |  int   | **LotShape: General shape of property**<br>3 (Reg) : Regular<br>2 (IR1) : Slightly irregular<br>1 (IR2) : Moderately Irregular<br>0 (IR3) : Irregular |
|  land_contour   | object | **LandContour: Flatness of the property**<br>Lvl : Near Flat/Level<br>Bnk : Banked - Quick and significant rise from street grade to building<br>HLS : Hillside - Significant slope from side to side<br>Low Depression |
|    utilities    |  int   | **Type of utilities available**<br>3 (AllPub) : All public Utilities (E,G,W,& S)<br>2 ( NoSewr) : Electricity, Gas, and Water (Septic Tank)<br>1 (NoSeWa) : Electricity and Gas Only<br>0 (ELO) : Electricity only |
|   lot_config    | object | **Lot configuration**<br>Inside : Inside lot<br>Corner : Corner lot<br>CulDSac : Cul-de-sac<br>FR2 : Frontage on 2 sides of property<br>FR3 : Frontage on 3 sides of property |
|   land_slope    |  int   | **Slope of property**<br>2 (Gtl) : Gentle slope<br>1 (Mod) : Moderate Slope<br>0 (Sev) : Severe Slope |
|  neighborhood   | object | **Physical locations within Ames city limits**<br>Blmngtn : Bloomington Heights<br>Blueste : Bluestem<br>BrDale : Briardale<br>BrkSide : Brookside<br>ClearCr : Clear Creek<br>CollgCr : College Creek<br>Crawfor : Crawford<br>Edwards : Edwards<br>Gilbert : Gilbert<br>IDOTRR : Iowa DOT and Rail Road<br>Meadow : Meadow Village<br>Mitchel : Mitchell<br>Names : North Ames<br>NoRidge : Northridge<br>NPkVill : Northpark Villa<br>NridgHt : Northridge Heights<br>NWAmes : Northwest Ames<br>OldTown : Old Town<br>SWISU : South & West of Iowa State University<br>Sawyer : Sawyer<br>SawyerW : Sawyer West<br>Somerst : Somerset<br>StoneBr : Stone Brook<br>Timber : Timberland<br>Veenker : Veenker |
|   condition_1   | object | **Proximity to main road or railroad**<br>Artery : Adjacent to arterial street<br>Feedr : Adjacent to feeder street<br>Norm : Normal<br>RRNn : Within 200' of North-South Railroad<br>RRAn : Adjacent to North-South Railroad<br>PosN : Near positive off-site feature--park, greenbelt, etc.<br>PosA : Adjacent to postive off-site feature<br>RRNe : Within 200' of East-West Railroad<br>RRAe : Adjacent to East-West Railroad |
|   condition_2   | object | **Proximity to main road or railroad (if a second is present)**<br>Artery : Adjacent to arterial street<br>Feedr : Adjacent to feeder street<br>Norm : Normal<br>RRNn : Within 200' of North-South Railroad<br>RRAn : Adjacent to North-South Railroad<br>PosN : Near positive off-site feature--park, greenbelt, etc.<br>PosA : Adjacent to postive off-site feature<br>RRNe : Within 200' of East-West Railroad<br>RRAe : Adjacent to East-West Railroad |
|    bldg_type    | object | **Type of dwelling**<br>1Fam : Single-family Detached<br>2FmCon : Two-family Conversion; originally built as one-family dwelling<br>Duplx : Duplex<br>TwnhsE : Townhouse End Unit<br>TwnhsI : Townhouse Inside Unit |
|   house_style   | object | **Style of dwelling**<br>1Story : One story<br>1.5Fin : One and one-half story: 2nd level finished<br>1.5Unf : One and one-half story: 2nd level unfinished<br>2Story : Two story<br>2.5Fin : Two and one-half story: 2nd level finished<br>2.5Unf : Two and one-half story: 2nd level unfinished<br>SFoyer : Split Foyer<br>SLvl : Split Level |
|  overall_qual   |  int   | **Overall material and finish quality**<br>10 : Very Excellent<br>9 : Excellent<br>8 : Very Good<br>7 : Good<br>6 : Above Average<br>5 : Average<br>4 : Below Average<br>3 : Fair<br>2 : Poor<br>1 : Very Poor |
|  overall_cond   |  int   | **Overall condition rating**<br>10 : Very Excellent<br>9 : Excellent<br>8 : Very Good<br>7 : Good<br>6 : Above Average<br>5 : Average<br>4 : Below Average<br>3 : Fair<br>2 : Poor<br>1 : Very Poor |
|   year_built    |  int   | **Original construction date**                               |
| year_remod/add  |  int   | **Remodel date (same as construction date if no remodeling or additions)** |
|   roof_style    | object | **Type of roof**<br>Flat : Flat<br>Gable : Gable<br>Gambrel : Gabrel (Barn)<br>Hip : Hip<br>Mansard : Mansard<br>Shed : Shed |
|    roof_matl    | object | **Roof material**<br>ClyTile : Clay or Tile<br>CompShg : Standard (Composite) Shingle<br>Membran : Membrane<br>Metal : Metal<br>Roll : Roll<br>Tar&Grv : Gravel & Tar<br>WdShake : Wood Shakes<br>WdShngl : Wood Shingles |
|  exterior_1st   | object | **Exterior covering on house**<br>AsbShng : Asbestos Shingles<br>AsphShn : Asphalt Shingles<br>BrkComm : Brick Common<br>BrkFace : Brick Face<br>CBlock : Cinder Block<br>CemntBd : Cement Board<br>HdBoard : Hard Board<br>ImStucc : Imitation Stucco<br>MetalSd : Metal Siding<br>Other : Other<br>Plywood : Plywood<br>PreCast : PreCast<br>Stone : Stone<br>Stucco : Stucco<br>VinylSd : Vinyl Siding<br>Wd Sdng : Wood Siding<br>WdShing : Wood Shingles |
|  exterior_2nd   | object | **Exterior covering on house (if more than one material)**<br>AsbShng : Asbestos Shingles<br>AsphShn : Asphalt Shingles<br>BrkComm : Brick Common<br>BrkFace : Brick Face<br>CBlock : Cinder Block<br>CemntBd : Cement Board<br>HdBoard : Hard Board<br>ImStucc : Imitation Stucco<br>MetalSd : Metal Siding<br>Other : Other<br>Plywood : Plywood<br>PreCast : PreCast<br>Stone : Stone<br>Stucco : Stucco<br>VinylSd : Vinyl Siding<br>Wd Sdng : Wood Siding<br>WdShing : Wood Shingles |
|  mas_vnr_type   | object | **Masonry veneer type**<br>BrkCmn : Brick Common<br>BrkFace : Brick Face<br>Block : Cinder Block<br>None : None<br>Stone : Stone |
|  mas_vnr_area   | float  | **Masonry veneer area in square feet**                       |
|   exter_qual    |  int   | **Exterior material quality**<br>4 (Ex) : Excellent<br>3 (Gd) : Good<br>2 (TA) : Average/Typical<br>1 (Fa) : Fair<br>0 (Po) : Poor |
|   exter_cond    |  int   | **Present condition of the material on the exterior**<br>4 (Ex) : Excellent<br>3 (Gd) : Good<br>2 (TA) : Average/Typical<br>1 (Fa) : Fair<br>0 (Po) : Poor |
|   foundation    | object | **Type of foundation**<br>BrkTil : Brick & Tile<br>CBlock : Cinder Block<br>PConc : Poured Contrete<br>Slab : Slab<br>Stone : Stone<br>Wood : Wood |
|    bsmt_qual    | float  | **Height of the basement**<br>5 (Ex) : Excellent (100+ inches)<br>4 (Gd) : Good (90-99 inches)<br>3 (TA) : Typical (80-89 inches)<br>2 (Fa) : Fair (70-79 inches)<br>1 (Po) : Poor (<70 inches)<br>0 (NA) : No Basement |
|    bsmt_cond    | float  | General condition of the basement<br>5 (Ex) : Excellent<br>4 (Gd) : Good<br>3 (TA) : Typical - slight dampness allowed<br>2 (Fa) : Fair - dampness or some cracking or settling<br>1 (Po) : Poor - Severe cracking, settling, or wetness<br>0 (NA) : No Basement |
|  bsmt_exposure  | float  | **Walkout or garden level basement walls**<br>4 (Gd) : Good Exposure<br>3 (Av) : Average Exposure (split levels or foyers typically score average or above)<br>2 (Mn) : Mimimum Exposure<br>1 (No) : No Exposure<br>0 (NA) : No Basement |
| bsmtfin_type_1  | float  | **Quality of basement finished area**<br>6 (GLQ) : Good Living Quarters<br>5 (ALQ) : Average Living Quarters<br>4 (BLQ) : Below Average Living Quarters<br>3 (Rec) : Average Rec Room<br>2 (LwQ) : Low Quality<br>1 (Unf) : Unfinshed<br>0 (NA) : No Basement |
|  bsmtfin_sf_1   | float  | **Type 1 finished square feet**                              |
| bsmtfin_type_2  | float  | **Quality of second finished area (if present)**<br>6 (GLQ) : Good Living Quarters<br>5 (ALQ) : Average Living Quarters<br>4 (BLQ) : Below Average Living Quarters<br>3 (Rec) : Average Rec Room<br>2 (LwQ) : Low Quality<br>1 (Unf) : Unfinshed<br>0 (NA) : No Basement |
|  bsmtfin_sf_2   | float  | **Type 2 finished square feet**                              |
|   bsmt_unf_sf   | float  | **Unfinished square feet of basement area**                  |
|  total_bsmt_sf  | float  | **Total square feet of basement area**                       |
|     heating     | object | **Type of heating**<br>Floor : Floor Furnace<br>GasA : Gas forced warm air furnace<br>GasW : Gas hot water or steam heat<br>Grav : Gravity furnace<br>OthW : Hot water or steam heat other than gas<br>Wall : Wall furnace |
|   heating_qc    |  int   | **Heating quality and condition**<br>4 (Ex) : Excellent<br>3 (Gd) : Good<br>2 (TA) : Average/Typical<br>1 (Fa) : Fair<br>0 (Po) : Poor |
|   central_air   |  int   | **Central air conditioning**<br>0 (N) : No<br>1 (Y) : Yes    |
|   electrical    |  int   | **Electrical system**<br>4  (SBrkr) : Standard Circuit Breakers & Romex<br>3 (FuseA) : Fuse Box over 60 AMP and all Romex wiring (Average)<br>2 (FuseF) : 60 AMP Fuse Box and mostly Romex wiring (Fair)<br>1 (FuseP) : 60 AMP Fuse Box and mostly knob & tube wiring (poor)<br>0 (Mix) : Mixed |
|   1st_flr_sf    |  int   | **First Floor square feet**                                  |
|   2nd_flr_sf    |  int   | **Second floor square feet**                                 |
| low_qual_fin_sf |  int   | **Low quality finished square feet (all floors)**            |
|   gr_liv_area   |  int   | **Above grade (ground) living area square feet**             |
| bsmt_full_bath  | float  | **Basement full bathrooms**                                  |
| bsmt_half_bath  | float  | **Basement half bathrooms**                                  |
|    full_bath    |  int   | **Full bathrooms above grade**                               |
|    half_bath    |  int   | **Half baths above grade**                                   |
|  bedroom_abvgr  |  int   | **Number of bedrooms above basement level**                  |
|  kitchen_abvgr  |  int   | **Number of kitchens**                                       |
|  kitchen_qual   |  int   | **Kitchen quality**<br>4 (Ex) : Excellent<br>3 (Gd) : Good<br>2 (TA) : Typical/Average<br>1 (Fa) : Fair<br>0 (Po) : Poor |
|  totrms_abvgrd  |  int   | **Total rooms above grade (does not include bathrooms)**     |
|   functional    |  int   | **Home functionality rating**<br>7 (Typ) : Typical Functionality<br>6 (Min1) : Minor Deductions 1<br>5 (Min2) : Minor Deductions 2<br>4 (Mod) : Moderate Deductions<br>3 (Maj1) : Major Deductions 1<br>2 (Maj2) : Major Deductions 2<br>1 (Sev) : Severely Damaged<br>0 (Sal) : Salvage only |
|   fireplaces    |  int   | **Number of fireplaces**                                     |
|  fireplace_qu   |  int   | **Fireplace quality**<br>5 (Ex) : Excellent - Exceptional Masonry Fireplace<br>4 (Gd) : Good - Masonry Fireplace in main level<br>3 (TA) : Average - Prefabricated Fireplace in main living area or Masonry Fireplace in basement<br>2 (Fa) : Fair - Prefabricated Fireplace in basement<br>1 (Po) : Poor - Ben Franklin Stove<br>0 (NA) : No Fireplace |
|   garage_type   | object | **Garage location**<br>2Types : More than one type of garage<br>Attchd : Attached to home<br>Basment : Basement Garage<br>BuiltIn : Built-In (Garage part of house - typically has room above garage)<br>CarPort : Car Port<br>Detchd : Detached from home<br>NA : No Garage |
|  garage_yr_blt  | float  | **Year garage was built**                                    |
|  garage_finish  | float  | **Interior finish of the garage**<br>3 (Fin) : Finished<br>2 (RFn) : Rough Finished<br>1 (Unf) : Unfinished<br>0 (NA) : No Garage |
|   garage_cars   | float  | **Size of garage in car capacity**                           |
|   garage_area   | float  | **Size of garage in square feet**                            |
|   garage_qual   | float  | **Garage quality**<br>5 (Ex) : Excellent<br>4 (Gd) : Good<br>3 (TA) : Typical/Average<br>2 (Fa) : Fair<br>1 (Po) : Poor<br>0 (NA) : No Garage |
|   garage_cond   | float  | **Garage condition**<br>5 (Ex) : Excellent<br>4 (Gd) : Good<br>3 (TA) : Typical/Average<br>2 (Fa) : Fair<br>1 (Po) : Poor<br>0 (NA) : No Garage |
|   paved_drive   |  int   | **Paved driveway**<br>2 (Y) : Paved<br>1 (P) : Partial Pavement<br>0 (N) : Dirt/Gravel |
|  wood_deck_sf   |  int   | **Wood deck area in square feet**                            |
|  open_porch_sf  |  int   | **Open porch area in square feet**                           |
| enclosed_porch  |  int   | **Enclosed porch area in square feet**                       |
|   3ssn_porch    |  int   | **Three season porch area in square feet**                   |
|  screen_porch   |  int   | **Screen porch area in square feet**                         |
|    pool_area    |  int   | **Pool area in square feet**                                 |
|     pool_qc     |  int   | **Pool quality**<br>4  (Ex) : Excellent<br>3 (Gd) : Good<br>2 (TA) : Average/Typical<br>1 (Fa) : Fair<br>0 (NA) : No Pool |
|      fence      |  int   | **Fence quality**<br>4 (GdPrv) : Good Privacy<br>3 (MnPrv) : Minimum Privacy<br>2 (GdWo) : Good Wood<br>1 (MnWw) : Minimum Wood/Wire<br>0 (NA) : No Fence |
|  misc_feature   | object | **Miscellaneous feature not covered in other categories**<br>Elev : Elevator<br>Gar2 : 2nd Garage (if not described in garage section)<br>Othr : Other<br>Shed : Shed (over 100 SF)<br>TenC : Tennis Court<br>NA : None |
|    misc_val     |  int   | **$Value of miscellaneous feature**                          |
|     mo_sold     |  int   | **Month Sold**                                               |
|     yr_sold     |  int   | **Year Sold**                                                |
|    sale_type    | object | **Type of sale**<br>WD : Warranty Deed - Conventional<br>CWD : Warranty Deed - Cash<br>VWD : Warranty Deed - VA Loan<br>New : Home just constructed and sold<br>COD : Court Officer Deed/Estate<br>Con : Contract 15\% Down payment regular terms<br>ConLw : Contract Low Down payment and low interest<br>ConLI : Contract Low Interest<br>ConLD : Contract Low Down<br>Oth : Other |
|    saleprice    |  int   | **Property's sale price in dollars**                         |

## File Navigation
```
Project_2_Reg_Challenge
|__ code
|   |__ regression_challenge_notebook.ipynb   
|	|__ kaggle_result.png
|__ datasets
|   |__ train.csv
|   |__ test.csv
|   |__ sample_sub_reg.csv
|   |__ submission.csv
|__ ames_reg_challenge.pdf
|__ README.md

```

## Data sources

### Provided

As part of the project, [train.csv](./datasets/test.csv), [test.csv](./datasets/test.csv) and [sample_sub_reg.csv](./datasets/sample_sub_reg.csv) files were provided. 

These sources of these data were pulled from the [Kaggle Challenge website](https://www.kaggle.com/c/dsi-us-6-project-2-regression-challenge/data)