# Analysis and Management of Production System

# Lesson 2: Introduction to Factory Models

Prof. Giulia Bruno

Department of Management and Production Engineering

giulia.bruno@polito.it

# Factory model

V Analytical approach for the modeling and analysis of manufacturing and production systems

>Firstly, extremely simple models (single machine models)are developed to show the necessary mechanics and concepts needed   
>Then, more complex models are developed by connecting simple models into networks of workstations with the appropriate interconnections

Overall approach

1． decompose a system into small components   
2． model components   
3． reintegrate the general system by appropriate combination of submodels

# Factory model

Decomposition approach is an approximation   
> Produces acceptable results in a wide variety of manufacturing applications   
> Any analytical model (exact or approximate) is an approximation of the real world environment   
Question to be answered: whether or not the model yields accurate enough results to be used as an analysis tool in support of design and operational decision making

# Factory model

> Modelled system doesn't take into account where or why jobs arrive or how they are transported to customers   
>modeling the order creation or completed job delivery systems is not within the scope of our analysis   
> Arriving job is a physical entity to be processed through the various processing steps or an order to begin the processing of raw material into a newly manufactured entity

### Visual Diagram: Modeled System Boundary
- **Overall Layout**: A schematic diagram showing input, a central process, and output.
- **Text Label**: "Modeled System" is positioned at the top, outside the curved boundary.

#### 1. Input
- **Visual Element**: An arrow originating from the left, pointing horizontally to the right.
- **Text Label**: "Orders" is positioned at the start of the arrow.

#### 2. Central Component
- **Visual Element**: A rectangular box located in the center of the diagram. The input arrow terminates at its left edge.
- **Text Label**: "Factory" is written inside the box.

#### 3. Output
- **Visual Element**: An arrow originating from the right edge of the central box, pointing horizontally to the right.
- **Text Label**: "Completed Jobs" is positioned above the output arrow.

# Notations and definitions

> Factory composed by several machines grouped together by type (called workstations) and series of jobs to be produced on the machines   
> Processing steps for a job consists of several processing operations to be performed by different machines in a specified sequence   
Jobs move through the factory, waiting in line at a workstation until their turn for being processed by the machine,then proceeding to the next workstation to repeat this sequence until all required operations have been completed   
V Jobs arrive at the factory either individually or in batches based on some distribution of the time between arrivals

# Workstation

> Collection of one or more identical machines or resources (i.e. machines which perform the same function)

# Routing

Sequence of processing steps for a job   
> Jobs with identical routings are said to be of the same job type

different job types are jobs with different routings

### Visual Diagram: Factory Routing and Job Flow
- **Component Type**: Network Flow Diagram.
- **Logic**: Illustrates how jobs travel through a complex manufacturing system via specific sequences of workstations, defining their routing.

#### 1. System Components
- **Workstations (WS)**: The square boxes labeled "WS" represent the machines or resources where processing operations occur.
- **Jobs and Orders**: Cylindrical icons represent physical entities. The cluster on the left is labeled "Job" (representing incoming work), while the final entity on the far right is labeled "Order".
- **Buffers**: Intermediate cylindrical icons between some workstations indicate where jobs might wait in a queue before the next processing step.

#### 2. Routing Paths
- **Material Flow**: Magenta arrows connect the workstations, mapping the physical flow of materials from one station to the next.
- **Highlighted Sequences**: Distinct colored outlines (orange, green, and pink) group specific sequences of workstations together. The label "**Routing**" points directly to these highlighted paths.
- **Functional Meaning**: The diagram visually defines a routing as the exact sequence of processing steps a specific job must follow from entry to completion. It also shows that a factory can have branching and converging paths; jobs that share the exact same highlighted path belong to the same "job type," while different paths represent different job types.

# Performance measures

Cycle time: time a job spends in a system

> Average cycle time of the line is denoted as CT   
> Sometimes called Lead Time, even if LT identifies the a priori evaluation of the cycle time (time allocated to a operation sequence to produce a certain job)

Work in process: number of jobs within a system (from the beginning to the end of the operations sequence) which are either undergoing processing or waiting in a queue for processing   
>Average work-in-process is denoted as WIP

V Throughput rate: number of completed jobs leaving the system per unit of time

>Throughput rate averaged over many jobs is denoted by TH

# Cycle time

Notational distinction

>average factory cycle time denoted as CTs   
>average cycle time at workstation i, denoted as CT(i)

> CTs: average time that a job spends within the factory, either being processed at a workstation or waiting in a workstation queue;   
CT(i): average time jobs spend being processed by workstation i plus the average time spend in the workstation i queue (or buffer)   
CT: used for general properties related to the average cycle time will be developed

# Cycle time

> Processing time often known or can be determined without much effort   
Queue time not easily estimated for a given job

>it depends on the number and processng times of the various types of jobs that are waiting in the queue ahead of the designated job   
V Average cycle time at workstation i given as the sum of two components:

$$
\mathsf {C T} (\mathsf {i}) = \mathsf {C T} _ {\mathsf {q}} (\mathsf {i}) + \mathsf {E} [ \mathsf {T} _ {\mathsf {s}} (\mathsf {i}) ]
$$

where Ts(i) denotes the service time (or processing time) at workstation i

# Factory analysis

> For most analyzed systems, long-run throughput rate is equal to the input rate of jobs   
> Main issue: estimation of the total length of time for the manufacturing process (CTs)   
The higher the factory capacity, the faster jobs are completed

>Cycle time increases as the factory becomes busier

# Factory analysis

Time dependent measures such as CTs(t) and WIPs(t) are very difficult to develop

>Focus restricted to the “steady-state" measures i.e., the limiting value of the time dependent measures   
>By a property called the ergodic property, steady-state values can also be considered to be time-averaged values as time becomes very large

> Steady-state measures are independent of the initial conditions of the system   
> In the queueing theory, results are for steady-state system measures

# Factory analysis

> System's performance measures CT and WIP can be estimated from the arrival and departure streams of the system   
Define Tai as the arrival time of the in job,and the function A(t) for t ≥ O as the total number of arrivals during the timeinterval [0, f]   
> Define Tai as the departure time of the injob,and the function D(t) for t ≥Oas the total number of departures during the interval [0, f]

### Visual Diagram: Factory Analysis - Arrival and Departure Streams
- **Component Type**: Cumulative flow diagram.
- **Logic**: Illustrates how system performance measures like Cycle Time (CT) and Work-in-Process (WIP) can be estimated by tracking the cumulative number of jobs entering and leaving the system over time.

#### 1. Axes
- **Y-axis**: "Cumulative number of jobs" representing the total running count of items.
- **X-axis**: "time" representing the elapsed observation period.

#### 2. Step Curves
- **Arrivals ($A(t)$)**: The upper step function. It represents the total number of arrivals during the time interval [0, t]. Each vertical jump indicates the exact arrival time ($T_{ai}$) of a new job into the system.
- **Departures ($D(t)$)**: The lower step function. It represents the total number of departures during the interval [0, t]. Each vertical jump indicates the exact departure time ($T_{di}$) of a completed job leaving the system.

#### 3. Functional Meaning and Metrics
- **WIP (Vertical Difference)**: At any specific point in time $t$, the vertical distance between the arrivals curve and the departures curve ($A(t) - D(t)$) equals the exact number of jobs currently residing inside the system ($N(t)$).
- **Cycle Time (Horizontal Difference)**: The horizontal distance between the two curves for a specific job index $i$ represents that job's cycle time, calculated as Departure Time minus Arrival Time ($T_{di} - T_{ai}$).
- **System Averages**: The total area between these two curves over a given time interval represents the integral of the number of jobs in the system. This area is the mathematical foundation used to calculate the time-averaged WIP and average Cycle Time, ultimately leading to Little's Law ($WIP = \lambda \times CT$).

# Factory analysis

> Consider a time interval (a,b) such that the system starts empty and returns to empty   
> Let Nab be the number of jobs that arrive to the system during the interval (a, b)   
> Number these jobs from 1 to N,with index i representing specific jobs.   
Then the average waiting time, CT(a,b), for jobs during this interval is given by

$$
C T (a, b) = \frac {1}{N _ {a b}} \sum_ {i = 1} ^ {N _ {a b}} (T _ {i} ^ {d} - T _ {i} ^ {a})
$$

# Factory analysis

The area, AB, between the curves A(t) and D(t) for a < t < b is merely the summation given in the above equation. This area can also be obtained by standard integration methods as

$$
A B = \int_ {a} ^ {b} (A (t) - D (t)) d t
$$

The area represents the integral of the number of jobs in the system at time t, since N(t) = A(t)-D(t) is the number of jobs in the system at t. So the time-averaged number of jobs waiting in the system during the time interval (a, b) is given by

$$
W I P (a, b) = \frac {1}{b - a} \int_ {a} ^ {b} (A (t) - D (t)) d t
$$

# Factory analysis

There is a relationship between the average number in the system during the interval (a, b) and the average waiting time or cycle time in the system during this interval. Since the area between A(·)and D( -) (namely AB) is constant regardless of the method used to measure it, we have

$$
C T (a, b) = \frac {1}{N _ {a b}} A B \quad W I P (a, b) = \frac {1}{b - a} A B
$$

Thus,the following relationship is obtained

$$
W I P (a, b) = \frac {N}{b - a} C T (a, b)
$$

# Factory analysis

V The mean number of jobs arriving to the system per unit time, normally denoted as λ, is Nab/(b-a), thus

$$
W I P (a, b) = \lambda C T (a, b)
$$

>This result is valid for any interval that starts with an empty system and ends with an empty system   
> In fact this relationship is the limiting behavior result,or long run average result, for stationary queueing systems,and is known as Little's Law   
> The result holds for individual workstations as wellas the system as a whole

# Factory analysis

> For a system that satisfies steady-state conditions, the following equation holds

$$
\mathrm {W I P} = \lambda \times \mathrm {C T}
$$

where WIP is the long-run average number of jobs in the system, CT is the long-run average cycle time and λ is the long-run input rate of jobs to the server

> Since the average input rate is usually equal to the average throughput rate, Litle's Law can also be written as

$$
W I P = t h \times C T
$$

# Factory analysis

> The formula estimates mean values, but the actual underlying random variables of the systems can be quite variable   
> In most single workstation system models, the average number in the system,WIP, can be easily obtained. However, the behavior of the random variable representing the number in the system at any one point in time can be highly variable

# Factory analysis

Term steady-state implies that the mean reaches a limiting value and thus ceases to change with respect to time

>lt does not imply that the system itself ceases to change

Variability continues forever

>fluctuations within the system never cease

> Steady-state does imply that the entire distribution reaches a limiting value

>not only the mean but also the standard deviation, skewness,and other such measures will have limiting values

# Exercise 1

A workstation with a single machine for processing has a long-run average inventory level (WiP) of 25 jobs. The average rate at which jobs enter the workstation is 4 per hour, and the average processing time is 14.5 minutes per job. What is the average time that a job spends in the queue?

# Exercise 1 Solution

# DATA

WIP = 25 pcs   
rate =>= 4 pcs/hr   
E[Ts]= 14.5 min = 14.5 14.5= 0.24 hrs   
CTq =？

### Visual Diagram: Workstation Input/Output Balance
- **Component Type**: Basic system block diagram.
- **Logic**: Illustrates the steady-state assumption for a single workstation where the arrival rate equals the departure rate.

#### 1. Input Flow
- **Visual Element**: An arrow pointing from left to right towards the central block.
- **Text Label**: "λ" (lambda), representing the arrival rate or input rate of jobs into the system.

#### 2. Central Component
- **Visual Element**: A light blue rectangular box.
- **Text Label**: "WS", representing the Workstation.

#### 3. Output Flow
- **Visual Element**: An arrow pointing from left to right away from the central block.
- **Text Label**: "TH = λ", indicating that the system's Throughput (TH) is equal to its input arrival rate (λ).

# Exercise 1 Solution

According to the Little's Law: WIP = TH × CT

Supposing to have no losses or reworks,we can say that TH = λ and the equations becomes:

$$
W I P = \lambda \times C T
$$

Thanks to this,we can find out the Cycle Time of the station:

$$
C T = \frac {W I P}{\lambda} = \frac {2 5}{4} = 6. 2 5 h r s
$$

We also know that CT = CTa +E[TS]

So,

$$
C T _ {q} = C T - E [ T _ {S} ] = 6. 2 5 - 0. 2 4 = 6. 0 1 h r s
$$


# Exercise 2

Consider a factory operating 24 hours per day consisting of two workstations. Arrivals to the first station occur at a rate of 10 per day. The long-run average time that a job spends at the first workstation is 4.2 hours. After processing at the first workstation,a job is sent directly to the second workstation where it spends an average of 5.3 hours. After processing at the second workstation, the job leaves the system.What is the average work-in-process within the factory?

# Exercise 2 Solution

Shift = 24 hrs/day   
rate(𝜆) = 10 pcs/day = 24 pcs/hr = 0.417 pcs/hr   
CT1 = 4.2 hrs   
CT2 = 5.3 hrs

### Visual Diagram: Two Workstations in Series
- **Component Type**: Basic system flow diagram for a serial production line.
- **Logic**: Illustrates a sequential manufacturing process where jobs must pass through multiple processing steps in a specific order.

#### 1. Initial Input Flow
- **Visual Element**: An arrow pointing from left to right towards the first block.
- **Functional Meaning**: Represents the arrival of raw materials or incoming jobs entering the system.

#### 2. First Processing Stage
- **Visual Element**: The first light blue rectangular box.
- **Text Label**: "WS 1" (Workstation 1).

#### 3. Intermediate Flow
- **Visual Element**: An arrow connecting WS 1 to WS 2.
- **Functional Meaning**: Represents the physical transfer of semi-finished goods. The output (Throughput) of the first workstation serves as the direct input for the second workstation.

#### 4. Second Processing Stage
- **Visual Element**: The second light blue rectangular box.
- **Text Label**: "WS 2" (Workstation 2).

#### 5. Final Output Flow
- **Visual Element**: An arrow pointing from left to right away from WS 2.
- **Functional Meaning**: Represents the completed jobs leaving the system after finishing all required operations across both workstations.

# Exercise 2 Solution

Computation of WIP level related to WS1 and WS2 with the Litle's Law:

> WIP1 = λ × CT = 0.417 × 4.2 = 1.75 pcs   
? WIP2 = λ × CT2 = 0.417 × 5.3 = 2.21 pcs

Total WIP given by the sum of the two WIP related to the single stations:

WIPtot = WIP1 +WIP2 = 1.75 + 2.21= 3.96 pcS

# Penny Fab model

Factory that makes only one type of product   
Four processing steps to be performed in sequence   
Each processing operation performed on a separate machine   
V Machines process only one unit of the product at a time (a job)   
Constant processing times: 1, 2, 1 and 1 hour(s) respectively   
Constant WIPs

>when a job has completed its four processing steps, it is immediately removed from thefactory and a new job is started at Machine 1 to keep the total factory WIPs at the specified level

# Penny Fab model

### Visual Diagram: Penny Fab Model (Constant WIP System)
- **Component Type**: Production line schematic.
- **Logic**: Illustrates a simplified factory model used to study the relationship between Cycle Time, Throughput, and Work-In-Process (WIP).

#### 1. Workstations in Series
- **Visual Elements**: Four square boxes representing sequential processing steps performed on separate machines.
- **Processing Times**: The numbers inside the boxes (1, 2, 1, 1) represent the constant processing time in hours for each machine.
- **Bottleneck**: The second machine is the bottleneck of this line, as it has the longest processing time (2 hours). This strictly limits the maximum throughput of the entire factory to 0.5 jobs/hour.

#### 2. The Constant WIP Loop (CONWIP)
- **Visual Element**: A long feedback arrow connecting the "out" point back to the beginning of the line as a "new" entry.
- **Functional Meaning**: This loop visually represents the **Constant WIP** policy. It dictates that a new job is allowed to enter Machine 1 *only* when a completed job immediately exits the factory. This mechanical rule ensures that the total number of jobs currently active inside the system (the WIP level) remains strictly fixed at a specific level decided by management.

Constant WIPs level fixed at 10 jobs decided by the Management   
> Result a th= O.5 job/h (one finished job every two hours on the average is produced)   
V Equal to the maximum throughput rate for this factory because its slowest processing step (at Machine 2) takes two hours per job   
> Jobs can be completed no faster than this single machine completes its own processing

# Penny Fab model

Y Management pleased with the throughput of the factory since it is at its maximum capacity, but concerned with the cycle time (20 hours per job)   
Very high since it only takes 5 hours of processing to complete each job   
V The x-factor for a factory is the ratio of CTs to the average total processing time per job   
X-factor = 4   
From literature analysis the x-factor for this sector is 2.6   
Y Management is worried about the ability to keep customers when the industry on average produces the same product with a considerably shorter lead-time from order placement to receipt

# Penny Fab model

Y Possible solution to address the cycle time problem: purchase a 25% faster machine (1.5 hours) for processing step two   
> This purchase would be made expressly for the purpose of reducing the x-factor for the factory to be more in line with the industry average   
The company selling the machine says that this investment will bring the x-factor down to 3.33 and the additional throughput of 0.166 units per hour would pay for the cost of the new machine in three years

# Penny Fab model

V Management decided that investment is not worthwhile just based on increased throughput   
V Funds needed to buy the machine are needed for other aspects of the company (e.g., research and development)   
> Hiring of a consulting team from the manufacturing engineering department of a local university to perform a short term factory flow analysis study   
First activity to devise a method of predicting the long-term factory performance measures of cycle time and throughput

# Penny Fab model

Hand simulation procedure of the factory flow   
V Beginning: 10 jobs al placed at Machine 1, then hourly updates to each job's status   
V Jobs soon distributed themselves throughout the factory and after a short period of time a two-hour cyclic pattern emerged   
V Every cycle of this pattern produced one completed job and the factory returned to the identical state for each machine and associated queue

>This set of conditions is referred to as the factory status

All the job cycle times had identical values after the system reached the cyclic behavior pattern (20 h,agreed with the company)

# Penny Fab model

Factory simulation with WIP = 10 for one 24-hour day   
Status (X,Y)

> X: number of jobs at the WS (queue + processing)   
Y: number of hours already completed for the job in processing

After hour 15 the factory status repeats every two hours (factory status at the start of hours 15, 17, 19, 21, etc. are identical)

### Visual Diagram: Factory Simulation Table
- **Component Type**: Data table (Hourly simulation).
- **Logic**: Shows the evolution of the numerical state of 4 workstations and the cumulative production over 24 time intervals.

#### 1. Column Structure
- **Time**: A sequential timeline from hour 0 to 24.
- **WS #1, WS #2, WS #3, WS #4**: The four workstations. The data within them is formatted as pairs of numbers in parentheses, for example, `(10,0)` or `(3,1)`. *(Note from previous slides: this represents `(Jobs at WS, Hours already completed)`)*.
- **Cum. Thru.** (Cumulative Throughput): An incremental counter that starts at 0 and ends at 10.

#### 2. Data Trends (Direct Observations)
- **Initial State (Time 0)**: The entire workload of 10 jobs is located at WS #1, shown as `(10,0)`. All other stations show `(0,0)` and the cumulative production is 0.
- **First Output**: The "Cum. Thru." counter registers its first tick from 0 to 1 at "Time 5".
- **Repetitive Pattern (From Time 16 to 24)**: Looking at the final portion of the table, a precise cyclic pattern emerges that repeats every two hours:
    - **In the even rows** (16, 18, 20, 22, 24): The values are exactly identical: `(0,0)` at WS #1, `(9,1)` at WS #2, `(0,0)` at WS #3, and `(1,0)` at WS #4. The "Cum. Thru." counter remains unchanged from the previous row.
    - **In the odd rows** (17, 19, 21, 23): The values alternate to: `(1,0)` at WS #1, `(8,0)` at WS #2, `(1,0)` at WS #3, and `(0,0)` at WS #4. At these specific rows, the "Cum. Thru." always increases by +1.
- **Final Result**: At "Time 24", the final value of the Cumulative Throughput is 10.

# Penny Fab model

V The consulting team decided to estimate the x-factor for various numbers of jobs in the system (WIP)   
From Little's Law: CT=WIP/th   
> In this case, th=0.5 j/h, then CT=2*WIP   
Processing time = 5h, then x=CT/5=WIP/2.5   
> In order to have the desired x-factor (2.6), the WIP must be 6.5   
How the th change by varying WIP?

# Penny Fab manual simulation

### Visual Diagram: Penny Fab Manual Simulation (WIP = 1)
- **Component Type**: State-time diagram (Manual simulation).
- **Logic**: Shows the physical progression of a single item (WIP = 1) through the production line hour by hour.

#### 1. Line Setup (Top)
- It defines the 4 workstations (WS1, WS2, WS3, WS4) and their respective processing times: $t_1=1h$, $t_2=2h$, $t_3=1h$, $t_4=1h$.
- Since the WIP is constantly kept at 1, there is only one cylinder (representing the "job" or item) in the entire factory at any given time.

#### 2. Time Evolution (Subsequent rows)
- **t = 0h**: The item enters the system and starts processing at WS1.
- **t = 1h**: After processing at WS1 (which takes 1h), the item moves to WS2.
- **t = 2h**: The item is still at WS2. Since WS2 requires 2 hours of processing, the item must stay there for an additional hour.
- **t = 3h**: Processing at WS2 is complete, and the item moves to WS3.
- **t = 4h**: Processing at WS3 is complete (1h), and the item moves to WS4.
- **t = 5h**: The item exits the line as a finished product. Because this is a constant WIP system, at the exact moment an item exits, a new item enters WS1.

#### 3. Results and Metrics (Text on the right and bottom)
- **Cycle Time (CT)**: Because there are no other items in the system, the item never waits in a queue. Its Cycle Time is exactly equal to the total raw process time ($T_0$): $1+2+1+1 = \mathbf{5\text{ hours}}$.
- **Throughput (TH)**: Exactly 1 item exits every 5 hours. Therefore, the Throughput is $\frac{1}{5} = \mathbf{0.2\text{ pcs/h}}$.
- The red text at the bottom summarizes the result for this scenario: **WIP=1, CT=5h, TH=1/5=0.2 pz/h**.

1 item every 5 hours comes out of the line (TH = 1/5 pcs/h)

Each item stays on the line for 5 hours (CT = 5 h)

# Penny Fab manual simulation

### Visual Diagram: Penny Fab Manual Simulation (WIP = 2)
- **Component Type**: State-time diagram (Manual simulation).
- **Logic**: Shows the physical progression of two items (WIP = 2) moving simultaneously through the production line.

#### 1. Line Setup (Top)
- The 4 workstations and their processing times remain identical ($t_1=1h$, $t_2=2h$, $t_3=1h$, $t_4=1h$).
- The WIP is now set to **2**, meaning there are strictly two cylinders (jobs) allowed inside the factory at any given time.

#### 2. Time Evolution & The Bottleneck Effect (Subsequent rows)
- **t = 0h**: The simulation starts with two items in the system: one in WS1 and one in WS2.
- **t = 1h**: The item in WS1 finishes its 1-hour process. However, WS2 takes 2 hours, so it is still busy processing the first item. The diagram visually shows the second item waiting in a queue, represented by a cylinder resting on the arrow between WS1 and WS2. This is the first visual evidence of WS2 acting as a **bottleneck**.
- **t = 2h to t = 3h**: As the first item moves forward to WS3 and WS4, the second item enters WS2.
- **t = 4h to t = 5h**: We see the items sequentially exiting the line as finished products (represented by the cylinders outside the WS4 box on the right). 

#### 3. Results and Metrics (Text on the right and bottom)
- **Cycle Time (CT)**: Despite the momentary wait in front of the bottleneck at `t=1h`, the text explicitly notes that "Each item stays on the line for 5 hours". The Cycle Time remains at its minimum theoretical value ($T_0$): **5 hours**.
- **Throughput (TH)**: Because there are more items in the system, the output rate increases. The text states "2 item every 5 hours comes out of the line". Therefore, the Throughput is $\frac{2}{5} = \mathbf{0.4\text{ pcs/h}}$.
- The red text at the bottom summarizes the result: **WIP=2, CT=5h, TH=2/5=0.4 pz/h**.

2 item every 5 hours comes out of the line (TH = 2/5 pcs/h)

Each item stays on the line for 5 hours (CT = 5 h)

# Penny Fab manual simulation

### Visual Diagram: Penny Fab Manual Simulation (WIP = 3)
- **Component Type**: State-time diagram (Manual simulation).
- **Logic**: Shows the physical progression of three items (WIP = 3) moving simultaneously through the production line.

#### 1. Line Setup (Top)
- The 4 workstations and their processing times remain identical ($t_1=1h$, $t_2=2h$, $t_3=1h$, $t_4=1h$).
- The WIP is now set to **3**, meaning there are strictly three cylinders (jobs) allowed inside the factory at any given time.

#### 2. Time Evolution & Queueing (Subsequent rows)
- **t = 0h**: The simulation starts with three items distributed in the system: one in WS1, one in WS2, and one in WS3. To help track individual jobs, some cylinders are colored (e.g., a yellow one in WS3).
- **t = 1h**: The item in WS1 finishes and moves forward, but WS2 is still occupied. We see a queue forming, represented by a cylinder resting on the arrow between WS1 and WS2. Meanwhile, the yellow item moves from WS3 to WS4.
- **t = 2h**: The yellow item exits the line as a finished product. To maintain the constant WIP of 3, a new item immediately enters WS1. 
- **t = 3h to t = 6h**: The simulation continues, introducing new colored cylinders (like an olive-green one at $t=4h$ and another yellow one at $t=6h$) to track the continuous flow. The diagram shows that an item regularly ends up waiting in the queue before WS2 because of its longer 2-hour processing time.

#### 3. Results and Metrics (Text on the right and bottom)
- **Cycle Time (CT)**: Because items now have to wait in the queue before the bottleneck, their total time in the system increases. The text explicitly states "Each item stays on the line for 6 hours". Therefore, the Cycle Time is now **6 hours**.
- **Throughput (TH)**: The output rate has reached its maximum capacity. The text notes "3 item every 6 hours comes out of the line". Therefore, the Throughput is $\frac{3}{6} = \mathbf{0.5\text{ pcs/h}}$.
- The red text at the bottom summarizes the result: **WIP=3, CT=6h, TH=3/6=0.5 pz/h**.

3 item every 6 hours comes out of the line (TH = 3/6 pcs/h)

Each item stays on the line for 6 hours (CT = 6 h)

# Penny Fab manual simulation

### Visual Diagram: Penny Fab Performance Summary Table
- **Component Type**: Data table.
- **Logic**: Summarizes the system performance metrics (Throughput, Cycle Time, and x-factor) across varying levels of Work-In-Process (WIP), based on the manual simulation.

#### 1. Column Structure
- **WIP**: The constant number of jobs in the system, evaluated from 1 up to 10.
- **Throughput**: The output rate of the factory (jobs per hour).
- **Cycle Time**: The total time a job spends in the factory from entry to exit (hours).
- **x-factor**: A ratio representing how much longer the actual Cycle Time is compared to the theoretical minimum raw process time ($CT / T_0$). 

#### 2. Data Trends & Factory Physics Laws (Direct Observations)
- **WIP 1 to 2 (Uncongested State)**: The Cycle Time remains completely flat at its minimum theoretical value ($T_0 = 5$ hours), resulting in a perfect x-factor of 1.0. During this phase, Throughput increases linearly as more WIP is added (from 0.2 to 0.4).
- **WIP 3 (Capacity Reached)**: Throughput hits its maximum ceiling of **0.5** jobs/hour (the bottleneck rate). Because jobs now begin queueing in front of the bottleneck, the Cycle Time increases to 6 hours, and the x-factor rises to 1.2.
- **WIP 4 to 10 (Congestion State)**: For every additional unit of WIP added to the system beyond this point, the Throughput remains completely stagnant at **0.5**. However, the Cycle Time inflates significantly and linearly (growing from 8 up to 20 hours). At WIP 10, the x-factor reaches 4.0, meaning jobs take 4 times longer to complete than physically necessary, entirely due to waiting in queues.

# Penny Fab manual simulation

### Visual Diagram: Cycle Time vs. Constant WIP Level
- **Component Type**: Line graph.
- **Logic**: Illustrates the relationship between the constant number of jobs in a system (WIP) and the resulting cycle time.

#### 1. Axes
- **Y-axis**: Labeled "Cycle Time", with numerical tick marks at 0, 5, 10, 15, and 20.
- **X-axis**: Labeled "Constant WIP Level", with numerical tick marks at 0, 2, 4, 6, 8, and 10.

#### 2. Visual Curve
- **Horizontal Segment**: The graph begins with a perfectly flat, horizontal line fixed at a Cycle Time of 5. This flat segment spans from a WIP level of 0 up to a WIP level of 2.
- **Linear Increase**: Starting exactly at a WIP level of 2, the trajectory changes. The line begins to angle upwards, following a steady, constant positive slope until it reaches the final marked point on the graph at WIP = 10 and Cycle Time = 20.

### Visual Diagram: Throughput vs. Constant WIP Level
- **Component Type**: Line graph.
- **Logic**: Illustrates the relationship between the constant number of jobs in a system (WIP) and the resulting system throughput.

#### 1. Axes
- **Y-axis**: Labeled "Throughput", with numerical tick marks at 0, 0.2, 0.4, and 0.6.
- **X-axis**: Labeled "Constant WIP Level", with numerical tick marks at 0, 2, 4, 6, 8, and 10.

#### 2. Visual Curve
- **Initial Increase**: The graph begins at a WIP level of 1 with a corresponding throughput of 0.2. The line slopes upwards, passing through a throughput of 0.4 at a WIP of 2, and continues to rise until it hits a WIP level of 3.
- **Horizontal Asymptote (Capacity Limit)**: Starting exactly at a WIP level of 3, the graph hits a ceiling at a throughput value of 0.5. From this point forward (from WIP 3 all the way to 10), the line becomes perfectly flat and horizontal, indicating that adding more WIP to the system yields zero additional throughput.

> The WiP level in the factory can be reduced to 3 jobs while maintaining the factory throughput rate of /2   
The cycle time reduces to 2xWiP= 6 hours with an x-factor of 1.2   
V Thus at no expense, the factory can maintain its current throughput rate and reduce its cycle time from 20 to 6 hours

# Conclusion

$$
\mathrm{CT}_{\mathrm{best}}(w) = \begin{cases} 
T_0 & \text{if } w \leq W_0 \\ 
w / r_b & \text{otherwise} 
\end{cases}
$$

$$
\mathrm{TH}_{\mathrm{best}}(w) = \begin{cases} 
w / T_0 & \text{if } w \leq W_0 \\ 
r_b & \text{otherwise} 
\end{cases}
$$

> CT remains constant at the minimum CT (To) as WIP increases and it increases to infinity once the maximum WIP (rb) is reached   
TH increases as WIP level increases, until the WIP level reaches the maximum WIP (rb); after that TH stabilizes,remaining constant   
The best case (min CT and max TH) is when with WIP = 3

# Line critical parameters

1. Bottleneck Rate (rb): TH of the workstation which is the bottleneck of a line (maximum TH obtained from the line)   
2. Raw process time (To): sum of the long-term average process times of each station in the line (minimum possible CT)   
3. Critical WIP (Wo= rb To): WIP level which allows a line to achieve the maximum TH (rb) with the minimum cycle time (To)

# Example: balanced production line

> Line composed of 4 machines in series   
? Each machine has a 2 hours per piece process time   
Capacity of each machine (inverse of process time) = 1 pcs/2h   
> Once an operation on a machine is completed, the product goes immediately to the next machine   
Machines work continuously, with no stops   
No discarded pieces

# Example: balanced production line

# Critical parameters:

rb = 1 pcs/2h = 0.5 pcs/g   
(max utilization 三 min capacity)  
To= 2h*4 = 8h   
(sum of process times on machines)   
W = rb*To= 0.5*8 = 4 pcs

Wo is the critical value of WIP, which allows to reach rb = 0.5 pcs/h and To= 8 h

# Example: not balanced production line

1 Line composed of workstations in series   
Each WS is composed of a different number of machines   
> Each WS is composed of identical machines (with the same process time) in parallel   
WS capacity = single machine capacity * number of machines

# Example: not balanced production line

Line composed of work stations in series   
Each WS is composed of a different number of machines   
V Each WS is composed of identical machines (with the same process time) in parallel   
> WS capacity = single machine capacity * number of machines

### Visual Diagram: Work Station Capacity Calculation
- **Component Type**: Data table.
- **Logic**: Demonstrates step-by-step how to calculate the overall throughput capacity of a workstation that contains multiple identical machines in parallel.

#### 1. Column Structure & Variables
*   **Work Station**: Identifies the specific processing stage ($i = 1, 2, 3, 4$).
*   **Machines ($m$)**: The number of parallel, identical machines operating at that station.
*   **Process time ($t$)**: The time it takes one single machine to process one part (hours).
*   **Machine capacity**: Calculated as the inverse of the process time ($\frac{1}{t}$). This gives the output rate of a *single* machine in pieces per hour.
*   **WS capacity**: The total capacity of the entire workstation, calculated by multiplying the single machine capacity by the number of machines ($m \times \frac{1}{t}$).

#### 2. Data Breakdown
*   **WS 1**: 1 machine taking 2 hours. Capacity = $1 \times \left(\frac{1}{2}\right) = \mathbf{0.5 \text{ pcs/h}}$.
*   **WS 2**: 2 machines taking 5 hours each. Single machine capacity is 0.2. Total WS Capacity = $2 \times 0.2 = \mathbf{0.4 \text{ pcs/h}}$.
*   **WS 3**: 6 machines taking 10 hours each. Single machine capacity is 0.1. Total WS Capacity = $6 \times 0.1 = \mathbf{0.6 \text{ pcs/h}}$.
*   **WS 4**: 2 machines taking 3 hours each. Single machine capacity is 0.33. Total WS Capacity = $2 \times 0.33 = \mathbf{0.67 \text{ pcs/h}}$.

# Example: not balanced production line

# Critical parameters:

> rb = 0.4 pcs/h (WS2 capacity: not WS3 with slower machines and not WS1 with smaller number of machines)   
To = 20 h (sum of process times)   
> Wo= 0.4*20 = 8 pcs (it is smaller than the number of machines, because some station won’t be completely used)

# HAL - Large Panel Line Processes

# Data:

Average process rate (number of panels/h)   
Average process time (h) at each station

### Visual Diagram: Factory Process Routing and Capacity Table
- **Component Type**: Production data table.
- **Logic**: Details the sequential processing steps, their individual capacities, and processing times to determine the overall system constraints.

#### 1. Columns & Data Structure
*   **Process**: Lists the 12 sequential workstations the job must pass through, from "Lamination" to "EOL Test" (End of Line Test). 
*   **Rate (p/hr)**: The individual capacity of that specific process, measured in parts per hour. 
*   **Time (hr)**: The raw processing time a single part spends at that specific station.

#### 2. Factory Physics Parameters (The Bottom Row)
The bottom row explicitly extracts the two most critical parameters for this factory, following standard Factory Physics definitions:
*   **Bottleneck Rate ($r_b$)**: The rate of the workstation with the lowest overall capacity. By scanning the "Rate" column, the lowest value is **114.0 p/hr**, which occurs at the "Internal Circuitize" process. This station dictates the maximum possible throughput for the entire line.
*   **Raw Process Time ($T_0$)**: The absolute minimum time it takes to produce one part if it never waits in a single queue. This is calculated by summing the "Time" column. The table lists **33.9 hours** as the total $T_0$ *(Note: if you manually sum the column exactly as written, it equals 34.0, which suggests the textbook table might have a minor rounding artifact in its display, but the concept remains exactly the same!)*.

Batches and parallel machines are present, so rate is different from 1/time

# HAL - Large Panel Line Processes

Large Panel Line: produces printed circuit boards   
Line runs 24 hr/day (only 19.5 hrs of productive time)   
Recent Performance (last 7 months):

>TH = 1,400 panels per day (71.8 panels/hr)   
WIP = 47,600 panels   
>CT = 34 days (663 hr at 19.5 hr/day)   
>Customer service= 75% on-time delivery

How HAL is performing?

Which data we need to evaluate?

# HAL - Large Panel Line Processes

Critical WIP: rbT。= 144 x 33.9 = 3,869   
Actual Values:

>CT= 34 days = 663 hours (at 19.5 hr/day)   
>WIP = 47,600 panels   
>TH = 71.8 panels/hour

Conclusions:

>TH is 63% of capacity   
>WIP is 12.3 times critical WIP   
>CT is 24.1 times raw process time

The factory is not performing well!

# Exercise 1

Consider a production line composed of four workstations,each consisting of a single machine,except the second station which consists of two identical machines in parallel

Each machine has mean process time equal to two hours per job

a) Determine the botleneck rate rb, the raw process time T。and the critical WIP of the line   
b) Compute CT and TH for values of WIP going from 1 to 10

# Solution

### Visual Diagram: Best-Case Performance Exercise Solution
- **Component Type**: Integrated production model and performance dataset.
- **Logic**: Models a 4-station serial line with a parallel workstation to demonstrate Best-Case Law relationships between WIP, Throughput, and Cycle Time.

#### 1. System Layout & Data
*   **Process Flow**: Illustrates a serial manufacturing line where jobs move from WS 1 through WS 4.
*   **Station Configuration**: WS 2 features two machines in parallel ($m=2$), while all other stations (1, 3, and 4) consist of a single machine ($m=1$).
*   **Workstation Data Table**: Lists a constant process time of 2 hours per machine and the resulting station capacity ($m/t$) for each stage.

#### 2. Fundamental System Parameters
The "Parameters" section calculates the theoretical limits based on the line configuration:
*   **Bottleneck Rate ($r_b$)**: Identified as **0.5 jobs/h**, which is the minimum capacity among all workstations (WS 1, 3, and 4).
*   **Raw Process Time ($T_0$)**: The absolute minimum time needed for a job to cross the line without queuing, equaling **8 hours** (the sum of individual process times).
*   **Critical WIP ($W_0$)**: Calculated as **4 jobs** ($r_b \times T_0$), representing the minimum inventory level to achieve maximum throughput with minimum cycle time.

#### 3. Performance Dataset (WIP 1 to 10)
The table displays the numerical results of the simulation as the inventory level increases:
*   **Cycle Time ($CT$)**: Remains fixed at 8 hours for $WIP \le 4$, then increases linearly up to 20 hours at WIP 10.
*   **Throughput ($TH$)**: Increases linearly from 0.13 to 0.50 jobs/h as WIP reaches the critical point ($WIP = 4$). For all $WIP > 4$, throughput remains saturated at the bottleneck rate of 0.50 jobs/h.

# Exercise 2

Consider a production line composed by three workstations in series.The characteristics of the workstations are reported in the table.

Compute the botleneck rate rb, the raw process time T。 and the critical WIP W。 of the system.

What happen to the TH and CT values when the WIP exceeds Wo?

### Visual Diagram: Workstation Data Table
- **Component Type**: Production data table.
- **Logic**: Outlines the processing characteristics for three sequential workstations, providing mean process times and the number of available machines for each.

#### 1. Columns & Data Structure
*   **Workstation i**: Numerical identifier for the workstations (1, 2, and 3).
*   **E[Tsi] (min)**: The expected mean process time ($E[T_{si}]$) for a single job at the workstation, measured in minutes.
*   **Machines**: The total number of parallel, identical machines located at the workstation.

#### 2. Table Data Breakdown
*   **Workstation 1**: Lists a mean process time ($E[T_{s1}]$) of **3 minutes** and utilizes **2 machines**.
*   **Workstation 2**: Lists a mean process time ($E[T_{s2}]$) of **2 minutes** and utilizes **1 machine**.
*   **Workstation 3**: Lists a mean process time ($E[T_{s3}]$) of **4 minutes** and utilizes **3 machines**.

# Solution

### Visual Diagram: Production Line Parameter Calculation Solution
- **Component Type**: Performance data table and parameter summary.
- **Logic**: Displays the calculated workstation production rates used to determine the fundamental limits ($T_0$, $r_b$, $W_0$) of a 3-station production system.

#### 1. Columns & Data Structure
*   **Workstation i**: Numerical identifier for the three sequential workstations in the system.
*   **E[Tsi] (min)**: The expected mean process time per job at each station (3, 2, and 4 minutes respectively).
*   **Machines**: The count of parallel machines at each station.
*   **Production rate (min^-1)**: The calculated capacity ($m / E[T_s]$) for each workstation:
    *   Workstation 1: **0.666666667**
    *   Workstation 2: **0.5**
    *   Workstation 3: **0.75**

#### 2. Fundamental System Parameters
The values calculated below the table represent the theoretical performance boundaries:
*   **Raw Process Time ($T_0$)**: The sum of process times across all stations, listed as **9 min**.
*   **Bottleneck Rate ($r_b$)**: The minimum production rate in the system, identified as **0.5 j/min** (dictated by Workstation 2).
*   **Critical WIP ($W_0$)**: The minimum Work-In-Process level required to achieve the bottleneck rate with the minimum cycle time, calculated as **4.5 j**.

# Solution

$$
\mathrm{CT}_{\mathrm{best}}(w) = \begin{cases} 
T_0 & \text{if } w \leq W_0 \\ 
w / r_b & \text{otherwise} 
\end{cases}
$$

$$
\mathrm{TH}_{\mathrm{best}}(w) = \begin{cases} 
w / T_0 & \text{if } w \leq W_0 \\ 
r_b & \text{otherwise} 
\end{cases}
$$

If the WIP exceeds WO, the TH remains constant at value of 0.5 j/min and the CT increases at a rate of WIP/0.5
