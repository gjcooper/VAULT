# Helicopter predictive inference task

Whilst this note records one task, there are actually a whole family of tasks that have grown out of an attempt to implement the task design used in the work of #author/nassar_matthew_r, such as [[nassar2021all|All or nothing belief updating in patients with schizophrenia reduces precision and flexibility of beliefs]].

All the tasks to date have the context of a hidden "helicopter" that is dropping parcels. The goal of the participants is to catch as many parcels as possible, with partial catches being allowed. The location of the parcels are drawn from a Gaussian distribution centred on the hidden location of the helicopter. The helicopter may change location. The ways in which the helicopter changes location is the most common variation between the multiple tasks outlined below.

In brief, there are three finalised versions.

1. The original helicopter task had two blocks types, change-point blocks where the helicopter changed to a new location on the screen with a hazard rate of 0.125, and oddball blocks where the helicopter randomly walked on the screen, but occasionally (probability 0.125) a parcel would drop from a uniform distribution over the whole screen instead of the helicopter centred Gaussian.
2. The 2022 Honours task dropped the oddball version, and kept the change-point condition. Different blocks though had different levels of variance on the drop distribution.
3. The task version developed for clinical populations has no conditions, just multiple blocks of the change-point condition as per the first version.

More detail can be found at: https://github.com/university-of-newcastle-research/helicopter_versions (Access to the University of Newcastle Github account is needed to see that page)
