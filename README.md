# Introduction to Digital Classics / Einführung in die "Digital Classics"

Block Seminar at the University of Rostock.

See <https://studip.uni-rostock.de/dispatch.php/course/details/index/111358225f25f791f8cce36960af243f>

Dates:

* 10.-11.12.2017 (Fri/Sat)
* 1.-2.12.2017 (Fri/Sat)

A GitHub repository for the course can be found [here](https://github.com/mromanello/DigiClass_UniRostock2017).

``` python

import codecs
import numpy as np
import pandas as pd

df = pd.read_csv("dayofquotes_full.csv", encoding="utf-8")

print(df.head())

for n, row in df.iterrows():
    name = row["name"].lower().replace(" ","_") if row["name"] is not np.nan else "anonym" 
    date = row["date"].split("-")[0]
    with codecs.open("dayofdhquotes/%i_%s_%s.txt" % (n + 1, name, date), "w", "utf-8") as f:
        f.write(row["quote"])
        
```

## Description

This intensive seminar (Blockseminar, 2 SWS) offers an introduction to Digital Classics for philology students, and does not require any prior technical knowledge, but just a basic level of [digital literacy](https://en.wikipedia.org/wiki/Digital_literacy).

Students will first gain some historical knowledge about Digital Humanities as a discipline, and of Digital Classics as a research area and community of practice. Then, they will be introduced to various digital methods, tools and technologies that can be applied to the core activities of classical philologists (i.e. reading, writing/publishing, collating, editing, translating, annotating).

During the practical sessions (accounting for approx. 30% of the course time) students will get to know the tools available to carry out each of these core activities in a digital environment, as well as the underlying standards and technologies. By doing so, they will develop a solid understanding of the problems related to the digital representation of philological data.

(The course is taught mostly in English, while the use of German in the classroom is possible and welcome, especially during the practical session. Structure of the course: frontal lessons (60-70%) + practical sessions (30-40%). A personal laptop is required for the practical sessions.)

--

## Detailed schedule

### Seminar 1 /10 Nov 2017

- 15:00-15:45 Lecture 1
- 16:15-16:30 Coffee break
- 16:30-17:15 Lecture 2
- 17:15-18:00 Practical session
- 18:00-19:00 Time for assigned reading

### Seminar 2 / 11 Nov 2017

#### AM

- 9:00-10:00 Time for assigned reading
- 10:00-10:45 Lecture 3
- 10:45-11:00 Coffee break
- 11:00-11:30 Lecture 4
- 11:30-12:15 Practical session
- 12:15-13:30 Lunch Break

#### PM

- 13:30-14:15 Lecture 5
- 14:15-15:00 Practical session
- 15:00-15:15 Coffee break
- 15:15-16:00 Lecture 6
- 16:00-16:45 Practical session
- 17:00-17:15 Coffee break
- 17:15-18:00 Lecture



### Seminar 3

TBD

### Seminar 4
 
 TBD