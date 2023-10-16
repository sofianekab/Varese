# Insee TCM example


For most households studies, Insee uses an harmonised series of questions to get information on the household, the persons and the dwelling (TCM for Tronc Commun des Ménages, or Common Core for Households). It can be used for one-time, or repeated over time for longitudinal surveys. It can be used as a whole or partly depending on the survey’s needs.

To illustrate (variables are in capital):

For each person in the dwelling the name (`PRENOM`), sex (`SEXE`) and age (`AGE`) is asked.

If the value of the variable `AGE` is greater than a certain threshold (15 by default), the person is asked about her situation regarding employment (`SITUA`) and if she has made at least one hour of paid work over the last week (`TRAREF`).

If the person is in employment (`SITUA=1`) but has not worked over the last week (`TRAREF=2`), the person is asked for a reason: holiday, leaves for sickness, part-time work, strike… (`RABS`).

The person is also asked a serie of questions to determine her occupation/trade (`PROFESSION`)

In case the person is re-interrogated, she is asked if her occupation is the same (`CFPROFESSION`). If not the serie of questions to determine her occupation/trade is asked again.

Currently, the question about the situation regarding employment is asked in many surveys (households budget survey, use of internet and telecommunication survey, labour force survey…). Represented variables `SITUA` have been created multiple times, one in each survey without links between them. Also, the questionnaire changed in 2022: the variable `SITUA` is now `SITUAEU`: it has one code less and the order and labels of the other codes has partly changed.

There is also a question whether the represented variable `SITUA` should be considered the same between surveys if the target population of the survey is not exactly the same.

On the matter of population/universe, there is also a question if it should be the same for the whole survey. For example, the `RABS` variable is strictly speaking only about persons in employment, the SITUA variable about persons over 15, when the survey would be about “persons living in a dwelling in France” as it is taken from the sample frame.
