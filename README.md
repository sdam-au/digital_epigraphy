# Inscriptions as data: digital epigraphy in macro-historical perspective 
*PUBLICATION*

---

## Abstract
[In two to three sentences state the purpose of this repository, ideally tying it to an existing SDAM milestone. E.g., The purpose of this repository is to provide templates for all future SDAM repositories in order to save precious time and maintain high standards and uniformity of our documentation.]

---
## Authors
* Petra Hermankova [![](https://orcid.org/sites/default/files/images/orcid_16x16.png)](https://orcid.org/0000-0002-6349-0540), Social Dynamics in the Ancient Mediterranean project, Aarhus University, petra.hermankova@cas.au.dk
* Vojtech Kase, Social Dynamics in the Ancient Mediterranean project, Aarhus University
* Adela Sobotkova, Social Dynamics in the Ancient Mediterranean project, Aarhus University

## License
CC-BY-SA 4.0, see attached [License.md](https://github.com/sdam-au/digital_epigraphy/blob/master/LICENSE.md)

## DOI
[Here will be DOI or some other identifier once we have it]

### References
[How to cite this resource]

---

# Data
1. [Epigraphic Database Heidelber (EDH)](https://edh-www.adw.uni-heidelberg.de/home) dataset is accessed and transformed by the series of Python and R scripts in [EDH ETL repository](https://github.com/sdam-au/EDH_ETL) and in [EDH exploration repository](https://github.com/sdam-au/EDH_exploration), created by SDAM Project. The latest version of the dataset (as JSON file) can be accessed via Sciencedata.dk or at this link: [EDH_public folder](https://sciencedata.dk/shared/b6b6afdb969d378b70929e86e58ad975)

* Result of ETL process JSON file: `EDH_text_cleaned_2021-01-21.json`

* [EDH dataset metadata](https://docs.google.com/spreadsheets/d/1O_4EH-POKqUgq5K-B1DbbJQ8WWF0NQ6s12dCiW29MbA/edit?usp=sharing)

2. [Epigraphic Database Clauss-Slaby (EDCS)](http://www.manfredclauss.de/) dataset is accessed and transformed by the series of Python and R scripts in [EDCS ETL repository](https://github.com/sdam-au/EDCS_ETL), created by SDAM project. The latest version of the dataset (as JSON file) can be accessed via Sciencedata.dk or at this link: [EDCS_public folder](https://sciencedata.dk/shared/1f5f56d09903fe259c0906add8b3a55e). 

* Result of ETL process JSON file: `EDCS_text_cleaned_2021-03-01.json`

* [EDCS dataset metadata](https://docs.google.com/spreadsheets/d/17k4quLM6RiEu821n3caitK8labzuurIGmzf0W1bHnss/edit?usp=sharing) with descriptions for all attributes.

## Data Access

**Access with R (using custom `sdam` package)**

```r
resp = request("EDH_text_cleaned_2021-01-21.json", path="/sharingin/648597@au.dk/SDAM_root/SDAM_data/EDH/public", method="GET")
```

**Access with Python (using custom [SDDK package](https://pypi.org/project/sddk/))**

```python
!pip install sddk
import sddk
auth = sddk.configure("SDAM_root", "648597@au.dk") # where "648597@au.dk is owner of the shared folder
EDH_utf8 = sddk.read_file("public/b6b6afdb969d378b70929e86e58ad975/EDH_text_cleaned_2021-01-21.json", "df", auth)
```







