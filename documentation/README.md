# Where Did All The Great Women Go?
## Data & Methodology
The data for Where Did All The Great Women Go comes from multiple different sources. The main data draws from a 2020 case study conducted by a university in Spain on female role models, The Department of Education Statistics, and The U.S. Census. The sources and data queries are detailed below.

#### Table 1. Key visualization data sources

| Source Title | Description / Citation | URL |
| ----------- | ----------- | ----------- |
| 2020 Case Study on Female Role Models in STEM | Data on differences in mean rating of the 5 variables measured in the study were pulled from the final study documentation | https://www.frontiersin.org/articles/10.3389/fpsyg.2020.02204/full | 
| Data on Online Science Curriculums | Data on scientists taught about in the classroom parsed from 5 online education websites | https://thebestschools.org/features/50-influential-scientists-world-today/ , https://www.dkfindout.com/us/science/famous-scientists/ , https://www.educationworld.com/science/scientists.shtml , https://teachwithfergy.com/famous-scientists-who-changed-the-world/ , https://www.famousscientists.org/popular/ | 
| Percent of Bachelor's Degrees Awarded to Women in the US from 1970 to 2011 | Department of Education Statistics. Percent of Bachelor's degrees pertaining to STEM were pulled from the dataset | https://www.kaggle.com/sureshsrinivas/bachelorsdegreewomenusa |
| STEM and STEM-Related Occupations by Sex and Median Earnings: ACS 2019 | U.S. Census Data. Data on estimated number of men and women in each STEM occupation group was parsed from the dataset|https://www.census.gov/data/tables/time-series/demo/income-poverty/stem-occ-sex-med-earnings.html|
| Statistics on Turing Awards | Number of women who received Turing Awards and descriptions of them pulled from an article on the Turing Award | https://slate.com/technology/2020/01/turing-award-acm-women-recipients.html#:~:text=Since%201966%2C%2070%20computer%20scientists,Only%20three%20have%20been%20women |
| Statistics on Fields Medals | Number of women who received Fields Medals and descriptions of them pulled from an article on the Fields Medal | https://www.nature.com/articles/d41586-020-01681-2#:~:text=Maryam%20Mirzakhani%20broke%20into%20the,Fields%20Medal%2C%20established%20in%201936 |
| Statistics on Nobel Prizes in Medicine, Chemistry, and Physics | Number of women who received the Nobel Prize in Medicine, Chemistry, and Physics pulled from an article on the Nobel Prize | https://apnews.com/article/nobel-prizes-chemistry-archive-3227341e3086af0cfee34a695416eeb9#:~:text=In%201983%2C%20Barbara%20McClintock%20won,chemistry%20and%20four%20in%20physics |
| Biographies of women affected by The Matilda Effect | Bios were pulled from multiple different sources | Hedy Lamarr, Vera Rubin, Chien-Shiung Wu, Ada Lovelace, Katherine Johnson (https://www.marieclaire.com/culture/g5026/female-discoveries-credited-to-men/?slide=1), Trotula of Salerno (https://thebestschools.org/magazine/brilliant-woman-greedy-men/), Maria Merian (https://www.biography.com/news/alice-ball-female-scientists) |

### Case Study Data

Study was conducted at the Department of Business Economics, School of Business & Economics, Universidad CEU San Pablo in Madrid, Spain and the Internet Interdisciplinary Institute, Universitat Oberta de Catalunya (UOC) in Barcelona, Spain. Data on the difference in mean rating of the 5 variables measured in the study were pulled from the final study documentation. The 5 variables assessed are enjoyment in math, importance attached to math, gender stereotypes around math, expectations of math success, and likelihood of choosing a university degree across the following four STEM disciplines: math, physical science, computer science, and engineering. The study was conducted on 304 girls, who were given a survey to rate the variables above on a scale of 1 to 7 before and after being exposed to the female role models. All mean differences were significant with p values less than 0.05.

### Online Science Curriculums Data

The data on online science curriculums was manually compiled from 5 children's education websites (thebestschools.org, Dorling Kindersley, educationworld.com, Teach with Fergy, famousscientists.org). Each website had a list of scientists to teach about in the classroom. The amount of females/males per list was pulled and added manually to an excel sheet and saved as an csv file to create the final dataset.

### Awards Data

The data on the amount of women/men who were awarded the Turing Award, Fields Medal, and Nobel Prize in Medicine, Chemistry, and Physics were manually compiled from multiple different websites and used to create the SVG based visualizations.

### Bios of Women

The bios of the women were manually compiled from several different websites and added to an excel sheet. The excel sheet was changed to a json file which was used for the final grid visualization.

### Libraries and Media

Where Did All The Great Women Go was developed using vanilla JavaScript. The project is deployed using github pages. The following libraries were used to create visualizations and interactions of the visual essay:

* graph-scroll.js - used to run all of the transitions in the visualization and create the sticky element for scrolling.
* D3.js - used to create all visuals except for the awards visuals

All photos of the women were taken from creative commons and are CC0 and public domain.

SVG based illustrations (all awards visualizations and final visual of the women's names) were created in Adobe Illustrator.
