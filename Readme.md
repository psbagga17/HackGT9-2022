# Optimization of GT Buses using Reinforcement Learning

HackGT9 project focused on improving the allocation of buses on routes to maximize efficiency and minimize pain points.

## Background

This project is aimed to improve the student experience of using GT Buses by targeting efforts toward the administration. The goal is to suggest a more systematic allocation of buses based on student movement patterns around campus.

## Construction

**Model is trained for each day since population distributions differ on a daily basis

1 - GT does not collect any sort of bus data relating to passengers. As such, we modeled student population distributions across campus for various time slots on each day of the week by fetching course data (specifically: location, time slot, & class size).

2 - Formatted data by utilizing pandas and NumPy. Added & deleted data to ensure a smooth training and to reduce pain points.

3 - Created a custom RL environment with discrete action space. Developed a unique reward function defined as the (sum of over each time interval of (matrix grandsum of (sum over each bus route of (number of buses on that route * bus route score matrix * flow matrix)))). That score is passed into a quadratic function to punish actions with too many or few buses. Additional constraints are added to ensure robustness & minimize error.

## Sample Allocations

[# of red buses, # of blue buses, # of green buses, # of gold buses]

visit [bus.gatech.edu](bus.gatech.edu/routes) to view all GT bus routes

Monday [4, 8, 3, 0]

Tuesday [5, 8, 3, 1]

Wednesday [7, 5, 4, 3]

Thursday [3, 5, 2, 0]

Friday [6, 6, 5, 5]


## Collaborators

---

@kakhil2004 (Akhil Kothapalli)

Grover H. Susanibar Sipan

@NarenSavkur (Naren Savkur)

---