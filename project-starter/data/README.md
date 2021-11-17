# data

Place data file(s) in this folder.

Then, include codebooks (variables, and their descriptions) for your data file(s)
using the following format.

## lemurs

- `taxon`: Taxonomic code: in most cases, comprised of the first letter of the genus and the first three letters of the species; if taxonomic designation is a subspecies, comprised of the first letter of genus, species, and subspecies, and hybrids are indicated by the first three letters of the genus.
- `dlc_id`: Specimen ID: Unique DLC number assigned at accession of animal
- `hybrid`: Hybrid status: N=not a hybrid. S=species hybrid. B=subspecies hybrid. If sire is one of multiple possible and animal could be a hybrid, it is designated a hybrid.
- `sex`: M=male. F=Female. ND=Not determined
- `name`: House name: Animal name assigned at DLC
- `current_resident`: Whether or not the animal currently lives in the DLC colony.
- `stud_book`: Regional or global unique ID among captive individuals of that species; assigned by AZA studbook keeper. Not all individuals have studbook numbers in this data record.
- `dob`: Date of Birth (DOB) is an exact date unless there is an entry in the 'Estimated_DOB' field.
- `birth_month`: month of birth
- `estimated_dob`: Whether or not the date of birth is an estimate. Y=estimated to the nearest year, M to the nearest month, and D to the nearest day. If there is a number after the letter code, that indicates to the Nth value of the code. U=unknown. If there is no entry in this field, DOB is not an estimate.
- `birth_type`: Whether the animal was captive-born (CB), wild-born (WB) or of unknown birth type (UNK)
- `birth_institution`: Name or ISIS abbreviation of institution where animal was born. Duke Prim=DLC. For wild caught animals, birth institution = country of origin, if known
- `litter_size`: Number of infants in the litter the focal animal was born into (including focal animal). Only indicated where verifiable (born at DLC). A missing value indicates that the litter size is unknown
- `expected_gestation`: 	Values based on DLC observations and reports from the literature, in days
- `estimated_concep`: Date of estimated conception: Calculated as (DOB-Expect ed_Gestation)
- `concep_month`: Month of estimated conception: Identified from Estimated_Concep
- `dam_id`: 	Specimen ID of female parent. DLC unique ID preferred if there is one. Local ID of another ISIS-reporting institution if known and no DLC number exists. 'Wild' indicates dam of wild-caught individual. 'Unk' or no data indicates dam is unknown
- `dam_name`: House name of female parent (at DLC)
- `dam_taxon`: Taxon of female parent: Based on taxonomic code (see description)
- `dam_dob`: 	Date of birth of female parent: If female parent is wild caught or of unknown origin, this date is an estimate
- `dam_age_at_concep_y`: Estimated age of female parent at conception of focal animal: in years ((Estimated_Concep-Dam_DOB)/365)
- `sire_id`: Specimen ID of male parent: DLC number preferred if there is one. Local ID of another ISIS-reporting institution if known and no DLC number exists. 'Wild' indicates sire of wild-caught individual. 'MULT' indicates multiple possible sires. A following number indicates number of possibilities (e.g. MULT2). 'Unk' or no data indicates unknown sire and may include cases of multiple possible sires.
- `sire_name`: House name of male parent (at DLC)
- `sire_taxon`: Taxon of male parent: Based on taxonomic code described above
- `sire_dob`: Date of birth of male parent: If male parent is wild caught or of unknown origin, this date is an estimate.
- `sire_age_at_concep_y`: 	Estimated age of male parent at conception of focal animal: in years ((Estimated_Concep-Dam_DOB)/365)
- `dod`: Date of death: Verified date an animal died. Missing indicates animal is either alive or status is unknown
- `age_at_death_y`: Age of animal at verifiable date of death, in years ((DODDOD)/ 365). Missing indicates animal is either alive or status is unknown.
- `age_of_living_y`: Age if alive: Verifiable living age of DLC-owned animals and/or current residents at DLC on loan, in years as of the date the datafile was updated ((date of last upda te-DOB)/365). Missing indicates animal is either dead or status is unknown.
- `age_last_verified_y`: Last verifiable age: Age of animal at most recent date a non-DLC owned, non-current resident animal was verifiably alive, in years. Dates were obtained from ISIS as entered by other institutions (dates of live weight or animal transfer) or via direct communication from other animal facilities. ((DateLastVerified-DOB)/365). Missing indicates animal is known to be dead or alive.
- `age_max_live_or_dead_y`: Maximum age: The animal's age from any of the three age categories (each individual must have a value in one of the three) indicating the maximum age the animal could have achieved as of the date the datafile was updated.
- `n_known_offspring`: Number of offspring: Number of offspring the individual is known to have produced. There may be additional offspring for this individual if they were born at another institution or if this individual is a possible, rather than known, parent.
- `dob_estimated`: Whether or not the date of birth is an estimate. Y=estimated to the nearest year, M to the nearest month, and D to the nearest day. If there is a number after the letter code, that indicates to the Nth value of the code. U=unknown. If there is no data in this field, DOB is not an estimate.
- `weight_g`: Weight: Animal weight, in grams. Weights under 500g generally to nearest 0.1-1g; Weights >500g generally to the nearest 1-20g.
- `weight_date`: Weight date: Date animal was weighed
- `month_of_weight`: 	Weight month: Month of the year the animal was weighed
- `age_at_wt_d`: Age in days: Age of the animal when the weight was taken, in days (Weight_Date-DOB)
- `age_at_wt_w`: Age in weeks: Age of the animal when the weight was taken, in weeks ((Weight_Date-DOB)/7))
- `age_at_wt_mo`: Age in months: Age of the animal when the weight was taken, in months (((Weight_Date-DOB)/365)*12)
- `age_at_wt_mo_no_dec`: Age in months with no decimal: AgeAtWt_mo value rounded down to a whole number for use in computing average individual weights (FLOOR(AgeAtWt_mo))
- `age_at_wt_y`: Age in years: Age of the animal when the weight was taken, in years ((weight_date-DOB)/365
- `change_since_prev_wt_g`: Weight difference: Difference, in grams, between this weight and the animal's previous weight
- `days_since_prev_wt`: Days difference: Difference, in days, between the date of this weight and the date of the animal's previous weight
- `avg_daily_wt_change_g`: Average daily change: Average daily weight change, in grams, between this weight and the animal's previous weight
- `days_before_death`: Days before death: Number of days before the animal's death the weight was taken (DOD- Weight_Date). Missing indicates animal is either alive or status is unknown.
- `r_min_dam_age_at_concep_y`: Dam minimum age at conception, in years, for the species from the life history summary table. Used to calculate 'Age_Category' as described below.
- `age_category`: Age category: IJ (infant or juvenile): (AgeAtWt_yr < R_Min_Dam_Age_AtConcep_yr). Young-adult: (Min_Dam_AgeAtConcep_yr <= AgeAtWt_yr < 2xMin_Dam_AgeAtConcep_ yr). Adult: AgeAtWt_yr >= 2xMin_Dam_A geAtConcep_yr
- `preg_status`: Pregnancy status: Whether or not animal is pregnant on date weight was taken. P=pregnant, NP=not pregnant (all males coded NP)
- `expected_gestation_d`: Expected gestation length: Values based on DLC observations and reports from the literature, in days
- `concep_date_if_preg`: Conception date: Estimated date of infant conception if the weight was taken while a female was pregnant
- `infant_dob_if_preg`: Infant Date of Birth: Date of infant birth if the weight was taken while a female was pregnant
- `days_before_inf_birth_if_preg`: Days until birth: Days remaining in the pregnancy if the weight was taken while a female was pregnant
- `pct_preg_remain_if_preg`: 	% of pregnancy remaining: Percentage of pregnancy remaining when weight was taken from a pregnant female calculated as (days_BF_inf_birth/Expected_Gestation)
- `infant_lit_sz_if_preg`: Infant litter size: Number of infants in the litter a female produced if she was pregnant on date weight was taken
