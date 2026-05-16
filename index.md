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

# 2.1 Introduction to Production System Modeling  
## Little’s Law and Exercises

## 2.1.1 Course Context and Objectives
This section introduces the **analysis and modeling of production systems**.  
It corresponds to **Chapter 2** of the reference textbook and defines the analytical framework used throughout the course.

The adopted approach is **analytical and hierarchical**:
- start from simple systems,
- derive fundamental relationships between KPIs,
- progressively extend the models to more complex systems.

---

# 2.1.2 Modeling Approach

The course follows a **bottom-up strategy**:
1. Single workstation (single machine)
2. Production line (series of workstations)
3. Networks with merging and splitting flows
4. Multiple product types
5. Batch arrivals

Each model is an **approximation** of reality:
- not all real-world elements are modeled,
- operators, transport systems, and detailed behaviors may be abstracted,
- assumptions must be justified by the analysis objectives.

---

# 2.1.3 System Boundaries

The analysis focuses on the **factory system only**:
- jobs arrive at the factory with given parameters,
- jobs follow a routing inside the factory,
- completed jobs exit the system (delivery or storage not analyzed further).

---

# 2.1.4 Basic Definitions

## Jobs
The terms *job*, *item*, and *order* are used interchangeably to indicate a physical entity entering the production system.

## Factory
A factory is composed of multiple **workstations**.

## Workstation
A workstation is a set of **identical machines or operators**:
- same processing parameters,
- parallel operation,
- identical processing time distributions.

## Queue
A physical or logical place where jobs wait when machines are busy.

## Routing
The ordered sequence of workstations visited by a job.

Different product types may follow **different routings** within the same factory.

---

# 2.1.5 Arrival Process

Jobs may arrive:
- individually,
- in batches.

Arrival is characterized by:
- average arrival rate,
- average inter-arrival time,
- probability distribution (often exponential).

These are **input parameters** of the model.

---

# 2.1.6 Processing Times

Processing times:
- are not deterministic,
- follow probability distributions,
- are characterized by mean value and variability.

---

# 2.1.7 Key Performance Indicators (KPIs)

## Cycle Time (CT)
The **cycle time** is the time a job spends inside the system.

Terminology note:
- in Value Stream Mapping this quantity is often called *lead time*,
- in queueing theory and analytical models it is called *cycle time*.

Two notions:
- real cycle time: directly measured in the plant,
- planned cycle time: conservative estimate used for planning and scheduling.

### System vs Workstation Cycle Time
- CTᵢ: cycle time at workstation *i*
- CTₛ: total cycle time of the system

At workstation level:
```
CTᵢ = CTQᵢ + E[TSᵢ]
```

---

## Work In Process (WIP)
WIP is the **average number of jobs inside the system**:
- jobs being processed,
- jobs waiting in queues.

---

## Throughput (TH)
Throughput is the **rate of completed jobs** leaving the system:
- jobs per hour,
- jobs per day.

In steady state:
```
TH = arrival rate
```

---

# 2.1.8 Steady-State Assumption

Performance measures are evaluated in **steady state**:
- after initial transient effects disappear,
- independent of initial system conditions.

Instantaneous values fluctuate due to variability,  
but **average values converge** to steady-state limits.

---

# 2.1.9 Arrival and Departure Functions

Define for job *i*:
- arrival time: aᵢ
- departure time: dᵢ

Define:
- A(t): cumulative arrival function
- D(t): cumulative departure function

The number of jobs in the system at time *t* is:
```
N(t) = A(t) − D(t)
```

---

# 2.1.10 Average Cycle Time

For a time interval [a, b]:

```
CT = (1 / Nₐᵦ) · Σ (dᵢ − aᵢ)
```

---

# 2.1.11 Average WIP

Average WIP over [a, b]:

```
WIP = (1 / (b − a)) · ∫ N(t) dt
```

---

# 2.1.12 Little’s Law

```
WIP = TH · CT
```

Equivalent form:
```
WIP = λ · CT
```

---

# 2.1.13 Exercise 1

**Given:**
- WIP = 25 jobs  
- λ = 4 jobs/hour  
- E[TS] = 14.5 minutes  

**Solution:**
- CT = 25 / 4 = 6.25 hours  
- E[TS] = 0.24 hours  
- CTQ = 6.01 hours  

---

# 2.1.14 Exercise 2

**Given:**
- λ = 10 jobs/day = 0.417 jobs/hour  
- CT₁ = 4.2 hours  
- CT₂ = 5.3 hours  

**Solution:**
- WIP = λ · (CT₁ + CT₂) = 3.96 jobs  

---

# 2.1.15 Key Takeaways
- Steady-state averages are central.
- Little’s Law links WIP, CT, and TH.
- Valid at all system levels.

# 2.2 Penny Fab Model  
## Single Workstation and Factory-Level Analysis

## 2.2.1 Purpose of the Model
The **Penny Fab Model** is a didactic example used to introduce:
- analytical modeling of production systems,
- performance evaluation using **Little’s Law**,
- the impact of variability and system boundaries.

---

# 2.2.2 Modeling Philosophy
The analytical approach:
- decomposes the factory into simple components,
- models each component separately,
- recomposes the system to analyze global behavior.

This is an approximation of reality and abstracts from operators and transport systems.

---

# 2.2.3 System Boundaries
The analysis focuses only on the factory:
- jobs arrive with known parameters,
- jobs follow a routing,
- completed jobs exit the system.

---

# 2.2.4 Core Definitions

## Workstation
A workstation is a set of identical machines or operators working in parallel.

## Queue
Jobs wait in a queue when machines are busy.

## Routing
The ordered sequence of workstations visited by a job.

---

# 2.2.5 Arrival Process
Jobs may arrive individually or in batches.
Arrival is characterized by the arrival rate λ and its distribution.

---

# 2.2.6 Processing Times
Processing times are random variables with known mean and variability.

---

# 2.2.7 Performance Measures

### Cycle Time (CT)
```
CT = CTQ + E[TS]
```

### Work In Process (WIP)
Average number of jobs inside the system.

### Throughput (TH)
Completed jobs per unit of time.
In steady state:
```
TH = λ
```

---

# 2.2.8 Little’s Law
```
WIP = TH · CT
```

---

# 2.2.9 Key Insights
- Variability generates waiting.
- Waiting dominates cycle time.
- Little’s Law links all KPIs.

---

# 2.2.10 Key Takeaway
The Penny Fab Model shows how simplified analytical models provide deep insight into production system behavior.

# 2.3 Critical Parameters of Production Lines

## 2.3.1 Introduction
This section introduces the **critical parameters** used to analyze the performance of production lines.
These parameters allow us to:
- determine the **best achievable performance** of a system,
- compare optimal conditions with actual factory behavior,
- identify inefficiencies and improvement potential.

The analysis builds on the relationships between **WIP, throughput, and cycle time**.

---

# 2.3.2 Definition of Critical Parameters

Three critical parameters characterize a production line:

## Bottleneck Rate (Rᵦ)
- Defined as the **throughput of the bottleneck workstation**.
- The bottleneck is the workstation with the **lowest capacity**.
- Rᵦ represents the **maximum achievable throughput** of the line.

---

## Raw Process Time (T₀)
- Defined as the **sum of the average processing times** of all workstations.
- Represents the **minimum possible cycle time**.
- No job can exit the system faster than T₀.

---

## Critical WIP (W₀)
- Defined as:
```
W₀ = Rᵦ · T₀
```
- Represents the minimum WIP level required to achieve:
  - maximum throughput,
  - minimum cycle time.

---

# 2.3.3 Example 1 – Balanced Production Line

### System Description
- 4 machines in series
- Each machine has:
  - processing time = 2 hours
  - capacity = 1 / 2 = 0.5 jobs/hour
- No failures, no scrap, immediate transfer

### Critical Parameters
- Bottleneck rate:
```
Rᵦ = 0.5 jobs/hour
```
- Raw process time:
```
T₀ = 2 + 2 + 2 + 2 = 8 hours
```
- Critical WIP:
```
W₀ = 0.5 · 8 = 4 jobs
```

This is a **balanced line**, since all machines have the same capacity.

---

# 2.3.4 Example 2 – Unbalanced Line with Parallel Machines

### System Description
Four workstations in series:
- WS1: 1 machine, 2 h
- WS2: 2 machines, 5 h
- WS3: 6 machines, 10 h
- WS4: 2 machines, 3 h

### Workstation Capacities
Capacity of each workstation is the **sum of machine capacities**:
- WS1: 0.5 jobs/h
- WS2: 0.4 jobs/h
- WS3: 0.6 jobs/h
- WS4: 0.67 jobs/h

### Critical Parameters
- Bottleneck: WS2
```
Rᵦ = 0.4 jobs/hour
```
- Raw process time:
```
T₀ = 2 + 5 + 10 + 3 = 20 hours
```
- Critical WIP:
```
W₀ = 0.4 · 20 = 8 jobs
```

---

# 2.3.5 Industrial Example – Performance Comparison

Given:
- Bottleneck rate: 114 parts/hour
- Raw process time: 33.9 hours
- Critical WIP:
```
W₀ ≈ 3869 units
```

Actual performance:
- Throughput: 71.8 parts/hour
- WIP: 47,600 units
- Cycle time: 663 hours

### Interpretation
- Throughput ≈ 63% of maximum
- WIP ≈ 12 × critical WIP
- Cycle time ≈ 24 × raw process time

The system performs **far from optimal conditions**.

---

# 2.3.6 Relationship Between WIP, CT, and TH

Let:
- W = WIP level

Then:

### Cycle Time
```
CT(W) = T₀            if W ≤ W₀
CT(W) = W / Rᵦ        if W > W₀
```

### Throughput
```
TH(W) = W / T₀        if W ≤ W₀
TH(W) = Rᵦ            if W > W₀
```

---

# 2.3.7 Interpretation of the Curves

- For W ≤ W₀:
  - Throughput increases linearly
  - Cycle time remains minimal

- For W > W₀:
  - Throughput saturates at Rᵦ
  - Cycle time increases linearly with W

This region corresponds to **congestion**.

---

# 2.3.8 Exam-Style Exercise (Solved)

### Given
Three workstations in series with processing times:
- 3 min
- 2 min
- 4 min

### Solution
- Capacities:
  - WS1: 0.33 jobs/min
  - WS2: 0.5 jobs/min
  - WS3: 0.25 jobs/min
- Bottleneck:
```
Rᵦ = 0.25 jobs/min
```
- Raw process time:
```
T₀ = 3 + 2 + 4 = 9 min
```
- Critical WIP:
```
W₀ = 0.25 · 9 = 4.5 jobs
```

### Behavior for W > W₀
- Throughput remains constant at Rᵦ
- Cycle time increases as W / Rᵦ

---

# 2.3.9 Key Takeaways
- Critical parameters define **optimal system performance**.
- Bottleneck determines maximum throughput.
- Excess WIP increases cycle time without increasing throughput.
- Comparing actual vs critical values reveals inefficiencies.

Topic about the analysis and and the modeling of production systems. That is the introduction to factory models. So today, we we see some basic concepts and notations and definition that then will be used in the next lessons also. This this part corresponds to the second chapter of the book that I listed in the material of the course, so the modeling and analysis of production systems. And so here, it's it's described the approach that we will follow during the course.
So it's an analytical approach for the modeling and analysis of the system, and we start by first reanalyzing the simple models. So we start with the single machine models, and then and by using these models, we define the basic relationships between the the KPIs. And then more complex models are developed. Okay? So we start with the first word, the single workstation analysis, then we add the complexity, and we analyze an entire line.
And then we add more complexity. We add several different networks. So workstations placed not only in series, also with merging and splitting of the flows of the product inside the network. Then we will see, the multiple product problem. So if, we have in the same plant, in the same network, different types of products that follow different routings, and we see how to model it.
And finally, the batches. So we consider that items or jobs arrive at the network not one by one, but in batches. And, again, we see how the formula changes. So the approach is to decompose the system into small components and then to model each component separately and then reintegrate the general system by combining all the sub models. Then let's also keep in mind that this approach is an approximation of the the real system.
And in general, so each analytical model, also simulation model, is an approximation of the real world environment. So we need to be sure that the model that we develop is enough to analyze in the proper way the real system. So we see that in the models that we develop, yes, we add some complexity, but not all the complexity that we have in a real system, in a real plant. For instance, we we don't model the operators or the transport systems. But so we need to be sure that these assumptions are are fine in order to analyze the system.
Then let's now fix the boundary of our analysis. So our model is represented in this picture. Consider only the factory. And so in our models, we don't analyze how the orders are formed, so where and why the orders arrive, neither what happened to the completed jobs. So how they are delivered to the customer or stored somewhere.
So our analysis is related only to the factory, And we know that the jobs arrive at the factory at with the specific parameters, so with specific interarrival times. And after they are they they follow the routing inside the factory, they exit the system, and we don't care where they where they go. Then the so at the beginning, we say that the order arrives at the factory. Here, the order sometimes I use the word order, other times the word jobs, otherwise, the the the word items. Okay?
So it means the the arrival of a physical entity of an order that start then the following production. Production. And here are the other definitions or the the the building blocks of our framework. So when we talk about factory, we mean a place composed by several machines, and the machines are grouped together by type in workstation. So a workstation is a set of machines of the same type with the same parameters that perform the same operation.
Then we have the processing steps. So we know the ordered list of workstation, so operations that a job needs from the beginning to the end. And then we have the movement of jobs through the factory. And so the job arrives at the beginning, then we know the list of workstations that it has to visit. And so the job the job moves from one workstation to another, and it waits in the queue before that is placed.
So it's a physical place where the jobs can accumulate before being processed by the machines if the machines are are busy working the previous jobs. About the arrival, we know that the jobs arrive at the factory individually, so one by one or in batches of a specific dimension. And we know these are called the input parameters. So we know if the jobs arrive one by one or in batches and which is the average inter arrival time or arrival rate. And usually, we know not only the average time, but also the distribution.
So we know that the items arrive following an exponential distribution of average value ten minutes, for instance. So these are the input parameters that we know in advance. Here, you have the representation of a workstation. So a workstation is a collection of one or more identical machines or or operators if the the the activity is done manually by the operators. K?
The important thing is that the machines are identical. So they work in parallel, and they are identical in the sense that they have the same processing parameters. So all the machine or the machines process the item with the same processing time. Also, for the processing times, we know the the average value and usually the distribution. So the the time the processing times following follow a distribution with a specific mean and standard deviation.
Then here, we have the definition of routing. So we call the processing step in the previous slide. This is an synonymous. So the routing is the sequence of the processing steps for a job. And here in the picture, you have so an example of a plant where you have several workstations.
And before each workstation, there is the corresponding queue or inventories. And you have represented several routing. So different product types can follow different routings inside the same plant. So they visit different workstations, maybe in different order. Then let's decide define also the performance measures.
We have already defined them. So we we already talked about the cycle time, the WIP, and the throughput, but let's just recall the definitions. So the cycle time is the the time that a job spends inside a system. So it's denoted as a city, the acronym of a cycle time. And here, pay attention to this distinction about the terminology Because if you remember in the value stream mapping, we called this quantity, so the time and the job spends in the system as lead time.
Instead, in the Q theory, so from now on, we call this quantity cycle time instead of lead time. So the difference here is that the term lead time is used more to represent an a priori evaluation of the cycle time. Instead, the cycle time is something that is directly measured from the plant. So if you have the possibility of going to the plant and measure the the the exact times an item remains in the system, well, you are measuring the cycle time. But then for other purposes, for instance, the planning of activities or the scheduling of jobs on the machine, it's better maybe not to use the the real value of the cycle time, so the effective processing time, but it's estimation.
Maybe you consider a longer time in order to produce a a schedule that is more effective. Effective. So in case you have some delays or failures of the machines and so on. Okay? So only so remember that this quantity sometimes is called the time, for instance, in the value stream map terminology.
But from now on, we call it cycle time. Then we have the working process. The working process is defined as the number of jobs inside the system from so the beginning to the end of the sequence, and it's denoted by the whip acronym. So the whip represent the number of items that are inside the system that can be or inside the machines so that they are processing they are being processed or waiting in the inventories, so in the queues before the machines. And finally, we have the throughput rate.
The throughput rate is the number of completed jobs leaving system per unit of time. The throughput is indicated by its acronym t h. So remember that the throughput is a rate, so it's a number of jobs completed per time unit. Then another distinction about the notation, this is taken again, so from the book, from our reference book. They so the book did a difference between the cycle time of the of the entire factory, of an entire system that is called CTS, where that s stands for system, so cycle time of the system, and the cycle time of each workstation that is indicated as a cycle time CT of I, where I is the index of the workstation.
So we have three workstations in our system. So we can define the cycle time of the first, so CT one, the cycle time of the second, and the third. And then we define we define also the total cycle time, so CTS. This is a distinction useful if you read and study the book. Instead here in the slides, usually, it's so we we understand if we are talking about the cycle time of an entire system of a workstation.
So sometime I I don't insert this s or I in the notation. Then, again, about the cycle time, this is the first formula that we see, and this is a formula that you have to memorize. So the fact that the cycle time of a workstation is given by the sum of two terms. That is the cycle time in queue. So CTQ means the waiting time in the queue before the the machine plus the processing time.
The processing time is indicated as e of t s of I, where e the letter e stands for expected value. So e of t s of I means the average processing time. Since as we will see in the next lesson, here in order to apply the Q theory, we assume that the times are not deterministic, but they have a variability. So they follow probability distributions. So the cycle time is given by the sum of these two terms.
And this is why it's particularly difficult to compute it because the processing time so the the average value of the processing time is easy to measure. You you go in the plant, and you know that the machine uses this time to process the item even if you have a variability. Instead, the problem is to estimate the waiting time. So the waiting time is the term that we want to estimate. So for which we wanted to derive the formulas to compute it.
Then Okay. Here, it's about the throughput. It's it's just written in this short phrase, but it's an important relationship. So it says that the throughput rate in the long run long run, it means in the steady state condition. So after the system works for a lot of time, not to consider the the initial time where the system at the beginning is empty, and then the the the jobs start arriving, and then the system start working.
So there is at the beginning a time in which the performances are not accurate. So we need to wait until certain time has passed. So this is why we call the the long run values of this of the of our measures. So the throughput rate is equal to the input rate of jobs. So it means that the throughput of the system usually is equal to the arrival rate of jobs.
So because if we have 10 jobs per hour arriving at our job, then if all of them are processed and we don't have discharged items or other things, then we have also 10 jobs per hour leaving the system. So this this equation is valid for most of the systems. And let's go on. Okay. Here, another thing.
So talking about the the steady state system, let's say that we are interested in computing only the steady state values of cycle time and the WIP because the cycle time at a specific time or the WIP of the system as a specific in a specific time are very difficult to compute. So in each time instant, we can have different values of cycle time and WIP because we have the variability. So each job can can have a different cycle time from the other jobs. And thus, in each time instant, we have a different WIP. So different total number of jobs inside the system at each time.
But so now we are interested only in computing the steady state measures, and these measures are independent of the initial condition of the system. So they may different a lot from the beginning of the system. So when the system at the beginning is empty and they start the the processing and from the end. But if we, let's say, analyze the system for a long time, then the value of the performance measures reach their steady state values. So now let's go on, and let's see also by using a small example how to compute the performance measure of cycle time and WIP.
They can be computed by analyzing the arrival and departure of jobs to the system. So let's define for each job I, its arrival time, t a I, and its departure time, t d of I. And let's define two functions, a and d, that are the arrival function. So it's the total number of arrivals at each time and the departure function that is the total number of departure at each time instance. And let's represent them them on a graph.
Here, let me just change the screen because I prefer, as usual, to do these things step by step with you in order to better understand the reasoning. Okay? So let me just change the screen and take the the other board. Example, in which we have so let's write a table with some item arriving. Let's call item I, and we insert, for instance, one, two, three, four, five.
So we insert in the system five items, one at a time, and we represent them in the the graph. And in this graph, we have the time on the x axis. And here we have the number of jobs, cumulative number of jobs. Cumulative number of jobs. Here for each item, we define the time of arrival, t a of I, the departure time, t d of I, And then let's insert also the duration.
So the time the job remains inside the system, that is t d of I minus t a of I. So the first item, let's assume that it arrives at the system at time two and it exit the system at time six with a duration of four minutes or hour. Okay. Here, let's assume that we are using the same time unit and all of the times are expressed in this unit. Okay?
So we represent this item here. So we have a time two. We have the first arrival. So here we have one. So one item in the system at time two.
Then the second item, let's assume that it arrives at time three and it exit the system at time seven for a duration of four. Three, four, five, six, seven, eight. So the first one is from two to six. So this is the first item. The second one is from three to seven.
This part here represent our arrival function. Then item three, let's assume that it enters the system at time five and it exit at time eight for a duration of three. So at time five, we have the third item until time eight. Then the fourth item arrives at time six and exit at time nine, again, for a duration of three. So from six to nine.
And then the fifth arrives at time seven and leave at time eleven for a duration of four. From seven to eleven. Okay. So here, the arrival function is this one. So the arrival function is zero until two, then it's one until three, then it's two until five, then it it hits three until six and so on.
So this one here, and then it remains at five. This is a of t, so the arrival function at each time. Instead, here, we have the departure function. So the departure is zero until six. Then we have the departure is one.
So we have the first item that is leaving the system. Then it becomes two at time seven, then three here at time eight, then four at time nine, and then five here at time eleven. And this is the departure function, d of t. Okay? So this is an example of that graph that we have seen together in the slides.
Then let's also define the number of items that arrives at the system in this time interval, and we call this quantity n a b, where a b is the time interval. So let's say that two is a and 11 is b. This is the time intervals in which the system contains at least one item. So in these time intervals, we have number of items arriving at the system equal to five, and a b is equal to five. Okay.
Now let's compute the cycle time. Here we have five items, and for each of them, we know its cycle time. So for the first item, the cycle time, it is the time it remains in the system is here, this quantity here, this one, four. For the second, again, four, this one, then three, then again three, and then four. Okay?
So we compute the average value to have the average cycle time of the system. In formulas, the average cycle time, so can be written as, let's write here, cycle time a v, so in this time interval, as the sum of all the cycle times divided by the number of items. This is the formula to compute the average value. So we sum all the values and we divide it by the number of items. So we write the sum for I from one to n a b of t d I minus t a I divided by n a b.
This is the formula to compute the average cycle time. So here, if we sum all the values, four plus four plus three plus three plus plus four, obtain 18 divided by NAB. That is five. So the result is 3.6. So by using this formula, are able to compute the average cycle time in this system.
Then now if we look at this quantity, at this sum, These correspond to this area that I I have inserted here in the graph. So this is the area. Let's call this quantity area a b. There is another way of expressing this area by using the integral. So this area can be also computed by doing the integral between a and the d function.
K? So, basically, it's a sort of looking at the same picture, but vertically. So the area is this part here, this part here, this part, and so on. So the same area can be expressed as the integral between a and b of a of t minus d of t, the t in time. Then what is the quantity a of t minus d of t?
Okay. So what is the meaning of this number here, this area here? Well, if I do the arrival minus the departure, I have the number of items currently in the system. Let's do, for instance, another table in which we compute for each time. Let me change the page for a moment because I needed to do another table, then we come back here to go on with the formula.
So let me write another table with for each time, I report the arrival at each time, the departure at that time, and then the difference between the arrival and the departure. Here in our example, we have 11 time instance. So 1234567891011. So at time one, we don't have any arrival and any departure, so everything is zero. At time two, we have the first arrival and no departure.
So the difference is one. At time three, we have the second arrival and no departure. So here is two. At time four, we have no new arrivals, so arrival is always two. The departure is zero.
Then at time five, we have the third arrival, so this is three, and the zero departures. Then at time six, we have the new arrival, so arrival is four, and we have the first departure, so departure is one. And the difference is three. Then at time seven, we have the fifth arrival and the second departure. So the difference is three again.
At time eight, no new arrival. And the third departure, so the total the difference is two. Then the arrival remains five for the other time instances. And the departure, so at time nine, we have the fourth departure. At time ten, again, four.
And at time eleven, the fifth departure. So here, the difference are one, one, and zero. So this is the table of reporting for each time instance, the number of items inside the system. That is this difference. This is this is called also n of t.
So the number of items in the system. Okay. So what is the meaning now of so now let's compute so what is the meaning of this quantity? So this is the average number of items inside the system. K.
So by using this other concept, can express also the WIP. So WIP a b as the integrals that we have written before from a to b of a t, a of t minus d of t, the t divided by b minus a. That is the total time interval. For instance, if we compute it here in this example, we have the WIP a b as if we sum of the the the third column, so if we sum all these numbers, we obtain 18. So check it.
So we divide 18, that is the total number of items in the system at each time, divided by the time interval b minus a. So 11 minus two, so nine, and the result is two. So two is the average number of items that we have in the system at each time. Okay. So now let's see the final step that is so we have written the first formula, this one here.
So it's cycle time of a b equal to let's call this area that is the same quantity for both function only as a b. The cycle time is written as this area a b divided by n a b, the number of arriving items. Then from the second part here, we can write the WIP as AB, so the same area that is written as integral here, divided by b minus a. So since these two formulas share the same term a b, we can derive the term a b from the first one and then insert it into the second in order to find the relationship between the WIP and the cycle time. So from the first formula, we derive a b that is equal to cycle time a b multiplied n a b.
And then we use this formula. So this expression of a b in the second formula here, and we write whip AB is equal to so n a b multiplied cycle time divided by b minus a. K. So here we have derived the relationship between the WIP and the cycle time. So they are so the WIP is equal to the cycle time multiplied by this coefficient.
Now let's understand the meaning of the coefficient. This is the number of items arriving in the system divided by the time interval. So this quantity is nothing else than the throughput of the system. The throughput is the number of items per time unit. So if we divide the total number of items divided by the total time, we obtain exactly the throughput rate.
This is the throughput. That usually here in the book is also indicated as with the letter lambda. In this book, they indicate t h with the throughput and the lambda with the arrival rate. So lambda is the letter used to indicate the arrival rate of items to the system. And we know that in most of the systems, lambda is equal to the throughput.
So the throughput is equal to the arrival rate of our system. Okay. So here we have derived the most important law that regulate our system. That is the little slow. We put equal to throughput multiplied the cycle time.
K. Now let me see if everything is clear. Ring is presented here, but without the example. Okay? So here you have the definition of the arrival and the departure functions.
And then you have the for the definition of n a b, and then the formula to compute the cycle time by using the sum of the duration of each item. Then you have the definition of the area a b also as the integral between the two functions. And thus, the computation of the whip as the integral of the number of items in the system divided by the time interval. And then the final steps to merge the two formulas and obtain the final relationship between the the WIP and the cycle time. That is the little slow.
Here, it's expressed also in the form of use by using lambda instead of the throughput. Okay? And here, it's also written that this law is valid at each level. So it's valid at the level of a single workstation, a single machine, a single queue, so a single element of the system, but also at the entire system. So if you compute the total cycle time and the total WIP and the throughput, then the little slow is always valid.
Okay? So you can compute one of these three KPIs by using the other two. And this is what is is reported here with the definition of the little slow. Then here, it's okay. Another we have already said these things.
The the part about the the fact that the cycle time and the WIP are very variable during each time. Okay? So if you analyze the number of, for instance, the number of items in the system or the the cycle time for each item, you obtain a graph such as this one, so with with a lot of variability. But the important thing is that in the steady state, so after the system is running in the same condition for a very long time, then the average value reach a fixed value. Okay?
Okay. So the this term, the steady state implies that the mean reaches a limiting value and stop to change, but only the mean value stop to change, not to the original values because the variability instead continues forever. So we always have this fluctuation. Okay. Now I leave you a few times to do two exercises where you can apply so these first two formulas that we have seen today.
So the little slow and the fact that the cycle time is composed by two terms that are the cycle time in queue and the average processing time. So let's read the text of the first exercise. We have a workstation with a single machine for processing that has a long run average inventory level, so an average WIP of 25 jobs. The average rate at which jobs enter the workstation is four per hour, and the average processing time is fourteen point five minutes per job. You have to compute the average time that the job spends in the queue.
Okay? So just to use the the two formulas that we have seen and solve this exercise. I leave you a few minutes to solve it, and then we do the solution together. So let's report the input data. So the WIP is 25 jobs.
Then the arrival rate indicated as lambda is four jobs per hour. And the pro the average processing time that is indicated as EOTS is fourteen point five minutes. Then since we have the rate in hours, let's translate it into hours. So fourteen point five divided by sixty, zero point twenty four hours. And the question is, which is the cycle timing queue?
So first three, we use the little slow. So the little slow is equal to throughput multiplied the cycle time. Okay. So the cycle time is width divided by throughput. And in our case, the throughput is equal to lambda.
So the cycle time is the WIP 25 divided by lambda for jobs per hour. So a cycle time of six point twenty five hours. And then we use the other relationship that is cycle time is equal to cycle time in q plus the processing time EOTS. And from here, we derive the cycle time in q. It is a cycle time minus e of t s.
So six point twenty five minus zero point twenty four hours. A result of six point zero one hours. Okay? Then let's do also the second exercise consisting of two workstations. The arrivals to the first station occur at a rate of 10 per day.
The long run average time that a job spends at the first workstation is four point two hours. After processing at the first workstation, a job is sent directly to the second workstation where it spends an average of five point three hours. After processing at the second workstation, the job leaves the system. What is the average working process within the factory? Again, five minutes for you, and then we see the solution.
Exercise two. So here we have a two workstations. So we have Lambda, then workstation one, and then workstation two. And so the input data is lambda equal to 10. 10 jobs per day.
But in the text, is written that one day is equal to twenty four working hours. So we can translate the quantity into hours. So 10 divided by 24, that is 0.417 jobs per hour. And then we know the cycle time of the first workstation, so CT one, that is four point two hours. And the cycle time of the second workstation, that is five point three hours.
And here the question is, which is the WIP of the system? Okay. So here we can solve this exercise into two ways. The first one is to analyze separately the two workstations. So compute with one by using the little slow, so lambda multiplied cycle time one.
So 0.417 multiplied 4.2. It is 1.75 jobs. Then the second whip, whip two as lambda multiplied the cycle time two, zero point four one seven multiplied 5.3, and the result is 2.21 jobs. And that's the total WIP. So the WIP dot or WIP s is the sum whip one plus whip two, and the sum is 3.96 jobs.
The second way to solve the exercise is to firstly sum the cycle times to compute the total cycle time as CT one plus CT two. So 4.2 plus 5.3. It is nine point five hours. And then compute the total WIP. It is lambda multiplied the cycle time dot 0.417 multiplied 9.5.
The result is 3.96 as before jobs.

Okay. So let's go on. Okay. So now we have seen the basic relationships and the definition of the KPIs of the factory. Now let's now address this example.
So by analyzing a sort of real case, here we have the penny fab model that is the model related to a factory that is called the penny fab because it produces the pennies. And it's composed by four workstations as represented in the picture here in the slides. So this factory produces only one type of product, and we have four processing steps to be performed in sequence. And each operation is performed on a separate machine. So here, the machines process is only one unit of the product at a time.
And the processing times are considered to be constant, so deterministic values, and are one hour for the first workstation, two hours for the second, one hour for the third and the fourth workstations. Then another characteristic of this system is that it is a con whip system, so a constant whip system. So it's represented by this arrow that instead of going out, come back to the first workstation. It means that constant means that we wanted to maintain a fixed number of items inside a system. So for instance, five items.
So at the beginning, we have five items on the first workstation, then the first one is processed, then is moved to the second, then the third, and the fourth. And then when one item is completed and as it leaves the system, a new one can enters can enter. So this is a definition of a constant with the system. It means that a new item can enter in the system only when one of the items exit the system in order to maintain always the same level of WIP. Okay.
So here, let's analyze this case. We have in this case, we have a constant WIP level fixed at the 10 jobs. And this is a decision of the management. This results in a throughput of 0.5 jobs per hour. So the production rate of this line is 0.5 jobs per hour.
And this is defined by the bottleneck station of the system, and it is the second workstation. So the second workstation has a processing time of two hours. So the processing rate of this workstation is the inverse of the processing time, so one divided by two. So 0.5 jobs per hour. It means that in order to complete one job, it takes two hours.
So the rate of production is 0.5 jobs per hour. So this is the maximum reachable throughput because the so the the line the the throughput of the line is defined by this lower workstation. Okay? So the throughput of the line cannot be higher than 0.5 jobs per hour. That is the throughput of the second workstation.
Then so the the fact that that the throughput is 0.5 is a good thing because this is the maximum reachable throughput. So the management is fine with this value. But the concern of the management is the cycle time because they observe that the average cycle time is twenty hours per job. So it means that each item remains inside the system twenty hours. And this value is very high because if we consider in just the processing time of the workstations, the total processing time is only five hours.
So if we sum the processing times of the four workstations. So the fact that the cycle time is twenty hours means that a lot of time is spent in the queue waiting for being processed. It's also possible to compute an index that is called x factor. That is the ratio of cycle time to the average total processing time per job. So if we divide the total cycle time, that is 20 for the sum of all the processing times, that is five, we obtain an x factor of four.
It means that the cycle time is four times higher than only the processing time. And thus, this this quantity is very high. And from the literature, it emerges that the x factor for the sector of the company is only 2.6. So the problem is addressing this issue and find a way to reduce the cycle time in order to reduce the x factor. Now at this point, there is one possible solution to address this the cycle time value that is to purchase a new machine that is faster than the previous one.
For instance, that is 20% faster machine. So it means that instead of having a processing time of two hours, it has a processing time of only one point five hours. In this way, the x factor can be reduced, and the line can reach, can also improve, increase the throughput because we are so inserting a faster machine and does the throughput of the line can increase. But this solution is not feasible for the company because it has a cost. So buying a new machine has a cost and this money so the company doesn't want to use this money to to buy the new machine because they are needed for other purposes.
So instead, they decided to hire a consulting team from the manufacturing engineering department of the local university. So they go to the university and ask for a consultant team to perform a study and analysis of the factory performances. So in order to find a way to predict the performance measure of cycle time and throughput and see how they are affected by the the parameters of the factory. So here, the the team decided to perform a manual simulation of the plant, of the line, in order to understand which is the behavior. So they start with the system empty.
And since the whip is fixed to 10 jobs, at the beginning, all the 10 jobs are placed at the first machine. And then in each hour, there is an update of the status of the system. So at the beginning, all the machine are empty apart the first one, which contains 10 jobs. Then after one hour, the first job is moved to the second machine. After two hours, it finishes processing.
And now after two hours is the the first one is already processed by the second machine, but the second one is moved to the second and it waits in the queue before being processed and so on. In order to see how the items distribute among the workstations and see if so which is the long run, so the steady state behavior of the system. And and to see if the average cycle time is twenty hours as the management said. So now let's do the same thing step by step also also as so let's do the simulation of this factory by representing in a table the state of the system at each time. So now as usual, let's move to the other board and do the simulation manually by creating this table in which we report the time instant on the first column and then the state of the workstations, and finally, the throughput, the accumulative throughput.
Here, status of the of each workstation is composed by two terms in the parenthesis. So we have the first term, the first number that indicates the number of jobs at the workstation. The total number of jobs at the workstation, both in the queue and on the machine. And the second term represent the number of hours already completed for the job in processing at that workstation. In order to keep trace that at the second workstation, we need two hours to complete the processing.
Okay? So now let's let's do and fill this table at each time instant until we reach the steady state condition. So let me change the screen. So now we are simulating the PennyFab. So PennyFab company that is composed by three war four workstation, workstation one, then workstation two, then workstation three, and workstation four in a system represented by the arrow that comes back.
And with processing hours of one, two, one, one hours of processing at each workstation. Here we have a WIP level fixed to 10. So now let's build the table in which we have the time. And then the status of each workstation. So west one, station two, station three, station four, and the cumulative throughput.
K. All better. Let's first restart the throughput, the simple throughput, and then the cumulative. So firstly, the throughput that is not sorry. Not the throughput, but the output.
So output. At each time instant, we report if we have an output from the line and then the cumulative throughput. Then so the time, let's insert from zero to one, two, three, four, five, six, seven, eight, nine, ten, then we go on. And then let's define the meaning of the status of the workstation. So in each workstation, we insert a parenthesis with two terms, two numbers, x and y.
So x is the total number of items in the workstation. So dot number of items in the workstation. So both q and processing. And y is the number of hours already completed in processing. Number of hours already completed or processing.
K. So now let's start the simulation of the system. At time zero, all the items at are at Workstation one. So they are just inserted in the system. So we have a total number of items, at the first workstation and zero hours completed for processing.
So ten zero. And for all the others, we have zero zero. So zero items and zero hours and zero output. Then at time one, what happened? Well, one item is moved to the second workstation because its processing is finished.
So in the first workstation, we only have nine items, zero processing. So at time one, we have one item in the second workstation. Again, zero processing because we are at the beginning of the time instance. And again, zero zero in the others, also in the output. Then at time two, we have that the first workstation finishes the processing of the third item.
So it is moved to the next workstation to sorry, the second item. So here, we only have eight items remained. Instead, in the second workstation, we already have the first item in processing because it takes two hours. So the new item stays and waits in the queue. So in the second workstation, we have a total of two items, and we have one completed hour of processing.
So the second number is one two one. We have zero and zero again in the third and in the fourth workstation. Then at time three, k, workstation one goes on decreasing the number of items because at each hour it finishes the processing of one item. So at the time three here we have seven zero. And in the second workstation, what happened?
That one item finishes the processing and does is sent to the next workstation, and a new item arrive. K? So here we have a total of two items in the workstation. One that is arrived from the first and the other that can start the processing because the previous one move moved them. So 20.
In Workstation 3, we have the first item arriving. One item and zero. And in the fourth, again, zero zero. Then let's go on at time four. Again, Workstation 1 decreases the items, so six zero.
In Workstation 2, we have the new item arriving from Bus Station 1, but the previous one already in processing. So here, Workstation 2 increases its total number of items and has three items and one hour completed of process. In Workstation 3, Workstation 3 finishes the processing, so it comes back in the state 00 because the item is moved to Workstation 4. So here, the first item at time 4 arrives at Workstation 4. Then at time five, here, Workstation 1 decreases its number.
So let's write for a moment five here and then zero. In Workstation 22, we have one item entering and one item exiting because after two hours, the the item can leave the workstation. So we have always three items here and zero hours of processing. So the item is moved to the third workstation. So here we have one zero, And again, zero zero here because this item here that was in workstation four at the previous instant, now it's moved as output.
Okay. But if one item exit the line, then one new item can enter because we maintain the width constant at 10. Okay? So at each time in which we are we have an output, we also have a new input. Okay?
So here in workstation one, we don't have only five items. We have the new item also that is entered because one is exit. Okay? So here we put already we put again six in workstation one because here we have the first output. So the new item can enter in the system.
And here we are at time five. So at time five, we have the first output, also the first cumulative output. Then let's go on because until now, we we we have not reached the the steady state because the system behavior is changing. So let's go on and see what happened in time six. So at time six, we have the new item that is moves from Workstation 1 to Workstation 2.
So the total number here decreases five zero. Then in Workstation 2, we have the new item arriving, but the previous one is still in processing, so we increase the number four and one because the item is in processing. Then here, nothing arrives at Workstation 3, so zero zero. And the item arrives at Workstation 4. And so here we have one zero.
Yes. So there is the question. Can you repeat why in time five we have six items in Workstation 1? Yes. Because at each time instant, we maintain a WIP level of ten ten items inside the system.
So since at time five, we have the first output because Workstation 4 at the end of time four, so at the beginning of time five, exits the height the first item. So the first item at time five is outside the line. And thus, we need to increase, so to make one item new entering the line. And as here, we put six instead of five. Okay?
Okay. Then at time six, only we have only the the shift of items. Then at time seven, the same because this item here exit at time seven. So at time seven, we have the new output, and thus workstation one does not decreases. So at time seven here, we still have five zero.
Here instead in Workstation 2, we have one item arriving and the other exiting. So again, four zero, then one zero here and zero zero here, then we can start seeing a sort of recurring behavior, especially for workstation three and four. Instead, one and two are already changing. So let's go on. So at time eight, here, we have Workstation one that decreases of one, so four zero.
Then workstation two, the new item arrives, but the previous one is still in processing, so it increases the number five one. Workstation 300, Workstation 410. Then at time nine, again, at time nine, we have the other output, this one here. So we have the new item, and so it doesn't decrease. So four zero.
The workstation two remains five zero. Workstation 31 0. And Workstation four, zero, zero. Zero output. Then we arrive at time ten.
Time ten, then there is the decrease of workstation one, so three zero. And the increase of workstation two, six one. So the new items arrive, and the previous is still in processing. So nothing exit. So Workstation 3 is empty.
And instead, Workstation 4 has the new item. Then let's go on because you see now the the effect is that are you seeing the effect? So the items that at the beginning were before workstation one now are accumulating before workstation two because workstation two is the bottleneck. So workstation two is the slowest machine. So in the steady state, we expect that the q is so accumulates before workstation two.
And this is the effect that we are simulating. So now let's go on and insert other. So eleven, twelve, thirteen, fourteen, fifteen, sixteen, seventeen, eighteen. And then here, we reached the steady state in a few more repetition. So at time eleven, again, three, zero because we have the output.
At time 11, we have the output that derives from the previous row. So no no decreases. It remains six zero, then one zero zero zero. Then at time twelve, there is the decrease here, so only two items because the one is moved. So here we have the increasing of the items in the second workstation.
So seven one, then zero zero one zero. Then in the next row, we have the output. So at row 13, we have again two zero, here seven zero, then one zero and zero zero. Then at line 14, the decrease, so one zero. Here we have eight one, then zero zero one zero.
Zero output. Then the output is on the next row. So in row 15, again, zero, eight zero, one zero, zero zero. Then in line 16, we have 00910010. And then in line 17, again, one zero, nine zero, one zero, zero zero And then basically, now we have reached the steady state.
So if you go on in the following rows, you see that the last two rows repeat. So here, if you have understood the the reasoning, you understand that how the system evolve. Okay? So in this case, it just now at time 17, we reached the steady state because all the items accumulate before workstation two. Okay?
And then they are moved until they exit the line. So now let's come back. K. So here you can see that the other lines so they arrived until row 24. So and the pattern repeats.
So after fifteen hours, the status repeated. It fluctuate between these two states. Okay. So now we understood how the system behaves and how it evolves and reach the steady state. So now if we go on and compute the the performance measure, we obtain the throughput of 0.5 jobs per hour and a cycle time, an average cycle time of twenty hours as as expected.
So now the idea is well, instead of so buying the new machine, that was the option that was not addressed by the company, which can be another way of reducing the cycle time. Because if we we are able to reduce the cycle time, then we can reduce the x factor and submit the the original point of the management. So now the the reasoning is let's change the value of the WIP because until now, we consider the the WIP level of 10. So this was a decision taken at the beginning. But which is the effect of changing this value of the whip?
So now the the reasoning is let's recompute sorry, do the simulation, not manually. Now that we have understood how it works, let's just have a look at the slides and see what happen if the WIP level changes and which is the effect on the of the WIP level on the other two performance measures of the throughput and the cycle time. Okay? So now let's reconsider our line starting with the WIP equal to one. Okay?
So we have our line that is always a convoy per system even if the the second arrow is missing. And now let's redo the simulation. So at the beginning, at time zero, we have only one item in the system, and it's placed in the first workstation. Then after one hour, the item is moved to the second workstation. After two hours so at the beginning of the second hour, the item is still in the second workstation.
And then at the beginning of the third hour, it is moved to the third. Then at the time four, it is moved to the fourth. And the time fifth, it exit the line, and thus the new item can enter. And thus, we repeat again from time zero on. So now let's compute the value of the throughput and the cycle time for week equal to one.
Well, in this case, the throughput is one item every five hours. Exit the line. So the throughput is 0.2 jobs per hour. Instead, the cycle time is just the sum of the processing time. So the cycle time is five hours.
So you see that in this case, the cycle time is very good because it is the minimum reachable cycle time. But the throughput, no, because the throughput is only 0.2, It means that the line is not fully exploited because the maximum throughput is 0.5. Instead, now the line only works at a throughput of 0.2. So this is not a good solution fixing the WIP to one. So now let's increase the WIP of another unit.
Now let's consider the WIP equal to two. Here, let's consider that here we start from the steady state because at time zero, all the two items are at workstation two. Then after one hour, one is moved to the second and one remaining the first and so on. Okay. So here instead, we consider that at times zero, the two items are already in the two different workstation.
Okay. So let's just imagine that the system worked for a cycle, and then this is the steady state condition because we want to compute the cycle time and the throughput for the steady state conditions. So in this in this case, with whip equal to two, we obtain a throughput of two items every five hours. So we have two output every five hours. So the throughput is two over five.
So 0.4 jobs per hour. And the cycle time is still five hours. Then so in this way, we are, let's say, in improving the performances because the cycle time is still the minimum value, so a very good result. And the throughput is increasing, so now the throughput is 0.4. So it means that we equal to two is better than we equal to one because it reaches a higher throughput.
So now let's go on with this reasoning and increase the WIP equal to three. So with WIP equal to three, we obtain a throughput of 0.5. So now every so we have an output of three items every six hours, so a throughput of 0.5. But each item stays on the line for six hours instead of five. Because here, if we have a WIP of three, when the item arrives at the second workstation, the workstation is still processing the previous item.
So we have one hour one hour of waiting. And as from WIP equal to three, the cycle time start increasing. And if we increase even more the WIP, then we expect that the cycle time also increases because there is more time spent in the queue. Okay? So this is what we expect.
If we go on by doing the simulation, we will obtain some graph, some values such as the one reported in the in the fee in the table. So for WIP, you see that that the WIP if the WIP increases, the throughput at the beginning increases and then reaches the maximum available throughput of the line and so remain constant. Instead, the cycle time do the opposite. So it is constant at the beginning with lower WIP, and then it start increasing due to the increase of the waiting time. And this behavior is reported by the graph that are shown here.
Okay? So let's also, this is the second part. Let's do do it in in the blackboard for a time because I wanted to better explain the things that with respect to the slide. So let me again open the board, the simulation of the PennyFab with the WIP equal to 10. Then we do on the slides the simulation with WIP equal to one, then two, then three in order to understand the behavior.
So how the WIP affects the computation of the the value of the throughput and the cycle time. So now what I want to do is to report the values of the throughput and the cycle time on the two graph in order to understand the relationships. So let's do it only the graph without so let's just use the data on the table and report the the data on the two graph. In this graph, we have the on the x axis, and then we have the cycle time or the throughput in the y axis. So we have one graph for the cycle time and the other for the throughput.
So from our analysis, so the manual simulation of the WIP, so we found that for WIP equal to one so from whip from one, two, three, four, five. For whip equal to one, the cycle time is five. Then for weep equal to two, again, And then for weep equal to three, it is six. So here, then for whip four, it's eight, and then ten, twelve, 14, and so on. So here, the effect of the cycle time is that it start increasing and it follow this path of increasing pattern in this way.
Okay? Instead, the throughput starts for week equal to one, the throughput is 0.2. Then for a week equal to two, the throughput is 0.4. So it start increasing. Then for we pick one to three, it is 0.5.
And it remains 0.5. Okay? So the throughput follow follows a different behavior. So it start increasing, then it reaches the maximum value and then remains constant. Okay.
So here, if we wanted to conclude the the original problems of the analysis of the PennyFab, so which is the answer of the original problem that is reducing find another way of reducing the cycle time. Well, here, the answer is that well, if we are able to reduce the WIP at, for instance, three jobs, we are able to maintain the maximum throughput, so throughput of 0.5, but we decrease the cycle time at six instead of 20. So here, the previous WIP was 10, and it corresponds to a cycle time of 20 because it follows this graph, so this behavior. But if we are able to reduce the WIP, then the effect is that also the cycle time is reduced. So we can try to reduce the WIP always considering to maintain the maximum throughput.
Okay? So not under this value. Then the last thing that I want to show you is now considering again the behaviors or the trend of these two graph, can express them also in formulas. Okay? So we can write which is the expression of the cycle time.
So in this case, we have the cycle time. So in general, it is constant to a specific value if the WIP is lower than a specific value of the WIP. So the cycle time can be expressed as equal to a fixed value that we call t zero if the WIP is lower or equal to a specific value of the WIP that we call w zero. And then if the WIP is higher than this value, then the cycle time is equal to, by using the little slow, to the width divided by the throughput of the line. And let's call the throughput of the line as r b.
R b is another fixed value. Otherwise k? So t zero, r b, and w zero are specific value depending on each case. But for each system, we are able to define the cycle time as in function of the whip by using this formula. Then the specific value of t zero, w zero, and r b changes depending on the specific example.
The same can be written for the throughput, but the throughput follows the opposite behavior. So we have a throughput of, at the beginning, it is increasing. So the throughput is equal to WIP divided by the minimum processing time that is called t zero. If whip is lower or equal to w zero. And then one of the once this point is reached, it remains constant to the maximum throughput of the line that is r b.
R b, otherwise. K. So here we can define the formulas of the cycle time and the throughput for different values of the WIP by using these three fixed parameters, t zero, w zero, and r b. These three parameters have also a name in addition to the acronym, and t zero is called raw process time. Then air b is called bottleneck rate.
And w zero is the critical whip. K. So for each line, for each system, we can define the value of these three parameters. So these are, let's say, input values. And then we are able to express the cycle time and the throughput depending on these values in function of the WIP.
So we are able to estimate the cycle time and the throughput for different number of WIP by using these three parameters. K. So coming back to the slides, have so seen until so the simulations, then the graph, then the things that we have seen together on the graph, and finally, these formulas. Okay? So the cycle time remains constant at the minimum cycle time that is called t zero as WIP increases, and it increases to infinity once maximum WIP is reached.
The throughput increases as WIP level increases until the WIP reaches the maximum WIP. After that, the throughput stabilizes remaining constant at r b. So the best case is where you have the minimum cycle time and the maximum throughput. So in this case, where the WIP is equal to three in this example. Now I think that for today is enough.

Okay. So, let's start where we ended yesterday. K. So yesterday, we ended these formulas. So we we have seen how to compute the cycle time and the throughput for different values of WIP depending on three parameters that are called critical parameters of the line.
So here, just recall the definition. We defined the bottleneck rate, r b, as the throughput of the workstation, which is the bottleneck of the line. This is the throughput of the slowest workstation That is also the maximum throughput obtainable from the line. The second parameter is t zero. That is the raw process time.
That is the sum of the average process time of each workstation in the line. And this value represents the minimum possible cycle time. So this is the minimum time each item spends inside the system. And the third parameter is the critical WIP, w zero, that is the product of r b and t zero. And this represent the the WIP level, which allows to achieve both the maximum throughput and the minimum cycle time.
Okay? Now let's now see two examples on how to compute these critical parameters in two sample lines. First one is a balanced production line composed by four machines in series. We know that each machine has a two hours processing time. So this is why the line is called balanced because each machine has the same processing time.
Thus, from the processing time, we also know the capacity of each machine. That is the production rate, and this is the inverse of the process time. So one over two, so 0.5 jobs per hour. Then we know that once an operation is completed, the product goes immediately to the next machine. And the machines work continuously without failures or stops, and we don't have any discharged items.
So now the question is, which are the critical parameters of this line? Okay. So the reason is okay. First thing, let's identify the bottleneck. The bottleneck is the workstation with the lower capacity.
And since in this example, all the machines has the have the same capacity, then all of them are the bottleneck. And thus, the bottleneck rate is 0.5 parts per hour. In this case, all the machines have the same capacity. Then which is, in this example, which is the raw process time, so which is the minimum cycle time reachable by the items. We need to sum all the processing times of the machines.
So two plus two plus two plus two, and we obtain eight hours. So in this example, the raw process time is eight hours. And then to obtain the critical WIP, that is the WIP level that allows to obtain the maximum possible throughput at the minimum cycle time is the product of the bottleneck rate and the raw process time. So 0.5 multiplied eight hours, and we obtain four items. Okay?
And here you have these the results. So this is a very simple example on how to compute the critical parameters in a simple line. It's a balanced line with the the machine all the machines with the same capacity. Now let's see another example with not balanced production line, and the line is a little bit more complex. So in this case, we have the line composed of, again, four workstations.
But each workstation is composed by a different number of machines. So if you remember, we defined a workstation as set of identical machines that have the same parameters, so the same processing parameters, and that work in parallel. So here in the table, we have the the data, the input data of of each workstation. So workstation one contains only one machine, and the process time of the machine is two hours. Then Work Station 2 contains two machines, and the process time is five hours.
This is the process time of each machine. Then workstation three contains six machines with the process time of ten hours. And the fourth workstation contains two machines with a process time of three hours. So here, the thing is before computing the critical parameters, we have to compute the capacity of each workstation. Because if we have a parallel machines, then the capacity of the workstation is given by capacity the sum of the capacity of each machine inside the workstation.
Okay? So let's fill the table. Let's do it together for workstation, and the workstation one is composed by a machine. So let's indicate in this way. The first workstation has one machine, then the second workstation has two machines.
Then the third has six machines in parallel, and then the fourth two machines. And, in the table, we report the parameters. So workstation one, two, three, and four. We have the number of machines for each workstation. One, two, six, two, and the process time.
The process time is indicated as EOTS of the machine. That is two hours, five hours, ten hours, and three hours. Then let's firstly compute the capacity of each machine. So this is the machine capacity. It is the inverse of the processing time.
So one divided by EOTS. And this quantity later will be called with the letter more. But now, okay, it's enough to call it one over ETS. So for the first machine, the capacity is one over two, so 0.5 jobs per hour. Then for the second, we have one divided by five.
So 0.2 if these are hours. Then for the third one divided by ten, zero point one. And for the fourth, divided by three, zero point thirty three. Okay? So this is the capacity that is the production rate of each machine.
And then we obtain the workstation capacity. That is the sum of all the machine capacity in this worst in that workstation. So in the first workstation, I have one machine multiplied by the its capacity, so it remains 0.5 jobs per hour. In the second, we have two machines multiplied by 0.2, so 0.4 jobs per hour. In the third, we have six machine machines multiplied by 0.1, so 0.6 jobs per hour.
And in the fourth one, we have two multiplied 0.33. 0.667 jobs per hour. Okay. So now that we have all these so the capacity for each workstation, then we can compute the bottleneck rate. So what do you think among these four workstation?
Which is the bottleneck of the line? So the bottleneck is the workstation with the lower capacity. The capacity of the workstation, okay, not the single machine. So in this case, the slowest machine is the slowest workstation is the second. This one this one is the bottleneck.
So this is RB. Erb is 0.4 jobs per hour. Then, which is the raw process time? So t zero. T zero is the minimum time an item spent in the system in the line.
So the minimum time is given by the sum of all the processing times. Here are the machines. So t zero is two plus five plus 10 plus three. That is twenty hours. The sum of all the processing times.
And then once we have the bottleneck rate and the raw process time, we compute the critical WIP. So w zero is 0.4 jobs per hour multiplied twenty hours, and the result is eight jobs. K? Then this approach is also appliable in, real cases, so more complex systems. As in the next slide, you have, the description of another company that is called Hull that produces a large panel for the computers, so microprocessors.
And in this company, we have several workstations that execute different technological processes that are listed in the table. So we have a workstation for the lamination, another for the machining, another for internal circuit ties, then the optical test, repair, and so on. So these are all the workstations available in the company. And for each of them, we know both the production rate, so the capacity, and processing time. Here, not always the rate is the inverse of the time because we have multiple machines.
So here we don't know how many machines we have, so we cannot do the computation by hand. But we have directly the final numbers. So for each workstation, we know the capacity of the workstation and the processing time. So from this data, we are able to compute the critical parameters because the bottleneck rate, r b, is the minimum of the capacities of the workstation. So if you select the minimum value of the column rate, you'll find that the bottleneck rate is 114 parts per hours that correspond to the third process, so the internal circuitizer.
And if you do the sum of all the processing times, you obtain a total of 33.9, and this is the minimum possible cycle time. Okay? And then if you multiply these two values, you obtain the critical WIP. So once we are able to compute the critical parameter, then the idea is to compare them with the actual behavior of the company. So let's assume that this company has this performance in the last seven months.
So we know that the line runs twenty four hours a day, but the working hours are only nineteen point five instead of twenty four. And the performances are a throughput of 1,400 panels per day that corresponds to a throughput expressed in hours of 71.8 panels per hour. Then a WIP of 47,600 panels and a cycle time of thirty four days that corresponds to six hundred sixty three hours. So now the question is, by looking at these numbers, how the alley is performing, how the company is performing. So in order to answer to this question, we can compare these real values with the critical parameters that are that represent the best conditions.
So the minimum possible cycle time and the maximum available throughput and the corresponding WIP. So here, if we compute the critical WIP, we obtain a value of 3,869. And by comparing the actual value with the critical parameters, we can say that, okay, the throughput is only 63% of the capacity of the maximum reachable throughput, so not a very good result. Then the WIP is very high compared to the critical WIP. It's 12 time the critical WIP.
And also the cycle time is 24 time the raw process time. So it means that the so the the raw process time is only thirty three point nine hours, but the actual value of the cycle time is six hundred sixty three hours. So it means that the items spend a lot of time waiting in the queue without being processed. So the factor is not performing very well. So the idea of being able to compute the critical parameters is to being able to compute the optimal values.
So the best case, the best obtainable performances of the system, and then to compare them with the actual value in order to see if there is room for improvement of the plant. Now let's go on with two more exercises so you can practice with the things that we have seen today and yesterday of the critical parameters. The first exercise, let's read together the text, then I leave you as usual few minutes to solve it, and then we check it together. So let's consider a production line composed of forward stations, each consisting of a single machine, except the second station which consists of two identical machines in parallel. Each machine has a mean process time equal to two hours per job.
With this data, let's compute the bottleneck rate, the raw process time, and the critical WIP of the line. And then also compute the cycle time, the throughput, and the WIP the cycle time and the throughput values for a WIP going from one to 10. So let's apply the formulas that we have seen yesterday to compute the cycle time and throughput for different numb values of WIP in this system. So a few minutes for you, and then we check the solution. Oh, we have the first workstation with one machine, the second with two machines, then the third and fourth with one machines.
Then let's write the table to compute the capacity of each workstation. Number of machines. One two one one. Then the processing time, EOTS, that is two hours for each machine. Then the capacity of the machine, the inverse of the processing time, 0.5, 0.5.
0.5 jobs per hour. And then the capacity of the workstation. It is 0.5 for the first, or two multiplies 0.5 for the second, zero zero point five and zero point five. Okay. So, let's compute the critical parameters.
So r b is the bottleneck rate. So the slowest capacity, 0.5 jobs per hour. Then the critical whip the raw process time, it is the sum of all the processing time. So two multiply by four, eight hours. And the the critical whip, it is the multiplication.
So 0.5 jobs per hour multiplied eight hours, so four jobs. Okay. The same results as before. Then to answer the second question, let's recall the formulas. Let me change the the page.
So let's recall the formula to compute the cycle time and the throughput depending on the WIP. So let's remember that the cycle time is computed as t zero if the whip is lower or equal the critical whip and is equal to the whip divided by r b if WIP is greater than the critical WIP. And the throughput is computed as the WIP divided by the raw process time if the whip is lower or equal to the critical whip and r b. If the whip is greater than w zero. Okay.
So let's compute the value of the cycle time and the throughput for the whip from one to 10. Let's do it in the table. So we have the WIP from one to 10. Then the cycle time and the throughput. So the cycle time, so the critical WIP in this case is four.
We have that until four, we apply one formula. And over four, we apply the other, the second one. So for the cycle time, for WIP from one to four, the cycle time is equal to the raw process time, so eight. And then it's equal to whip divided by r b, and r b is 0.5. So for whip equal to five, have whip five multiplied RB.
So then the cycle time is in hours. Then six multiplied 0.512, and so on. So fourteen, sixteen, eighteen, and twenty. So the cycle time start increasing with this rate. Then for the throughput, we have for WIP from one to four, we apply the formula.
WIP divided raw process time. So one divided by eight is zero point one hundred and twenty five. The throughput is expressed in jobs per hour. Then two divided by eight, zero point twenty five. Then three divided by eight, zero point three seven five.
And four divided by eight, zero point five. Now we have reached the the bottleneck rate, and then the throughput remains equal to the bottleneck rate for all the other values of the WIP. So zero point five, zero point five, and so on until 10. Now let's also represent these values in the two graph, one for the cycle time. So for the cycle time, we have at the beginning, a cycle time of eight.
For here, we have WIP and here cycle time. So we have here eight until four. And then start increasing. So five is ten, six is 12, and so on. So this is the graph of the cycle time and the graph for the throughput.
The throughput start at 0.125 at one, then raise to 0.25 at two, then at 0.375, and then 0.5 at four, and then remains 0.5. K. And we have so the graph for the cycle time and the throughput depending on the WIP. These other exercise is taken from an exam of the previous year. So it was, let's say, an open question.
So you know that in the exam, you can have both multiple choice questions and then exercises or open questions in the second part. So this was the question that I asked the last year. So consider a production line composed by three workstations in series. The characteristics of the workstations are reported in the table. Compute the bottleneck rate, the raw process time, and the critical WIP of the system.
This is the first point. So compute the the critical parameters. And then answer the question, what happened to the throughput and the cycle time values when the WIP exceeds the critical WIP? So now let's try answering this question as it was an exam question. So we are able to so to evaluate if your answer is correct, totally, or partially.
So you also better understand what the what I ask, what I I want that you write during the exam. So let's first try to answer by yourself, and then we see the solution. So here, let's fill the table as usual. With the data. And the processing times in minutes.
And the capacity in jobs per minute. So the inverse of the processing time, so one over three, zero point thirty three, one over two, zero point five, and one over four, zero point twenty five. And then the capacity of the workstation. 0.33 multiplied by two, zero point sixty six. Then 0.5 remains 0.5, 0.24 multiplied by four by three.
Sorry. 0.75. Also here, unit of measure is jobs per minute. Okay. So here, let's compute the critical parameters, which is the bottleneck of this line.
It is the workstation with the lowest capacity. So the second one. So in this case, r b is equal to 0.5 jobs per minute. Then the row process time t zero is the sum of all the processing times. Three plus two plus four.
So nine minutes. And the critical whip is the product 0.5 multiplied nine, four point five jobs. This is the answer to the first question. So compute the critical parameters of the line. Then what about the second question?
So explain what happened to the throughput and the cycle time values when the WIP exceeds the critical WIP. What do you think is the answer to this question? Don't you want to try writing your answer here in the chat? So here, the answer that I expect here is saying that so if the WIP exceeds the critical WIP, then the throughput remains constant at the value of the bottleneck rate, so 0.5 jobs per minute. And the cycle time increases at the rate of WIP divided by 0.5.
And here, if you want, you can also report the formulas that you used. So here the answer to the second question is, if the exceeds the critical WIP, so w zero. Then the throughput remains constant at 0.5 jobs per minute. And the cycle time increases at rate divided by 0.5. And in addition to this sentence, you could also have reported the formula of the cycle time and the throughput that we have seen before.
So oops. K. So this formula here, cycle time and the throughput. K? Then the last thing be before moving to the next topic, paste here the link of a form that I prepared with other so three questions summarizing these things.
Let me so here, just paste it here. This is the link. This one. Okay. Okay.
So please access the form and answer to the questions. Okay. So let's check your answer. So here, let's see. So for the first question, yes, you answered correctly.
So which is the definition of a workstation? It's a collection of one or more identical machines performing the same function. Then the bottleneck rate, very well. All of you answered correctly, so the throughput rates of this lowest workstation. And then where is?
So consider a line of n workstations, each with a single machine. The processing time of each machine is k minutes, which is the critical width of the line. Here you divide it more or less equally in three parts. Here, you you just have to do the, the computation. So you know the processing time of each machine.
You know that you have n workstation each with a single machine, and the processing time is k. So you also know the pro the bottleneck rate because all the machines have the same capacity that is one over k. So let me do the computation here. So you have n workstation with EOTS, so processing time equal to k. So the critical WIP w zero is r b multiplied by t zero.
And which is r b, so the button crater is the inverse of the processing time. So one over k. And t zero is n time. K, n time the processing time, so n multiplied by k. So by doing the product, we obtain w zero of n.
This, again, this was a question taken from one exam of last year. This is an example of the multiple choice questions.

# Analysis and Management of Production System

# Lesson 3: Single Workstation Analysis

Prof. Giulia Bruno

Department of Management and Production Engineering

giulia.bruno@polito.it

# Deterministic vs Stochastic Models

V The simple throughput analysis of a serial factory with deterministic processing times was used to illustrate several system performance measures and their inter-relationships   
V The modeling approach was developed specifically for deterministic processing times

>This approach does not yield accurate results when processing times are random   
The next models will include probabilistic behavior for the arrival process and processing times,and the early models will restrict these two probability laws to the exponential distribution

# Variability

Definition: not uniformity of a class of entities   
>It causes a departure from regularity and predictability of the system behaviour   
Examples of variability sources:   
>Machine failures   
>Material shortages   
Operator unavailability   
>Different skill levels   
>Material handling   
>Product variety

# Variability

> Random variable: consequence of events out of our immediate control   
A random variable is characterized by:

Type of distribution: Exponential, Normal,Poisson.,..   
V Parameters:

V Mean value μ   
Variance g2   
V Skewness   
V Kurtosis   
V

# Variability

> To classify and to quantify the variability of a random variables, dimensionless coefficients are used:

Coefficient of Variation (CV):

$$
c = \frac {\sigma}{\mu}
$$

Squared coefficient of variation (SCV):

$$
c ^ {2} = \frac {\sigma^ {2}}{\mu^ {2}}
$$

# Variability

> To allow the comparison，systems are classified according to the level of variability expressed through the coefficient of variation:

>Low variability (LV): c < 0,75   
>Moderate variability (MV): 0,75 < C < 1,33   
>High variability (HV): c ≥ 1,33

Mean Value = 25 min

StDev = 5.65 min

CV = 0.226

### Visual Diagram: Variability Classification Axis
- **Component Type**: Quantitative classification scale.
- **Logic**: Categorizes production systems into three levels of variability based on the value of the Coefficient of Variation ($c$).

#### 1. Axis Structure
*   **Variable ($c$)**: The horizontal axis represents the Coefficient of Variation, defined as the ratio of standard deviation to the mean ($c = \sigma / \mu$).
*   **Scale**: The axis starts at 0 and increases to the right, using color-coded segments to define performance zones.

#### 2. Variability Thresholds
The diagram establishes three specific regimes:
*   **Low Variability (LV)**: Highlighted in green for values where **$c < 0.75$**.
*   **Moderate Variability (MV)**: Highlighted in blue for values in the range **$0.75 \le c < 1.33$**.
*   **High Variability (HV)**: Highlighted in red for values where **$c \ge 1.33$**.

# Effect of variability

# Example

Constant processing time:

$$
t _ {0} = 1 0 \mathrm {m i n}
$$

Constant arrival rate:

$$
A = 1 / 3 0 \quad p c s / m i n
$$

$$
\mathrm {B} = 1 / 2 0 \quad \mathrm {p c s} / \mathrm {m i n}
$$

$$
C = 1 / 1 0 \quad p c s / m i n
$$

$$
D <   1 / 1 0 \quad p c s / m i n
$$

### Visual Diagram: Effect of Variability
- **Component Type**: Integrated process flow and utilization graph.
- **Logic**: Demonstrates a system with zero variability (constant arrival and service times) to illustrate the theoretical behavior of queues at varying utilization levels.

#### 1. System Layout
*   **Process Flow**: Illustrates items arriving, entering a buffer ("Units waiting for process"), and moving to a server with a fixed **process time of 10 minutes**.
*   **Deterministic Assumption**: Both the inter-arrival times and the processing times are constant, meaning there is no randomness in the system.

#### 2. Utilization vs. Waiting Items Graph
The plot illustrates how the system queue behaves as the arrival rate increases toward the processing capacity:
*   **Points A & B**: Represent arrival rates significantly below capacity (e.g., $1/30$ and $1/20$ pcs/min). Because the system is perfectly regular and arrival is slower than service, the number of items waiting remains at **zero**.
*   **Point C**: Marks the **100% utilization** point where the arrival rate exactly matches the processing capacity ($1/10$ pcs/min). 
*   **Point D**: Shows that if the arrival rate even slightly exceeds the capacity in a deterministic system, the queue grows toward infinity because the server can never "catch up."

#### 3. Theoretical Baseline
This diagram provides the "ideal" baseline for Factory Physics: in a world with zero variability, we could run a machine at 100% utilization without ever having a queue. Any deviation from this horizontal line in real systems is caused by variability.

# Effect of variability

# Example

Constant processing time = 10 min

Variable arrival rate

Waiting time in queue = 3 min

6 units processing time = 65 min

Mean waiting time = 3/65 = 0.046 min

Inactivity time = 5 min = 7.7% of 65

Utilization = 92.3%

### Visual Diagram: Effect of Variability
- **Component Type**: Numerical data table and Gantt-style timeline chart.
- **Logic**: Illustrates how variability in arrival times creates system waste (idle time) and congestion (queues) even when the processing time remains constant.

#### 1. Data Table Breakdown
The table tracks six items (**A through F**) through a single workstation with a **constant process time of 10 minutes**:
*   **Arrival Times**: Items arrive at irregular intervals (e.g., Item B at 12 min, Item C at 20 min).
*   **Waiting Times**: Although the machine is fast, Item C must wait **2 minutes** and Item E must wait **1 minute** because they arrive before the previous job has finished.
*   **Process Flow**: The "Start of process" is dictated by either the arrival time or the "End of process" of the preceding item, whichever is later.

#### 2. Visual Timeline Analysis
The chart maps the table data onto a 65-minute timeline, highlighting two types of inefficiency:
*   **Unused Machine (Blue)**: These gaps represent idle capacity. They occur when the machine is empty but no job has arrived yet (e.g., between Items A and B, B and C, or D and E). There are **5 minutes** of total idle time.
*   **Waiting Time in Queue (Red)**: These blocks represent jobs waiting for the server to become available. Even with idle periods earlier, the system still experiences **3 minutes** of total queuing.
*   **System Paradox**: This demonstrates that variability prevents a system from being perfectly efficient; you can have both "starvation" (idle machines) and "congestion" (waiting jobs) within the same period.

#### 3. Performance Summary
Based on the 65-minute observation period:
*   **Utilization**: **92.3%** (calculated as $(65 - 5) / 65$).
*   **Mean Waiting Time**: **0.046 minutes** per job (3 minutes total wait / 65 minutes duration).
*   **Inactivity**: The machine was idle for approximately **7.7%** of the time.

Units which enters in a process with variable arrival times and a constant processing time (10 minutes)

# Effect of variability

### Visual Diagram: Transition from Deterministic to Stochastic Variability Effects
- **Component Type**: Comparative analysis of performance curves.
- **Logic**: Illustrates the fundamental shift in system behavior when moving from an "ideal" deterministic environment (top) to a "real-world" stochastic environment (bottom) where arrival and process times vary.

#### 1. Top Graph: The Deterministic Case (Constant Rates)
This plot shows the theoretical behavior of a system with zero variability (constant inter-arrival and process times):
*   **Axis**: Maps **Utilization** (X) against **Waiting Items** (Y).
*   **Points A, B, & C**: Represent a flat line at zero. In a deterministic world, no queue forms as long as utilization is $\leq 100\%$.
*   **Point D**: At exactly $100\%$ utilization, any infinitesimal increase in load causes the queue to grow infinitely, represented by the vertical dashed line.

#### 2. Bottom Graph: The Stochastic Case (Variable Rates)
This plot represents the system behavior observed in the stochastic arrival example:
*   **Axis**: Maps **Utilization** (X) against **Mean Waiting Time** (Y).
*   **The Non-Linear Curve**: Unlike the deterministic case, the waiting time is no longer zero. It begins to rise gradually and then grows exponentially as it approaches the $100\%$ saturation point.
*   **Point X**: Corresponds to the numerical results: at **$92.3\%$ utilization**, the mean waiting time is **$0.046$ minutes**.
*   **Visual Significance**: Even before reaching full capacity, variability "steals" capacity, forcing jobs to wait because of the lack of perfect synchronization between arrivals and service.

#### 3. Key Takeaway
The blue arrow indicates the transition from theoretical "ideal" planning to realistic performance. It highlights the **Variability Law**: as utilization increases, the presence of variability causes waiting time (and thus WIP) to increase disproportionately. To improve performance, one must move the curve downward by reducing variability.

# Effect of variability

### Visual Diagram: Strategies for Managing Variability
- **Component Type**: Performance curve analysis graphs.
- **Logic**: Demonstrates the impact of reducing variability on system performance and the strategic trade-offs between utilization and waiting time.

#### 1. Top Graph: Decreasing Variability
*   **Axis**: Maps **Utilization** (X-axis, 0 to 100%) against waiting time (Y-axis).
*   **Multiple Curves**: Shows a family of curves representing different levels of system variability.
*   **The Arrow**: A large diagonal arrow points downward and to the right, labeled "Decreasing Variability." It illustrates that as you reduce variability in arrival or process times, the entire performance curve shifts lower. For any given level of utilization, the waiting time is significantly reduced.

#### 2. Bottom Graph: Strategic Trade-offs (Points X, Y, Z)
This graph highlights three distinct operational strategies on a variability curve:
*   **Point X (High utilization but long waiting times)**: Represents a system pushed close to maximum capacity (e.g., $90\%$ utilization). Due to the steepness of the curve at this level, jobs experience very long queues.
*   **Point Y (Short waiting times but low utilization)**: Represents a system operating at a much lower capacity (e.g., $40\%$ utilization) on the same variability curve. Waiting times are short, but the machine is idle most of the time, resulting in poor asset utilization.
*   **Point Z (Reduction of variability)**: The ideal state. By structurally reducing variability (moving to a lower curve), the system achieves both high utilization (like X) and short waiting times (like Y) simultaneously.

#### 3. Managerial Implication
The graphs visually reinforce a core principle of Factory Physics: you cannot simply increase utilization without paying a penalty in cycle time unless you first reduce the underlying variability in the system.

X = accepting long waiting times to obtain a high utilization of the machine

Y = accepting a low machine utilization to obtain short waiting time

Z = reducing the variability of arrival times and processing times to obtain a higher utilization and short waiting times

# Example: limited system

Consider a facility with a single machine that is used to service only one type of job.

The company policy is to limit the number of orders accepted at each time to 3.

The mean arrival rate of orders,λ, is 5 jobs per day,and the mean processing time for a job is 1/4 day (thus, the processing rate is μ = 4/day).

Both the processing and inter-arrival times are assumed to be exponentially distributed.

# Diagram model

> Straightforward method for developing the balance equations for ay system in steady-state whose inter-arrival and service times are exponentially distributed   
> The approach is to start by listing all the states as nodes in a network   
Each state represents the number of items in the system   
The node listing is

### Visual Diagram: Initial State Nodes for a Finite Queuing System
- **Component Type**: State-transition diagram nodes.
- **Logic**: Represents the first step in modeling a workstation with limited capacity (M/M/1/3) by listing all possible discrete states as nodes in a network.

#### 1. Node Definitions
*   **State Space**: The circles labeled **0, 1, 2, and 3** represent the specific states of the system based on inventory levels.
*   **System Status**: Each node number corresponds to the total number of items currently in the workstation:
    *   **0**: The system is empty (idle).
    *   **1**: One job is present in the system (being processed).
    *   **2**: Two jobs are present in the system (one in process, one waiting).
    *   **3**: The system has reached its maximum capacity of three jobs.

#### 2. Analytical Role
*   **Foundation for Balance Equations**: These nodes serve as the starting point for developing balance equations for systems in a steady-state.
*   **Network Development**: These nodes will subsequently be connected by directional arcs to represent flows: arrivals ($\lambda$) moving the system to the right and service completions ($\mu$) moving it to the left.

# Diagram model

> Directional arcs are added to the network to represent possible flows between nodes.

>Node 0 is connected to node 1 to represent the flow from state 0 to 1 when an arrival occurs, and the system is in state 0   
>Node 1 is connected to node O to represent the flow when a service occurs with the system in state 1 (a service results in an empty system or state 0)

> Note that an arrival into the system cannot occur when the system is in state 3 (i.e., when the system is full)

### Visual Diagram: State-Transition Network with Flow Arcs
- **Component Type**: Directed state-transition network.
- **Logic**: Adds directional arcs to the previously defined nodes to represent the possible movement (flows) between discrete system states.

#### 1. Flow Representation
*   **Forward Arcs ($0 \to 1 \to 2 \to 3$)**: These directional arrows represent arrivals into the system. For example, node 0 is connected to node 1 to show the flow that occurs when an arrival happens while the system is empty.
*   **Backward Arcs ($3 \to 2 \to 1 \to 0$)**: These arrows represent service completions. For example, node 1 is connected to node 0 to show the system returning to an empty state after a job is processed.
*   **Finite Boundary**: There is no forward arc exiting node 3, reflecting the constraint that arrivals cannot enter the system when it is already full.

#### 2. Analytical Role
*   **State Transitions**: The arcs visually define every possible way the system can change from having $n$ items to $n+1$ or $n-1$ items.
*   **Prerequisite for Balance**: This completed network is the necessary visual tool for deriving steady-state balance equations, where the flow into a state must equal the flow out.

# Diagram model

> Upward movements among the states all occur at a rate λ times the probability of being in that state,Pn

>The conditional arrival rate given that the system is in state n is ^ and the net upward rate from state n is λ Pn

Downward movements all occur when a service has been completed and these have rates that are μ times the probability of being in the particular state, Pn

>The conditional service rate given that there is a job in the system to be serviced is μ and the resulting downward rates from state n is μ Pn

### Visual Diagram: State-Transition Network with Transition Rates
- **Component Type**: process diagram.
- **Logic**: Quantifies the movement between system states by assigning specific rates ($\lambda$ and $\mu$) to the transition arcs, enabling the calculation of steady-state probabilities.

---

#### 1. Transition Rate Definitions
*   **Arrival Rate ($\lambda$)**: Represents the frequency at which new jobs enter the system. Upward movements from state $n$ to $n+1$ occur at this rate.
*   **Service Rate ($\mu$)**: Represents the processing speed of the workstation. Downward movements from state $n$ to $n-1$ occur at this rate when a service is completed.

#### 2. Flow Dynamics
*   **Net Flow Calculation**: The actual flow rate between states is determined by multiplying the transition rate by the probability ($p_n$) of being in the origin state. For instance, the net upward rate from state $n$ is $\lambda p_n$.
*   **Boundary Constraints**: An arrival cannot occur when the system is in state 3 because the system has reached its maximum capacity. This is why there is no $\lambda$ arc moving forward from the final node.

#### 3. Analytical Application
*   **Steady-State Balance**: This diagram is the primary tool for deriving balance equations, based on the principle that the flow into each state must equal the flow out of it.
*   **Example Equation**: By partitioning the nodes between state 0 and state 1, you obtain the first balance equation: $\lambda p_0 = \mu p_1$.

# Diagram model

The completed directed network can now be used to derive the steadystate balance equations   
> Assuming that a steady-state exists, then the flow into and out of each state must balance   
Partition the nodes into two subsets of nodes, then establish values for the appropriate steady-state probabilities to balance the flow between the two subsets   
> Partitions are redrawn at n-1 different locations to obtain n-1 equations; these equations are combined with the norming equation   
First equation

### Visual Diagram: Partitioning for the First Balance Equation
- **Component Type**: Partitioned state-transition diagram[cite: 1].
- **Logic**: Illustrates the method of partitioning nodes into subsets to establish steady-state balance equations.

#### 1. The Partitioning Method (The "Cut")
*   **The "Cut"**: A diagonal line intersects the transition arcs specifically between **node 0** and **node 1**.
*   **Subset Definition**: This partition separates the system into two subsets: the state to the left (idle) and the states to the right (active/busy).
*   **Steady-State Requirement**: For a steady-state to exist, the flow moving out of a subset must exactly balance the flow moving back into it.

#### 2. Deriving the First Equation
*   **Outward Flow**: Represents an arrival ($\lambda$) occurring when the system is in state 0. The rate is defined as **$\lambda p_0$**.
*   **Inward Flow**: Represents a service completion ($\mu$) occurring when the system is in state 1. The rate is defined as **$\mu p_1$**.
*   **First Equation**: Equating these flows across the partition yields the balance equation.

#### 3. Analytical Role
*   **Iterative Application**: This "cut" procedure is repeated at each boundary (between 1-2 and 2-3) to generate a system of $n-1$ equations[cite: 1].

$$
\lambda p _ {0} = \mu p _ {1}
$$

# Diagram model

Second equation

### Visual Diagram: Partitioning for the Second Balance Equation
- **Component Type**: Partitioned state-transition diagram.
- **Logic**: illustrates the method of partitioning nodes to establish the second steady-state balance equation in a finite queuing system.

#### 1. The Partitioning Method (The "Cut")
*   **The "Cut"**: A diagonal line intersects the transition arcs specifically between **node 1** and **node 2**.
*   **Subset Definition**: This partition separates the system into two distinct subsets: states {0, 1} to the left and states {2, 3} to the right.
*   **Steady-State Requirement**: For the system to remain in steady-state, the flow moving from the left subset to the right must exactly balance the flow moving from the right subset to the left.

#### 2. Deriving the Second Equation
*   **Outward Flow (Left to Right)**: Represents an arrival ($\lambda$) occurring when the system is in state 1. The rate is defined as **$\lambda p_1$**.
*   **Inward Flow (Right to Left)**: Represents a service completion ($\mu$) occurring when the system is in state 2. The rate is defined as **$\mu p_2$**.
*   **Second Equation**: Equating these flows across the partition yields the balance equation.
  
#### 3. Analytical Role
*   **Iterative Process**: This "cut" is the second of three possible partitions in an M/M/1/3 system. 

$$
\lambda p _ {1} = \mu p _ {2}
$$

Third equation

### Visual Diagram: Partitioning for the Third Balance Equation and Norming Equation
- **Component Type**: Partitioned state-transition diagram and mathematical summation.
- **Logic**: Illustrates the final partition of the state space to complete the system of balance equations and introduces the conservation of probability.

#### 1. The Final Partition (The Third "Cut")
*   **The "Cut"**: A diagonal line intersects the transition arcs between **node 2** and **node 3**.
*   **Subset Definition**: This partition separates the system into states {0, 1, 2} on the left and the boundary state {3} on the right.
*   **Third Equation**: Equating the flow rates across this boundary (arrival into the full system vs. service completion from the full state).

#### 2. The Norming Equation
To solve for the individual probabilities ($p_0, p_1, p_2, p_3$), the balance equations are combined with the **Norming Equation**:
*   **Definition**: It states that the sum of the probabilities of all possible mutually exclusive states must equal 1 (100% probability).

#### 3. Analytical Conclusion
*   **System of Equations**: By substituting the balance equations ($p_1 = \frac{\lambda}{\mu}p_0$, etc.) into the norming equation, the idle probability $p_0$ can be isolated and calculated.
*   **Steady-State Solution**: This represents the final step required to determine the long-term performance measures of the workstation, such as average WIP and Throughput.
  
$$
\lambda p _ {2} = \mu p _ {3}
$$

Norming equation

$$
\sum_ {n = 0} ^ {3} p _ {n} = 1.
$$

# Solution

$$
p _ {1} = \left(\frac {\lambda}{\mu}\right) p _ {0}, \quad p _ {2} = \left(\frac {\lambda}{\mu}\right) ^ {2} p _ {0}, \quad p _ {3} = \left(\frac {\lambda}{\mu}\right) ^ {3} p _ {0}
$$

$$
p _ {0} = \left[ 1 + \frac {\lambda}{\mu} + \left(\frac {\lambda}{\mu}\right) ^ {2} + \left(\frac {\lambda}{\mu}\right) \right] ^ {- 1}
$$

$$
(p _ {0}, p _ {1}, p _ {2}, p _ {3}) = (0. 1 7 3, 0. 2 1 7, 0. 2 7 1, 0. 3 3 9)
$$

# Comments

> The server is idle when the system is empty, so the percentage of server idle time is 17.3%.   
The probability of having 1 item in the system is p1: 21.7%   
The probability of having 2 items in the system is pz: 27.1%   
The probability of having 3 items in the system is p3: 33.9%

$$
W I P = E [ N ] = \sum n p _ {n} = 1 \times 0. 2 1 7 + 2 \times 0. 2 7 1 + 3 \times 0. 3 3 9 = 1. 7 7 6 \text {j o b s}
$$

# Comments

> The number of lost jobs per hour (i.e., those arriving to a full system) is given by λxp= 5x0.339 = 1.695.   
Throughput is equal to the number of jobs that enter the system per unit time (those jobs that actually get into the system,called the effective arrival rate).   
Thus, throughput rate equals the arrival rate minus the loss rate; namely,5 - 1.695= 3.305 jobs/day.

$$
C T = W I P / t h = W I P / \left(\lambda \left(1 - p _ {3}\right)\right) = 1. 7 7 6 / 3. 3 0 5 = 0. 5 3 7 \text {d a y s}
$$

# Effective arrival rate

> Whenever the system is finite, there is the possibility that the system will be full and arriving jobs will be lost; hence, the actual rate of jobs that enter the system, ∧e may not be the same as the arrival rate, λ.   
V The effective arrival rate for a system is te rate at which jobs enter the system. For a workstation with constant arrival rate, ^,and with a maximum number of jobs at the workstation limited to nmax, the effective arrival rate is given by

$$
\lambda_ {e} = \lambda (1 - p _ {n _ {\max}})
$$

where Pnmax is the probability that the workstation is full.

V A system at steady-state willhave its system throughput rate equal to the effective arrival rate; that is, th =λe, and the use of Little's Law must always use λe and not λ for the throughput.

# Queuing Systems

> Queues Theory: development of models to study the waiting phenomena which appears in presence of a service demand   
Applications

Customers waiting at the bank or at the post office   
Patients waiting for the doctor   
People waiting for a taxi   
Parts waiting to be processed by a machine

Defined in 1917 by Erlang and applied in telephonic sector

# A queuing systems includes:

# 1. An arrival process

Single jobs or batches   
Deterministic or stochastic arrival times

# 2. A production/service process

Single or parallel machines   
Deterministic or stochastic process times

# 3. A queue

FCFS (First Come First Served),LCFS (Last Come First Served), SIRIO (Service In Random Order),....   
Limited or illimited length

### Visual Diagram: Fundamental Components of a Queuing System
- **Component Type**: Process flow diagram.
- **Logic**: Defines the basic architectural elements and flow of a standard queuing model, illustrating the transition from a source population to service completion.

#### 1. Population (Calling Source)
*   **Role**: Represents the pool of potential customers or jobs that can enter the system.
*   **Cycle**: The diagram illustrates a closed-loop flow where completed items (Output) return to the source population.

#### 2. Arrival Process
*   **Action**: The arrow labeled "Arrival" indicates items leaving the population to enter the workstation.
*   **Modeling**: This is the first element defined in queuing theory (e.g., in Kendall notation), usually characterized by an inter-arrival time distribution.

#### 3. The Queue
*   **Visual Representation**: Depicted as a series of vertical slots within a horizontal buffer.
*   **Purpose**: A waiting area for items when the service node is occupied. Key parameters include its capacity (limited or unlimited) and its discipline (e.g., FCFS - First Come First Served).

#### 4. Service Node
*   **Visual Representation**: A circle representing the server or workstation.
*   **Operation**: The stage where the actual processing or service takes place, defined by a specific service time distribution ($\mu$).

#### 5. Output
*   **Action**: The final arrow represents the completion of the service and the departure of the item from the workstation area.


# Kendall Notation

List of characters separated by a “/"   
First element: inter-arrival time distribution   
Second element: service time distribution   
V Third element: number of servers   
V Fourth element: maximum number of jobs allowed in the system at one time   
Optional fifth element: queueing discipline

/ maximum arrival service number queue (process/process of servers possible discipline in system

Example: M/M/1/3

# Commonly used abbreviations

### Visual Diagram: Kendall Notation Symbols and Abbreviations
- **Component Type**: Reference table for shorthand notation.
- **Logic**: Defines the standard symbols used in Kendall's notation to categorize queuing systems based on arrival/service distributions, capacity, and queue discipline.

#### 1. Distribution Symbols (First & Second Elements)
*   **M**: Exponential (Markov) distribution for inter-arrival or service times.
*   **D**: Deterministic (constant) inter-arrival or service times.
*   **$E_k$**: Erlang type $k$ distribution.
*   **G**: General distribution (any probability law).

#### 2. Numerical Parameters (Third & Fourth Elements)
*   **1, 2, ..., $\infty$**: Indicates the number of parallel servers or the maximum allowed capacity in the system.
*   **Note**: Most often the fourth parameter is omitted when it is not finite (e.g., M/M/1 instead of M/M/1/$\infty$).

#### 3. Queue Disciplines (Optional Fifth Element)
*   **FIFO**: First In, First Out.
*   **LIFO**: Last In, First Out.
*   **SIRO**: Service In Random Order.
*   **PRI**: Priority queue discipline.
*   **GD**: General queue discipline.

V If the system has no effective limit on the number of jobs allowed, then the fourth parameter would be infinity. Most often the fourth parameter is omitted when it is not finite, so that such a model would often be written as M/M/1 instead of M/M/1/.

# Infinite Capacity Model (M/M/1)

Exponential distribution of arrival times   
Exponential distribution of processing times   
One machine in the server   
Queue of unlimited dimension (it can be omitted)

### Visual Diagram: State-Transition Network for Infinite Capacity System (M/M/1)
- **Component Type**: Infinite state-transition diagram (Markov chain).
- **Logic**: Illustrates the state space and transition flows for a single-server queuing system with no physical limit on the queue length.

#### 1. Infinite State Space
*   **The Ellipsis (...)**: Unlike the finite model, the nodes extend from 0, 1, 2, 3 towards infinity, represented by the ellipsis. This reflects the assumption that the system can accommodate an unlimited number of waiting jobs.

#### 2. Constant Transition Rates
*   **Arrival Rate ($\lambda$)**: The forward transition rate remains constant for every state. New jobs continue to arrive at the same rate regardless of how long the queue is.
*   **Service Rate ($\mu$)**: The backward transition rate also remains constant for every state above zero. Because there is only one server (M/M/1), the processing speed does not increase when the queue gets longer.

#### 3. Analytical Implication
*   **Infinite Equations**: This open-ended network generates an infinite sequence of balance equations (e.g., $\lambda p_n = \mu p_{n+1}$).
*   **Mathematical Resolution**: To find the steady-state probabilities ($p_n$), this infinite system requires the use of successive substitution and the properties of geometric series, converging to a solution only if the utilization factor ($u = \lambda/\mu$) is strictly less than 1.

# Infinite Capacity Model (M/M/1)

> An infinite system of equations exists

$$
\lambda p _ {0} = \mu p _ {1}
$$

$$
\lambda p _ {1} = \mu p _ {2}
$$

$$
\lambda p _ {2} = \mu p _ {3}
$$

$$
\lambda p _ {n} = \mu p _ {n + 1}
$$

$$
\sum_ {n = 0} ^ {\infty} p _ {n} = 1.
$$

->

$$
{p _ {1}} {= \frac {\lambda}{\mu} p _ {0}}
$$

$$
p _ {2} = \frac {\lambda}{\mu} p _ {1}
$$

$$
p _ {3} = \frac {\lambda}{\mu} p _ {2}
$$

$$
p _ {n} = \frac {\lambda}{\mu} p _ {n - 1}
$$

# Infinite Capacity Model (M/M/1)

Using a successive substitution procedure,each pn term can be written as a function of Po

$$
p _ {n} = \left(\frac {\lambda}{\mu}\right) ^ {n} p _ {0} \text {f o r} n = 0, 1, \dots
$$

By substituting in the norming equation:

$$
p _ {0} + \left(\frac {\lambda}{\mu}\right) p _ {0} + \left(\frac {\lambda}{\mu}\right) ^ {2} p _ {0} + \dots + \left(\frac {\lambda}{\mu}\right) ^ {n} p _ {0} + \dots = 1
$$

->

$$
p _ {0} = \frac {1}{\left(1 + \frac {\lambda}{\mu} + \left(\frac {\lambda}{\mu}\right) ^ {2} + \cdots + \left(\frac {\lambda}{\mu}\right) ^ {n} + \cdots\right)}
$$

# Infinite Capacity Model (M/M/1)

Remembering the property of a geometric series:

$$
\sum_ {n = 0} ^ {\infty} r ^ {n} = 1 / (1 - r) \text {f o r} | r | <   1
$$

V The denominator is a geometric series that has a finite value if Vu<1, thus

$$
p _ {0} = 1 - \frac {\lambda}{\mu}
$$

The general solution to the steady-state probabilities is

$$
p _ {n} = \left(1 - \frac {\lambda}{\mu}\right) \left(\frac {\lambda}{\mu}\right) ^ {n} \text {f o r} n = 0, 1, \dots
$$

# Infinite Capacity Model (M/M/1)

V Computation of the expected number of jobs in the system (WIP)

$$
\begin{array}{l} W I P _ {s} = E [ N ] = \sum_ {n = 0} ^ {\infty} n p _ {n} = \sum_ {n = 0} ^ {\infty} n \left(1 - \frac {\lambda}{\mu}\right) \left(\frac {\lambda}{\mu}\right) ^ {n} \\ = \left(1 - \frac {\lambda}{\mu}\right) \left(\frac {\lambda}{\mu}\right) \sum_ {n = 1} ^ {\infty} n \left(\frac {\lambda}{\mu}\right) ^ {n - 1} \\ = \left(1 - \frac {\lambda}{\mu}\right) \left(\frac {\lambda}{\mu}\right) \overbrace {\left(\frac {1}{1 - \frac {\lambda}{\mu}}\right) ^ {2}} \\ = \frac {\left(1 - \frac {\lambda}{\mu}\right) \left(\frac {\lambda}{\mu}\right)}{\left(1 - \frac {\lambda}{\mu}\right) ^ {2}} = \frac {\left(\frac {\lambda}{\mu}\right)}{\left(1 - \frac {\lambda}{\mu}\right)} = \frac {u}{1 - u} \\ \end{array}
$$

Utilization factor (u)

$$
\boxed {\sum_ {n = 1} ^ {\infty} n r ^ {n - 1} = 1 / (1 - r) ^ {2} \text {f o r} | r | <   1}
$$

# Infinite Capacity Model (M/M/1)

> Using Little's Law, the expected time in system (the cycle time) CTs is given by:

$$
C T _ {s} = \frac {W I P _ {s}}{\lambda} = \frac {1}{\lambda} \frac {\frac {\lambda}{\mu}}{(1 - \frac {\lambda}{\mu})} = \frac {1}{\mu - \lambda}
$$

# Example

Consider a single server system with exponentially-distributed interarrival times and exponentially-distributed service times.

4 jobs per hour arrive for service and the mean service time is 1/5 hour.

Compute the WS performance measures

# Data

λ = 4 jobs/hr (=TH)   
μ = 5 jobs/hr → E[Ts]= 1/5 hr = 0.2 hr

# Solution

u = =4/5 =0.8 μ   
WIPs = u 0.8 = 4 jobs 1-u 1-0.8   
CTs = WIPs = 4/4 = 1 hr TH   
CTq = CTs-E[Ts] = 1 - 0.2= 0.8 hr

# Solution

Probability that the server is idle: po= 1-u = 0.2   
> Probability of having 1 item in the system: p,= u*(1-u)= 0.8*0.2 = 0.16   
> Probability of having 2 item in the system: P2= u2*(1-u) = 0.82*0.2 = 0,128   
> Probability of having 3item in the system: p3 = u3*(1-u)= 0.83*0.2 = 0.1024   
  
> Probability of having n item in the system: Pn = un*(1-u) = 0.8n*0.2

# Exercise

V Consider a M/M/1 system with the following parameters:

>λ = 2,875 jobs/hr   
>μ = 3 jobs/hr -> E[Ts] = 1/3 = 0.333 hr

> What is the utilization factor of the WS?   
What is the probability that there are no jobs at the WS?   
> What is the average number of jobs lost per hour?   
> What is the average throughput rate per hour?   
What is the average WIP?   
What is the average CT in hours?   
What are the average CTq (in hours) and WIPq?

# Solution

u = =2.875/3=0.958   
> Probability that there are no jobs in the WS: po= 1-u = 1-0.958 = 0.042   
Number of jobs lost = O,because the queue is unlimited   
TH=λ =2.875 jobs/hr   
WIP =1= 22.81 jobs   
CT = WP = 23/2.875 = 7.934 hrs   
? CTq = CT - E[Ts] = 7.934 -0.333 = 7.6 hrs   
WIPq = TH · CTq = 21.85 jobs

# M/M/1 - Summary of Performance Measures

Work In Process:

$$
W I P _ {s} = \frac {u}{1 - u}
$$

Cycle Time:

$$
C T _ {\mathrm {s}} = \frac {W I P _ {\mathrm {s}}}{\lambda} = \frac {1}{\lambda} \frac {\frac {\lambda}{\mu}}{(1 - \frac {\lambda}{\mu})} = \frac {1}{\mu - \lambda}
$$

Queue Cycle Time:

$$
C T _ {q} = \frac {u}{1 - u} E [ T _ {s} ]
$$

Moreover:

$$
\mathrm {T H} = \lambda
$$

V Queue Work In Process:

$$
W I P _ {q} = \frac {u ^ {2}}{1 - u}
$$

$$
u = \lambda / \mu <   1
$$

> Performance measures increase as u and E[Ts] increase, and tend to infinity as u → 1

# Infinite Capacity Model (M/M/c)

> In most models,it is usually assumed that allthe machines are identical and jobs are not split,but processed completely on one machine.   
> If one machine operates at a rate of μ, then c machines operate at a rate of cu ，and the state diagram must be adjusted accordingly.   
For example, suppose a workstation has three machines, then the service rate when two machines are busy is 2μ and whenever all machines are busy the service rate is 3μ; thus, the rate diagram is as below. 入 2 入

### Visual Diagram: State-Transition Network for Multiple Servers (M/M/c)
- **Component Type**: Infinite state-transition diagram for a multi-server system.
- **Logic**: Illustrates the transition flows for a queuing system with infinite capacity and multiple parallel servers, specifically modeling an M/M/3 system (where $c=3$).

#### 1. Constant Arrival Dynamics
*   **Arrival Rate ($\lambda$)**: The forward transition rate remains constant for every state. New jobs arrive at the same rate regardless of how many items are in the system or how many servers are busy.

#### 2. Variable Service Rates (The Multi-Server Effect)
Unlike the single-server model, the backward transition rates (service completions) scale dynamically with the number of active servers:
*   **Partial Load (States 1 & 2)**: When there are fewer jobs than servers ($n < c$), the service rate is $n\mu$. For example, moving from state 2 to 1 happens at a rate of **$2\mu$** because two servers are working simultaneously.
*   **Full Capacity (States $\ge 3$)**: Once the system reaches state 3, all three servers are occupied. The total service rate caps at **$3\mu$**. Any state beyond 3 (represented by the ellipsis) will also return at a rate of $3\mu$ because the maximum processing capacity has been reached and the excess items are waiting in the queue.

#### 3. Analytical Implication
*   **Piecewise Balance Equations**: This structure requires a two-part approach to defining the balance equations and calculating steady-state probabilities. The mathematical logic changes depending on whether the system is partially loaded ($n < c$) or fully saturated with a queue forming ($n \ge c$).

# Infinite Capacity Model (M/M/c)

$$
C T _ {q} (M / M / c) = \left(\frac {u ^ {\sqrt {2 c + 2} - 2}}{c}\right) C T _ {q} (M / M / 1)
$$

$$
C T _ {q} (M / M / c) = \frac {u ^ {\sqrt {2 (c + 1)} - 1}}{c (1 - u)} E [ T s ]
$$

> When c=1, the formula is equal to the M/M/1 case

# Non-identical service rates

> Workstation with two machines with non-identical service rate   
> If a job arrives to the system and finds that only one machine is busy, the job is assigned to the idle machine regardless of the speed of the machine   
V Once a job is assigned to a machine for processing, it remains on that machine until its processing is complete   
> Inter-arrival times exponentially distributed with a mean arrival rate of λ   
> Mean service rates of μ and γ for the two distinct machines

Y<μ, the μ machine is faster

Limit of four jobs in the system at one time

# Example M/M/2/4

Nmax = 4   
> Possible number of states are nmax + 2 → {0, 1f, 1s,2,3,4}   
> n=1f: one job in the system in the faster machine   
V n=1s: one job in the system in the slower machine

### Visual Diagram: State-Transition Network for Parallel Tasks and Finite Capacity
- **Component Type**: Continuous-Time Markov Chain (CTMC) / State-transition diagram.
- **Logic**: Models a queuing system with a finite capacity ($N=4$) and a server that performs two independent tasks in parallel for each job.

#### 1. State Space Definitions
The system consists of six discrete states based on the number of jobs present and the completion status of the parallel tasks:
*   **State 0**: The system is idle (empty).
*   **States 1f and 1s**: The system contains 1 job. The suffixes "f" and "s" denote which of the two parallel tasks is still pending.
*   **States 2, 3, 4**: The system contains 2, 3, or 4 jobs respectively. State 4 is the **maximum capacity**; any further arrivals are blocked and lost.

#### 2. Transition Rate Dynamics
*   **Arrival Rate ($\lambda$)**: Represents new jobs entering the system, moving the state to the right (e.g., $0 \to 1f$ or $2 \to 3$).
*   **Service Rates ($\mu, \gamma$)**: Represent the completion rates of two distinct internal tasks (Task A and Task B) required to process a single job.

#### 3. Parallel Service Logic
This model captures a workstation where each job requires two operations that can be performed simultaneously:
*   **Parallel Processing ($n \ge 2$)**: When 2 or more jobs are present, the server works on both tasks ($\mu$ and $\gamma$) at the same time for the job at the head of the queue. If either task finishes, the system moves to a lower state. The return rate from states 3 and 4 is the sum **$(\gamma + \mu)$**.
*   **The State 1 Split**: When only one job remains (transitioning from state 2), the system enters a specific state based on which task finished first:
    *   If task $\gamma$ finished first, the system enters **1f** (where only task $\mu$ remains to be completed).
    *   If task $\mu$ finished first, the system enters **1s** (where only task $\gamma$ remains to be completed).
*   **Re-entry**: If a new arrival ($\lambda$) occurs while the system is in 1f or 1s, it returns to state 2, where both parallel processes resume.

#### 4. Analytical Application
*   **Steady-State Balance**: This diagram is used to establish the global balance equations (e.g., the flow out of state 0, $\lambda p_0$, must equal the flow into state 0, $\mu p_{1f} + \gamma p_{1s}$).
*   **Performance Metrics**: Essential for calculating the blocking probability ($p_4$), effective throughput ($\lambda_{eff}$), and the average Work-In-Process (WIP).

Cutting the graph

### Visual Diagram: State Partitioning for Idle State Balance
- **Component Type**: Partitioned state-transition diagram.
- **Logic**: Isolates the idle state (0) from the rest of the state space to establish flow equilibrium between being empty and having at least one job in the system.

#### 1. Subset Definition
The diagram highlights two distinct subsets via dashed blue lines:
*   **Subset A (Left)**: Contains only **State 0** (system empty).
*   **Subset B (Right)**: Encompasses the active states **{1f, 1s, 2, 3, 4}**.

#### 2. Flow Equilibrium Across the Boundary
In steady-state, the flow exiting Subset A must equal the flow entering it from Subset B:
*   **Outward Flow (0 to B)**: An arrival ($\lambda$) occurs while the system is in state 0. Rate: $\lambda p_0$.
*   **Inward Flow (B to 0)**: Final service completions returning the system to idle:
    *   Task $\mu$ completion from state 1f (rate $\mu p_{1f}$).
    *   Task $\gamma$ completion from state 1s (rate $\gamma p_{1s}$).

#### 3. Resulting Balance Equation
The equality of flows yields:
$$ \lambda p_0 = \mu p_{1f} + \gamma p_{1s} $$

#### 4. Analytical Role
This partition is essential for isolating the idle probability ($p_0$). It serves as the foundation for the recursive calculation of all subsequent state probabilities ($p_n$), leading to the final determination of system throughput and average WIP.

$$
\lambda p _ {0} = \mu p _ {1 \mathrm {f}} + \gamma p _ {1 \mathrm {s}}
$$

$$
\lambda p _ {1 \mathrm {f}} = \gamma p _ {2} + \gamma p _ {1 \mathrm {S}}
$$

$$
\lambda p _ {1 \mathrm {f}} + \lambda p _ {1 \mathrm {S}} = (\gamma + \mu) p _ {2}
$$

$$
\lambda p _ {2} = (\gamma + \mu) p _ {3}
$$

$$
\lambda p _ {3} = (\gamma + \mu) p _ {4}
$$

$$
p _ {0} + p _ {1 \mathrm {f}} + p _ {1 \mathrm {S}} + p _ {2} + p _ {3} + p _ {4} = 1
$$

# Example M/M/2/4

Cutting the graph

### Visual Diagram: Partitioning for State Subset Balance
- **Component Type**: Partitioned state-transition diagram.
- **Logic**: Illustrates the application of the "cut" method to a complex state-transition diagram, isolating specific groups of states to derive local balance equations.

---

#### 1. Subset Definitions
The diagram defines two disjoint subsets using dashed blue circles:
*   **Subset Left**: Contains nodes **0** and **1f** (representing an empty system or a system where only task $\mu$ remains).
*   **Subset Right**: Contains nodes **1s**, **2**, **3**, and **4** (representing states where task $\gamma$ is active or multiple jobs are present).

#### 2. Flow Dynamics Across the Cut
For the system to be in equilibrium, the total probability flow exiting the left subset must equal the flow entering it from the right:
*   **Flow Out (Left to Right)**: A single transition occurs from **state 1f to state 2** due to an arrival at rate **$\lambda$**. The total flow rate is defined as $\lambda p_{1f}$.
*   **Flow In (Right to Left)**: Two distinct transitions return the system to the left subset:
    *   Completion of the parallel task $\gamma$ from **state 2 to state 1f**.
    *   Completion of the parallel task $\gamma$ from **state 1s to state 0**.

#### 3. Derived Balance Equation
Equating these crossing flows results in the following balance equation:
$$ \lambda p_{1f} = \gamma p_2 + \gamma p_{1s} $$

#### 4. Analytical Significance
This partition is a fundamental step in solving the parallel task model. By isolating these subsets, we can relate the probabilities of having one job in a specific phase ($1f$ or $1s$) to the probability of having two jobs ($p_2$), allowing us to eventually solve the entire system via the norming equation.

$$
\lambda p _ {0} = \mu p _ {1 \mathrm {f}} + \gamma p _ {1 \mathrm {S}}
$$

$$
\lambda p _ {1 \mathrm {f}} = \gamma p _ {2} + \gamma p _ {1 \mathrm {S}}
$$

$$
\lambda p _ {1 \mathrm {f}} + \lambda p _ {1 \mathrm {S}} = (\gamma + \mu) p _ {2}
$$

$$
\lambda p _ {2} = (\gamma + \mu) p _ {3}
$$

$$
\lambda p _ {3} = (\gamma + \mu) p _ {4}
$$

$$
p _ {0} + p _ {1 \mathrm {f}} + p _ {1 \mathrm {S}} + p _ {2} + p _ {3} + p _ {4} = 1
$$

# Example M/M/2/4

Cutting the graph

### Visual Diagram: Partitioning for State Subset Balance
- **Component Type**: Partitioned state-transition diagram.
- **Logic**: Illustrates the application of the "cut" method to a complex state-transition diagram, isolating specific groups of states to derive local balance equations.

#### 1. Subset Definitions
The diagram defines two disjoint subsets using dashed blue circles:
*   **Subset Left**: Contains nodes **0** and **1f** (representing an empty system or a system where only task $\mu$ remains).
*   **Subset Right**: Contains nodes **1s**, **2**, **3**, and **4** (representing states where task $\gamma$ is active or multiple jobs are present).

#### 2. Flow Dynamics Across the Cut
For the system to be in equilibrium, the total probability flow exiting the left subset must equal the flow entering it from the right:
*   **Flow Out (Left to Right)**: A single transition occurs from **state 1f to state 2** due to an arrival at rate **$\lambda$**. The total flow rate is defined as $\lambda p_{1f}$.
*   **Flow In (Right to Left)**: Two distinct transitions return the system to the left subset:
    *   Completion of the parallel task $\gamma$ from **state 2 to state 1f** (rate $\gamma p_2$).
    *   Completion of the parallel task $\gamma$ from **state 1s to state 0** (rate $\gamma p_{1s}$).

#### 3. Derived Balance Equation
Equating these crossing flows results in the following balance equation:
$$ \lambda p_{1f} = \gamma p_2 + \gamma p_{1s} $$

#### 4. Analytical Significance
This partition is a fundamental step in solving the parallel task model. By isolating these subsets, we can relate the probabilities of having one job in a specific phase ($1f$ or $1s$) to the probability of having two jobs ($p_2$), allowing for the recursive resolution of the entire state probability distribution.

$$
\lambda p _ {0} = \mu p _ {1 \mathrm {f}} + \gamma p _ {1 \mathrm {s}}
$$

$$
\lambda p _ {1 \mathrm {f}} = \gamma p _ {2} + \gamma p _ {1 \mathrm {S}}
$$

$$
\lambda p _ {1 \mathrm {f}} + \lambda p _ {1 \mathrm {S}} = (\gamma + \mu) p _ {2}
$$

$$
\lambda p _ {2} = (\gamma + \mu) p _ {3}
$$

$$
\lambda p _ {3} = (\gamma + \mu) p _ {4}
$$

$$
p _ {0} + p _ {1 \mathrm {f}} + p _ {1 \mathrm {S}} + p _ {2} + p _ {3} + p _ {4} = 1
$$

# Example M/M/2/4

Cutting the graph

### Visual Diagram: Partitioning for High Congestion States
- **Component Type**: Partitioned state-transition diagram.
- **Logic**: Isolates the states representing higher congestion (3 or more jobs) to define the balance between moderate work-in-process and near-capacity conditions.

#### 1. Subset Definitions
The diagram defines two disjoint subsets using dashed blue circles:
*   **Subset Left**: Includes states **{0, 1f, 1s, 2}**.
*   **Subset Right**: Includes states **{3, 4}**.

#### 2. Flow Dynamics Across the Cut
For the system to be in equilibrium, the total probability flow exiting the left subset must equal the flow entering it from the right:
*   **Flow Out (Left to Right)**: An arrival ($\lambda$) occurs while the system is in state 2, moving it to state 3. Rate: $\lambda p_2$.
*   **Flow In (Right to Left)**: The completion of parallel service (sum of rates $\gamma + \mu$) while the system is in state 3, returning it to state 2. Rate: $(\gamma + \mu) p_3$.

#### 3. Derived Balance Equation
Equating these crossing flows results in the following balance equation:
$$ \lambda p_2 = (\gamma + \mu) p_3 $$

#### 4. Analytical Significance
This partition establishes the mathematical relationship between the probabilities of the system being "busy" (2 jobs) versus "congested" (3 jobs). It is a critical step in calculating the stationary distribution for the system, which allows for the final determination of the blocking probability at state 4.

$$
\lambda p _ {0} = \mu p _ {1 \mathrm {f}} + \gamma p _ {1 \mathrm {S}}
$$

$$
\lambda p _ {1 \mathrm {f}} = \gamma p _ {2} + \gamma p _ {1 \mathrm {s}}
$$

$$
\lambda p _ {1 \mathrm {f}} + \lambda p _ {1 \mathrm {S}} = (\gamma + \mu) p _ {2}
$$

$$
\lambda p _ {2} = (\gamma + \mu) p _ {3}
$$

$$
\lambda p _ {3} = (\gamma + \mu) p _ {4}
$$

$$
p _ {0} + p _ {1 \mathrm {f}} + p _ {1 \mathrm {S}} + p _ {2} + p _ {3} + p _ {4} = 1
$$

# Example M/M/2/4

Cutting the graph

### Visual Diagram: Partitioning for the Blocking State Balance
- **Component Type**: Partitioned state-transition diagram.
- **Logic**: Isolates the blocking state (4) from the rest of the system to establish flow equilibrium at the capacity limit.

#### 1. Subset Definitions
The diagram defines two disjoint subsets using dashed blue circles:
*   **Subset Left**: Includes states **{0, 1f, 1s, 2, 3}**.
*   **Subset Right**: Includes only **State 4** (system full).

#### 2. Flow Dynamics Across the Cut
For the system to be in equilibrium, the total probability flow exiting the left subset must equal the flow entering it from the right:
*   **Flow Out (Left to Right)**: An arrival ($\lambda$) occurs while the system is in state 3, moving it to the full state (4). Rate: $\lambda p_3$.
*   **Flow In (Right to Left)**: The completion of parallel service (sum of rates $\gamma + \mu$) while the system is in state 4, returning it to state 3. Rate: $(\gamma + \mu) p_4$.

#### 3. Derived Balance Equation
Equating these crossing flows results in the following balance equation:
$$ \lambda p_3 = (\gamma + \mu) p_4 $$

#### 4. Analytical Significance
This partition is critical for calculating the **Blocking Probability ($p_4$)**. This value is used to determine the effective arrival rate and the service level of the workstation, as any job arriving in state 4 is rejected by the system.

$$
\lambda p _ {0} = \mu p _ {1 \mathrm {f}} + \gamma p _ {1 \mathrm {S}}
$$

$$
\lambda p _ {1 \mathrm {f}} = \gamma p _ {2} + \gamma p _ {1 \mathrm {s}}
$$

$$
\begin{array}{l} \lambda p _ {1 \mathrm {f}} + \lambda p _ {1 \mathrm {S}} = (\gamma + \mu) p _ {2} \\ \lambda p _ {2} = (\gamma + \mu) p _ {3} \\ \lambda p _ {3} = (\gamma + \mu) p _ {4} \\ \end{array}
$$

$$
p _ {0} + p _ {1 \mathrm {f}} + p _ {1 \mathrm {S}} + p _ {2} + p _ {3} + p _ {4} = 1
$$

# Example M/M/2/4

Norming equation

### Visual Diagram: State-Transition Network for Parallel Tasks and Finite Capacity
- **Component Type**: Continuous-Time Markov Chain (CTMC) / State-transition diagram.
- **Logic**: Models a queuing system with a finite capacity ($N=4$) and a server that performs two independent tasks in parallel for each job.

---

#### 1. State Space Definitions
The system consists of six discrete states based on the number of jobs present and the completion status of the parallel tasks:
*   **State 0**: The system is idle (empty).
*   **States 1f and 1s**: The system contains 1 job. These states distinguish which of the two parallel tasks is still pending completion.
*   **States 2, 3, 4**: The system contains 2, 3, or 4 jobs respectively. State 4 represents the **maximum capacity**; arrivals occurring in this state are blocked.

#### 2. Transition Rate Dynamics
*   **Arrival Rate ($\lambda$)**: Represents new jobs entering the system, moving the state from left to right (e.g., $0 \to 1f$ or $2 \to 3$).
*   **Service Rates ($\mu, \gamma$)**: Represent the completion rates of two distinct tasks (e.g., Task A and Task B) required for each job.

#### 3. Parallel Service Logic
This model captures a workstation where each job requires two operations that are performed simultaneously:
*   **Parallel Processing ($n \ge 2$)**: When 2 or more jobs are present, the server works on both tasks ($\mu$ and $\gamma$) at the same time for the job in service. Completing either task moves the system to a lower state. Thus, the total service rate from states 3 and 4 is the sum **$(\gamma + \mu)$**.
*   **The State 1 Split**: When the system transitions from state 2 (having completed one task), it enters a specific state based on which task finished first:
    *   If task $\gamma$ finished first, the system enters **1f** (where only task $\mu$ remains).
    *   If task $\mu$ finished first, the system enters **1s** (where only task $\gamma$ remains).
*   **Re-entry**: An arrival ($\lambda$) during states 1f or 1s returns the system to state 2, where both parallel tasks resume.

#### 4. Analytical Application
*   **Global Balance Equations**: This diagram is the foundation for establishing balance equations (e.g., $\lambda p_0 = \mu p_{1f} + \gamma p_{1s}$) to solve for steady-state probabilities.
*   **Performance Metrics**: Used to calculate the **Blocking Probability ($p_4$)**, effective throughput, and the average number of jobs in the system (WIP).
$$
\lambda p _ {0} = \mu p _ {1 \mathrm {f}} + \gamma p _ {1 \mathrm {S}}
$$

$$
\lambda p _ {1 \mathrm {f}} = \gamma p _ {2} + \gamma p _ {1 \mathrm {S}}
$$

$$
\begin{array}{l} \lambda p _ {1 \mathrm {f}} + \lambda p _ {1 \mathrm {S}} = (\gamma + \mu) p _ {2} \\ \lambda p _ {2} = (\gamma + \mu) p _ {3} \\ \lambda p _ {3} = (\gamma + \mu) p _ {4} \\ \end{array}
$$

$$
p _ {0} + p _ {1 \mathrm {f}} + p _ {1 \mathrm {S}} + p _ {2} + p _ {3} + p _ {4} = 1
$$

# Numerical example

An overhaul facility for helicopters is open 24 hours a day, seven days a week and helicopters arrive to the facility at an average rate of 3 per day according to a Poisson process (i.e., exponential inter-arrival times).

One of the areas within the facility is for degreasing one of the major components.There is only room in the facility for 4 jobs at any one time and there are two machines that do the degreasing.

The newer of the two degreasing machines takes an average of 8 hours to complete the degreasing and the older machine takes 12 hours for the degreasing operation. Because of the large variability in helicopter conditions,al times are exponentially distributed.

Thus, we have λ = 3 per day, μ = 3 per day,and γ = 2 per day.

# Solution

$$
3 p _ {0} - 3 p _ {1 \mathrm {f}} - 2 p _ {1 \mathrm {S}} = 0
$$

$$
3 p _ {1 \mathrm {f}} - 2 p _ {2} - 2 p _ {1 \mathrm {s}} = 0
$$

$$
3 p _ {1 \mathrm {f}} + 3 p _ {1 \mathrm {s}} - 5 p _ {2} = 0
$$

$$
3 p _ {2} - 5 p _ {3} = 0
$$

$$
3 p _ {3} - 5 p _ {4} = 0
$$

$$
p _ {0} + p _ {\mathrm {l f}} + p _ {\mathrm {1 S}} + p _ {2} + p _ {3} + p _ {4} = 1.
$$

V The solution of this system equation is:

$$
p _ {0} = 0. 2 8 8, p _ {1 \mathrm {f}} = 0. 2 0 9, p _ {1 \mathrm {S}} = 0. 1 1 8, p _ {2} = 0. 1 9 6, p _ {3} = 0. 1 1 8, p _ {4} = 0. 0 7 1
$$

# Solution

Average number of jobs in the system:

$$
W I P s = p _ {1 f} + p _ {1 s} + 2 p _ {2} + 3 p _ {3} + 4 p _ {4} = 1. 3 5 6
$$

> Average number of jobs in the queue:

$$
\mathsf {W I P q} = \mathsf {p} _ {3} + 2 \mathsf {p} _ {4} = 0. 2 5 9
$$

The average cycle times are:

$$
\mathrm {C T s} = \frac {W I P S}{\lambda e} = \left(\frac {1 . 3 5 6}{3 * (1 - 0 . 0 7 1)}\right) = 0. 4 8 6 \mathrm {d a y}
$$

$$
\mathrm {C T q} = \frac {W I P q}{\lambda e} = \left(\frac {0 . 2 5 9}{3 * (1 - 0 . 0 7 1)}\right) = 0. 0 9 3 \mathrm {d a y}
$$

# Solution

Because of the preference given to using the faster machine, we would expect the average time of processing of the workstation to be closer to 8 hours than to 12 hours   
> To get an exact value, we take advantage of the fact that the time in the system equals the time in the queue plus service time

$$
E [ T ] = C T _ {s} - C T _ {q} = 0. 4 8 6 - 0. 0 9 3 = 0. 3 9 3 \mathrm {d a y s} = 9. 4 \mathrm {h r}
$$

# Solution

V Other measures that are sometimes desired by the management   
Expected number of busy servers E[BS]

$$
E [ B S ] = 1 p _ {1 \mathrm {f}} + 1 p _ {1 \mathrm {S}} + 2 p _ {2} + 2 P _ {3} + 2 p _ {4} = 1. 0 9 7
$$

>System utilization factor (u),i.e., the expected number of busy servers divided by the number of machines available

$$
u = \frac{E[BS]}{2} = 0.5485 = 54.85\%
$$

# Exercise

> By analyzing the reported simulation model (two servers with non identical service rate and max wip of 4),find the following parameters:

>Arrival rate (^), processing rate of faster (μ) and slower (Y) machine   
>Probability that a job is rejected   
>Utilization of the workstation

### Simulation Interface: System Layout and Performance Dashboard
- **Component Type**: Discrete-Event Simulation (DES) interface (FlexSim).
- **Logic**: Represents a parallel workstation configuration with differentiated processing speeds and a real-time performance tracking dashboard.

---

#### 1. Model Layout (3D View)
The left panel illustrates the physical material flow within the system:
*   **Source1**: The entry point for entities (jobs) into the simulation.
*   **Queue1**: A central buffer where jobs wait before being dispatched to the next available resource.
*   **Parallel Processors**: 
    *   **FASTER**: The upper workstation, characterized by a higher processing speed.
    *   **SLOWER**: The lower workstation, characterized by a lower processing speed.
*   **Sink1 & Sink2**: Departure points. Sink1 collects finished products from both processors, while Sink2 handles a secondary flow (potentially scrap or bypassed units) directly from the source.

---

#### 2. Performance Dashboard (KPIs)
The right panel displays metrics collected over a total simulation run time of **761,602.03 units**.

**A. State (Resource Utilization)**
Visualizes the percentage of time machines spend in the *Processing* state versus the *Idle* state.
| Object | Utilization (Processing) |
| :--- | :--- |
| **FASTER** | 36.48% |
| **SLOWER** | 25.85% |

**B. Cycle Time (Avg Staytime)**
Indicates the average duration an entity spends within each specific module.
| Object | Avg Staytime (Days) |
| :--- | :--- |
| **Queue1** | 0.030 |
| **FASTER** | 0.250 |
| **SLOWER** | 0.500 |

**C. Work in Process (Average WIP)**
Represents the average number of entities present in each section simultaneously.
| Object | Average WIP |
| :--- | :--- |
| **Queue1** | 0.059 |
| **FASTER** | 0.365 |
| **SLOWER** | 0.259 |

**D. Cumulative Throughput**
The total count of entities that have successfully passed through each component.
| Object | Total Throughput |
| :--- | :--- |
| **Source1** | 1,522,955 |
| **Queue1** | 1,505,065 |
| **FASTER** | 1,111,178 |
| **SLOWER** | 393,886 |
| **Sink2** | 17,890 |

---

#### 3. Technical System Analysis
The data suggests a **capacity-based load balancing** strategy:
1.  **Throughput Distribution**: The "FASTER" machine handles approximately **74%** of the total processed volume ($1,111,178$ out of $1,505,064$ total), confirming its role as the primary bottleneck-reducing resource.
2.  **Processing Ratio**: The cycle time for the "SLOWER" machine is exactly double that of the "FASTER" machine (0.500 vs 0.250), which directly correlates with the throughput variance.
3.  **Stability**: Despite the high cumulative throughput, machine utilization remains under 40% and the Queue1 WIP is very low (0.059), indicating that the system is stable and currently over-capacitated for the given arrival rate.

# Solution

V CT of faster machine = 0.25 days

$$
\rightarrow \mu = 1 / 0. 2 5 = 4 \mathrm {j} / \mathrm {d}
$$

V CT of slower machine = 0.5 days

$$
\rightarrow \mathrm {y} = 1 / 0. 5 = 2 \mathrm {j} / \mathrm {d}
$$

V Cumulative TH of Source = 1522955, Run time = 761602

$$
\rightarrow \lambda = 1 5 2 2 9 5 5 / 7 6 1 6 0 2 = 2 \mathrm {j} / \mathrm {d}
$$

V Cumulative TH of Sink = 17890, Cumulative TH of Source = 1522955

$$
\rightarrow \% \text {lost items} = 17890 / 1522955 = 0.0117 = 1.17 \%
$$

V Utilization of faster machine = 36.48, Utilization of slower machine = 28.85

→ Utilization of the workstation = (36.48+28.85)/2=32.67

# Combination of exponentials

> To model more general systems,one approach is to approximate the general times by combinations of exponentials   
The Erlang-k distribution is the sum of k independent and identical exponential distributions   
Since the Erlang-k has a squared coeficient of variation given by C² = 1/k, it also allows modeling of processes that have less variation than the exponential distribution

# Erlang distribution

> If times are not exponentially distributed   
>Approximation of times by combinations of exponentials   
> Erlang random variable with parameters k and β is the sum of k (independent) exponential random variables each with mean β /k Two Eriangprobawthy Two Erlang probability density functions with

$$
f (s) = \frac {k (k s) ^ {k - 1} e ^ {- (k / \beta) s}}{\beta^ {k} (k - 1) !} \text {f o r} s \geq 0
$$

$$
E [ X ] = \beta ; V [ X ] = \frac {\beta^ {2}}{k}; C ^ {2} [ X ] = \frac {1}{k}
$$

mean 1 and shape parameters k = 2 (solid line) and k = 10 (dashed line)

### Visual Diagram: Probability Density Functions for Service Times
- **Component Type**: Comparison graph of probability distributions.
- **Logic**: Illustrates the difference in variability between a purely random process and a multi-stage (Erlang) process, which is critical for calculating system congestion.

---

#### 1. The Solid Line: Exponential Distribution ($M$)
*   **Definition**: Represents the "Markovian" or memoryless process used in $M/M/1$ systems.
*   **Characteristics**: It has the highest probability at very short durations and a very long "tail."
*   **Variability**: The standard deviation is equal to the mean ($\sigma = E[x]$), resulting in a **Coefficient of Variation ($CV$) of 1**. This represents a high degree of randomness.

#### 2. The Dashed Line: Erlang Distribution ($E_k$)
*   **Definition**: Represents a process consisting of $k$ independent exponential stages.
*   **Characteristics**: The probability of very short service times is near zero because all $k$ stages must be completed. The curve is more concentrated around the mean.
*   **Variability**: As $k$ increases, the variance decreases ($\sigma^2_{E_k} = \frac{\sigma^2_M}{k}$). This results in a **Coefficient of Variation ($CV$) < 1**.

#### 3. Impact on Queuing Performance (VUT Logic)
In industrial engineering, the shape of these curves directly impacts the **VUT (Kingman's) formula**:
*   **High Variability (Solid Line)**: Leads to "clustering" of jobs, causing longer queues and higher Work-In-Process (WIP) even at moderate utilization.
*   **Low Variability (Dashed Line)**: Moving toward the dashed line (or a deterministic $D$ distribution) reduces the "Variability" term in the VUT equation, significantly lowering the average waiting time.

#### 4. Transition toward Determinism
*   **The Trend**: If $k$ continues to increase towards infinity, the dashed line would eventually become a single vertical spike at the mean.
*   **Engineering Goal**: Reducing process variability (moving from the solid line to the dashed line) is a primary objective in Lean manufacturing to stabilize cycle times without necessarily increasing machine speed.

# M/E2/1/3- Erlang processing time

Y Maximum number of jobs allowed in the system equal to 3   
> Inter-arrival times exponentially distributed with a mean arrival rate of 入   
> Processing time described by an Erlang-2 with mean rate μ   
Erlang-2 is modeled using two exponential nodes

Each node has a mean rate of 2u   
>The mean time spent in each node is 1/(2μ)→ the total time spent in the two nodes as 1/u

# M/E2/1/3- Erlang processing time

When a job begins its processing,it enters the node representing phase 1 and stays in phase 1 for an exponential length of time   
> When the job has been completed its phase 1 service, the job moves to the node representing phase 2   
> As long as the job is in either phase,it is considered to be continuing its processing and a new job is not allowed into service

Pair (n.i)

>n: number of jobs in the system   
>i: service phase occupied by the job being processed

### Visual Diagram: State-Transition Network for Erlang-2 Service ($M/E_2/1/3$)
- **Component Type**: Continuous-Time Markov Chain (CTMC) with phase-type service.
- **Logic**: Illustrates a queuing system with a finite capacity of 3 jobs ($N=3$), where the service time follows an Erlang-2 distribution ($k=2$).

---

#### 1. State Definition (Phase-Space Representation)
States are defined by the pair $(n, x)$, where **$n$** is the total number of jobs in the system and **$x$** is the current service phase of the job being processed:
*   **State 0**: The system is empty (idle).
*   **States 11, 12**: One job in the system. The job is currently in Phase 1 or Phase 2, respectively.
*   **States 21, 22**: Two jobs in the system. The job in service is in Phase 1 or Phase 2; the second job is waiting in the queue.
*   **States 31, 32**: Three jobs in the system (**Maximum Capacity**). The job in service is in Phase 1 or Phase 2; two additional jobs are waiting.

#### 2. Transition Rate Dynamics
*   **Arrival Rate ($\lambda$)**: Represents a new job entering the system. An arrival increases the job count but does not alter the service phase of the job currently at the server (e.g., $11 \xrightarrow{\lambda} 21$ or $12 \xrightarrow{\lambda} 22$).
*   **Service Phase Rate ($2\mu$)**: The service process consists of $k=2$ identical exponential phases. To maintain a total mean service rate of $\mu$, each phase must complete at rate **$2\mu$**.
    *   **Phase Completion**: Moving from Phase 1 to Phase 2 (e.g., $21 \to 22$).
    *   **Job Departure**: Completing Phase 2 of the current job and immediately starting Phase 1 of the next job in the queue (e.g., $22 \to 11$ or $32 \to 21$).

#### 3. System Boundaries
*   **Blocking**: In states 31 and 32, there are no outgoing $\lambda$ arcs. Any arrival occurring when 3 jobs are present is blocked and lost.
*   **Return to Idle**: When the system is in state 12 (the only job present is in its final phase), completion at rate $2\mu$ returns the system to State 0.

#### 4. Analytical Application
*   **Global Balance Equations**: This diagram is used to solve for steady-state probabilities ($p_{n,x}$). For example, the balance for state 12 is: $(\lambda + 2\mu)p_{12} = 2\mu p_{11}$.
*   **Performance Impact**: Because $k=2$, the service variability is lower than a standard exponential distribution ($CV = 1/\sqrt{2} \approx 0.707$). This reduction in variability results in a lower average Work-In-Process (WIP) compared to a Markovian $M/M/1/3$ system with the same utilization.

# M/E2/1/3- Erlang processing time

Node partitioning and corresponding equations

$$
\lambda p _ {0} - 2 \mu p _ {1 2} = 0
$$

$$
\lambda p _ {0} + \lambda p _ {1 2} - 2 \mu p _ {1 1} = 0
$$

$$
(\lambda + 2 \mu) p _ {1 1} - 2 \mu p _ {1 2} - 2 \mu p _ {2 2} = 0
$$

$$
\lambda p _ {1 1} + \lambda p _ {1 2} - 2 \mu p _ {2 2} = 0
$$

$$
\lambda p _ {2 1} + \lambda p _ {2 2} - 2 \mu p _ {3 2} = 0
$$

$$
\lambda p _ {2 2} + 2 \mu p _ {3 1} - 2 \mu p _ {3 2} = 0
$$

$$
p _ {0} + p _ {1 1} + p _ {1 2} + p _ {2 1} + p _ {2 2} + p _ {3 1} + p _ {3 2} = 1.
$$

# M/E2/1/3- Erlang processing time

Node partitioning and corresponding equations

$$
\lambda p _ {0} - 2 \mu p _ {1 2} = 0
$$

$$
\lambda p _ {0} + \lambda p _ {1 2} - 2 \mu p _ {1 1} = 0
$$

$$
(\lambda + 2 \mu) p _ {1 1} - 2 \mu p _ {1 2} - 2 \mu p _ {2 2} = 0
$$

$$
\lambda p _ {1 1} + \lambda p _ {1 2} - 2 \mu p _ {2 2} = 0
$$

$$
\lambda p _ {2 1} + \lambda p _ {2 2} - 2 \mu p _ {3 2} = 0
$$

$$
\lambda p _ {2 2} + 2 \mu p _ {3 1} - 2 \mu p _ {3 2} = 0
$$

$$
p _ {0} + p _ {1 1} + p _ {1 2} + p _ {2 1} + p _ {2 2} + p _ {3 1} + p _ {3 2} = 1.
$$

# M/E2/1/3- Erlang processing time

Node partitioning and corresponding equations

$$
\lambda p _ {0} - 2 \mu p _ {1 2} = 0
$$

$$
\lambda p _ {0} + \lambda p _ {1 2} - 2 \mu p _ {1 1} = 0
$$

$$
(\lambda + 2 \mu) p _ {1 1} - 2 \mu p _ {1 2} - 2 \mu p _ {2 2} = 0
$$

$$
\lambda p _ {1 1} + \lambda p _ {1 2} - 2 \mu p _ {2 2} = 0
$$

$$
\lambda p _ {2 1} + \lambda p _ {2 2} - 2 \mu p _ {3 2} = 0
$$

$$
\lambda p _ {2 2} + 2 \mu p _ {3 1} - 2 \mu p _ {3 2} = 0
$$

$$
p _ {0} + p _ {1 1} + p _ {1 2} + p _ {2 1} + p _ {2 2} + p _ {3 1} + p _ {3 2} = 1.
$$

# M/E2/1/3- Erlang processing time

Node partitioning and corresponding equations

$$
\lambda p _ {0} - 2 \mu p _ {1 2} = 0
$$

$$
\lambda p _ {0} + \lambda p _ {1 2} - 2 \mu p _ {1 1} = 0
$$

$$
(\lambda + 2 \mu) p _ {1 1} - 2 \mu p _ {1 2} - 2 \mu p _ {2 2} = 0
$$

$$
\lambda p _ {1 1} + \lambda p _ {1 2} - 2 \mu p _ {2 2} = 0
$$

$$
\lambda p _ {2 1} + \lambda p _ {2 2} - 2 \mu p _ {3 2} = 0
$$

$$
\lambda p _ {2 2} + 2 \mu p _ {3 1} - 2 \mu p _ {3 2} = 0
$$

$$
p _ {0} + p _ {1 1} + p _ {1 2} + p _ {2 1} + p _ {2 2} + p _ {3 1} + p _ {3 2} = 1.
$$

# M/E2/1/3- Erlang processing time

Node partitioning and corresponding equations

$$
\lambda p _ {0} - 2 \mu p _ {1 2} = 0
$$

$$
\lambda p _ {0} + \lambda p _ {1 2} - 2 \mu p _ {1 1} = 0
$$

$$
(\lambda + 2 \mu) p _ {1 1} - 2 \mu p _ {1 2} - 2 \mu p _ {2 2} = 0
$$

$$
\lambda p _ {1 1} + \lambda p _ {1 2} - 2 \mu p _ {2 2} = 0
$$

$$
\lambda p _ {2 1} + \lambda p _ {2 2} - 2 \mu p _ {3 2} = 0
$$

$$
\lambda p _ {2 2} + 2 \mu p _ {3 1} - 2 \mu p _ {3 2} = 0
$$

$$
p _ {0} + p _ {1 1} + p _ {1 2} + p _ {2 1} + p _ {2 2} + p _ {3 1} + p _ {3 2} = 1.
$$

# M/E2/1/3- Erlang processing time

Node partitioning and corresponding equations

$$
\lambda p _ {0} - 2 \mu p _ {1 2} = 0
$$

$$
\lambda p _ {0} + \lambda p _ {1 2} - 2 \mu p _ {1 1} = 0
$$

$$
(\lambda + 2 \mu) p _ {1 1} - 2 \mu p _ {1 2} - 2 \mu p _ {2 2} = 0
$$

$$
\lambda p _ {1 1} + \lambda p _ {1 2} - 2 \mu p _ {2 2} = 0
$$

$$
\lambda p _ {2 1} + \lambda p _ {2 2} - 2 \mu p _ {3 2} = 0
$$

$$
\lambda p _ {2 2} + 2 \mu p _ {3 1} - 2 \mu p _ {3 2} = 0
$$

$$
p _ {0} + p _ {1 1} + p _ {1 2} + p _ {2 1} + p _ {2 2} + p _ {3 1} + p _ {3 2} = 1.
$$

# M/E2/1/3- Erlang processing time

# Norming equation

$$
\lambda p _ {0} - 2 \mu p _ {1 2} = 0
$$

$$
\lambda p _ {0} + \lambda p _ {1 2} - 2 \mu p _ {1 1} = 0
$$

$$
(\lambda + 2 \mu) p _ {1 1} - 2 \mu p _ {1 2} - 2 \mu p _ {2 2} = 0
$$

$$
\lambda p _ {1 1} + \lambda p _ {1 2} - 2 \mu p _ {2 2} = 0
$$

$$
\lambda p _ {2 1} + \lambda p _ {2 2} - 2 \mu p _ {3 2} = 0
$$

$$
\lambda p _ {2 2} + 2 \mu p _ {3 1} - 2 \mu p _ {3 2} = 0
$$

$$
\left. \overline {{p _ {0} + p _ {1 1} + p _ {1 2} + p _ {2 1} + p _ {2 2} + p _ {3 1} + p _ {3 2} = 1}} \right\rbrack
$$

# M/E2/1/3- Erlang processing time

# V Alternative solution with node isolation

### Visual Diagram: Node Isolation for Local Balance (State 22)
- **Component Type**: Partitioned state-transition diagram for an $M/E_2/1/3$ system.
- **Logic**: Illustrates the isolation of a specific node to derive a local balance equation by equating the total probability flow entering and exiting that state.

---

#### 1. The Isolation Method
*   **Target Subset**: The diagram isolates **State 22** (representing 2 jobs in the system, with the job in service currently in its second phase) using a dashed blue partition.
*   **External Subset**: All other states in the Markov chain **{0, 11, 12, 21, 31, 32}** are grouped as the external environment relative to the isolated node.

#### 2. Flow Dynamics Across the Boundary
For the system to maintain steady-state equilibrium, the flow rate crossing the boundary into the node must equal the flow rate exiting it:

*   **Outward Flow (Exiting State 22)**:
    *   **Arrival ($\lambda$)**: A new job arrives, moving the system to state 32.
    *   **Service Completion ($2\mu$)**: The second phase of service concludes, returning the system to state 11 (starting phase 1 of the next job).
    *   **Total Outward Rate**: $(\lambda + 2\mu) p_{22}$.

*   **Inward Flow (Entering State 22)**:
    *   **Arrival from State 12**: An arrival occurs while the system is in phase 2 of the first job.
    *   **Phase Shift from State 21**: The job in service completes its first phase at rate $2\mu$.
    *   **Total Inward Rate**: $\lambda p_{12} + 2\mu p_{21}$.

#### 3. Resulting Local Balance Equation
Equating these flows provides the algebraic relationship necessary to solve for the steady-state probability of this specific state:
$$ (\lambda + 2\mu) p_{22} = \lambda p_{12} + 2\mu p_{21} $$

#### 4. Analytical Significance
Isolating nodes individually allows for the systematic construction of the global balance matrix. This specific equation links the probability of having two jobs ($p_2$) to both the lower-congested state ($p_1$) and the higher-congested state ($p_3$), facilitating the recursive resolution of the entire finite-capacity model.

$$
\begin{array}{l} \lambda p _ {0} = 2 \mu p _ {1 2} \\ \lambda p _ {1 1} + 2 \mu p _ {1 1} = \lambda p _ {0} + 2 \mu p _ {2 2} \\ \lambda p _ {1 2} + 2 \mu p _ {1 2} = 2 \mu p _ {1 1} \\ \lambda p _ {2 1} + 2 \mu p _ {2 1} = \lambda p _ {1 1} + 2 \mu p _ {3 2} \\ 2 \mu p _ {3 1} = \lambda p _ {2 1} \\ 2 \mu p _ {3 2} = \lambda p _ {2 2} + 2 \mu p _ {3 1} \\ \end{array}
$$

$$
p _ {0} + p _ {1 1} + p _ {1 2} + p _ {2 1} + p _ {2 2} + p _ {3 1} + p _ {3 2} = 1
$$

# M/E2/1/3- Erlang processing time

V Performance measures

$$
W I P _ {s} = \sum_ {n = 1} ^ {3} n \left(p _ {n 1} + p _ {n 2}\right)
$$

$$
t h = \lambda_ {e} = \lambda (1 - p _ {3 1} - p _ {3 2})
$$

$$
C T _ {s} = W I P _ {s} / \lambda_ {e}.
$$

# Exercise

# Input data

>Maximum number of jobs allowed in the system equal to 2   
>Inter-arrival times exponentially distributed with a mean arrival rate of λ=3 j/h   
> Processing time described by an Erlang-3 with mean rate μ=6 j/h

# V Questions

Draw the state diagram   
Derive the balance equations   
>Compute the performances of the system (WIP, WIPq, TH, CT, CTq)

# Solution

State diagram

### Visual Diagram: State-Transition Network for Erlang-3 Service ($M/E_3/1/2$)
- **Component Type**: Continuous-Time Markov Chain (CTMC) with phase-type service.
- **Logic**: Illustrates a queuing system with a finite capacity of 2 jobs ($N=2$), where the service time is modeled as an Erlang-3 distribution ($k=3$).

---

#### 1. State Definition (Phase-Space Representation)
States are labeled as $(n, x)$, where **$n$** is the number of jobs in the system and **$x$** is the current service phase of the job being processed:
*   **State 0**: The system is idle (empty).
*   **States 11, 12, 13**: One job in the system. The job is currently in Phase 1, 2, or 3, respectively.
*   **States 21, 22, 23**: Two jobs in the system (**Maximum Capacity**). One job is in service (Phase 1, 2, or 3), and one job is waiting in the queue.

#### 2. Transition Rate Dynamics
*   **Arrival Rate ($\lambda$)**: Represents a new job entering the system. 
    *   An arrival moves the system from $n$ to $n+1$ without changing the current service phase (e.g., $11 \xrightarrow{\lambda} 21$ or $12 \xrightarrow{\lambda} 22$).
    *   From state 0, an arrival moves the system to state 11.
*   **Service Phase Rate ($3\mu$)**: The service consists of $k=3$ identical exponential phases. To maintain a total mean service rate of $\mu$, each phase completes at rate **$3\mu$**.
    *   **Phase Shift**: Moving from one phase to the next (e.g., $11 \to 12 \to 13$).
    *   **Job Departure**: Completing Phase 3 triggers a departure. 
        *   If no one else is waiting ($13 \to 0$).
        *   If a second job is waiting ($23 \to 11$), the system returns to state 11 as the waiting job starts its first phase of service.

#### 3. System Constraints
*   **Blocking**: There are no arrival arrows ($\lambda$) exiting the states $21, 22, 23$. This confirms the system capacity is strictly limited to 2. Any arrival occurring when 2 jobs are already present is blocked and lost.
*   **Variability Reduction**: By using $k=3$ phases, the service time variability is significantly lower than a standard exponential distribution ($CV = 1/\sqrt{3} \approx 0.577$).

#### 4. Analytical Significance
This Markov chain allows for the calculation of steady-state probabilities $p_{n,x}$. These are used to determine:
*   **Blocking Probability**: $P_{block} = p_{21} + p_{22} + p_{23}$.
*   **Average WIP**: $\sum n \cdot p_{n,x}$.
*   **Effective Throughput**: $\lambda_{eff} = \lambda (1 - P_{block})$.

# Solution

# Equations with node isolation

### Visual Diagram: Node Isolation Method for $M/E_3/1/2$ System
- **Component Type**: Partitioned state-transition diagram (Local Balance approach).
- **Logic**: Illustrates the isolation of individual states via mathematical "cuts" to establish the equilibrium between inward and outward probability flows for each node.

---

#### 1. Partitioning Strategy (Node Isolation)
The dashed blue circles represent the **Isolation Method**. In steady-state, for any isolated subset (or single node), the rate at which the process leaves the subset must equal the rate at which it enters it. This is the visual basis for deriving the **Global Balance Equations**.

#### 2. Analysis of Key Isolated States
Based on the provided diagram, we can derive the following local equations:

*   **Isolated State 0 (Idle)**:
    *   **Flow Out**: $\lambda p_0$ (an arrival occurs).
    *   **Flow In**: $3\mu p_{13}$ (the only job finishes its 3rd phase).
    *   **Equation**: $\lambda p_0 = 3\mu p_{13}$
*   **Isolated State 11 (1 Job, Phase 1)**:
    *   **Flow Out**: $(\lambda + 3\mu) p_{11}$ (either a new arrival moves it to 21, or the first phase finishes).
    *   **Flow In**: $\lambda p_0$ (arrival when empty) + $3\mu p_{23}$ (a departure occurs from a full system).
    *   **Equation**: $(\lambda + 3\mu) p_{11} = \lambda p_0 + 3\mu p_{23}$
*   **Isolated State 23 (Full, Phase 3)**:
    *   **Flow Out**: $3\mu p_{23}$ (the job in service finishes).
    *   **Flow In**: $\lambda p_{13}$ (arrival while 1 job was in phase 3) + $3\mu p_{22}$ (phase 2 finishes while the system is full).
    *   **Equation**: $3\mu p_{23} = \lambda p_{13} + 3\mu p_{22}$

#### 3. Observation on State 12
In this specific visualization, **State 12** is the only node not highlighted with a dashed circle. This typically implies that its balance equation is either considered redundant (due to the linearly dependent nature of the equation system) or is derived as the "leftover" once all other nodes are balanced against the **Norming Equation** ($\sum p_{n,x} = 1$).

#### 4. Engineering Objective
This method allows us to transform a complex state-transition network into a solvable system of linear equations. By solving for $p_{n,x}$, we can determine the **Blocking Probability** ($p_{21}+p_{22}+p_{23}$) and the system's overall efficiency.

$$
\begin{array}{l} \lambda p _ {0} = 3 \mu p _ {1 3} \\ \lambda p _ {1 1} + 3 \mu p _ {1 1} = \lambda p _ {0} + 3 \mu p _ {2 3} \\ 3 \mu p _ {1 3} + \lambda p _ {1 3} = 3 \mu p _ {1 2} \\ 3 \mu p _ {2 1} = \lambda p _ {1 1} \\ 3 \mu p _ {2 2} = \lambda p _ {1 2} + 3 \mu p _ {2 1} \\ 3 \mu p _ {2 3} = \lambda p _ {1 3} + 3 \mu p _ {2 2} \\ \end{array}
$$

$$
\begin{array}{l} p _ {0} + p _ {1 1} + p _ {1 2} + p _ {1 3} + p _ {2 1} + p _ {2 2} + \\ \mathsf {p} _ {2 3} = 1 \\ \end{array}
$$

Solution: Po= 0.557,P11= 0.127, P12= 0.108,P13= 0.093,

$$
\mathsf {p} _ {2 1} = 0. 0 2 1, \mathsf {p} _ {2 2} = 0. 0 3 9, \mathsf {p} _ {2 3} = 0. 0 5 5
$$

# Solution

Excel to solve linear systems of N equations

>Linear systems can be written in matrix form Ax = b   
>If the matrix Ahas an nverse,the solutionisX=A-1b

Select a column of N cells and type the function:

$$
= \text {M M U L T (M I N V E R S E (F i r s t C e l l O f A : L a s t C e l l O f A) , F i r s t C e l l O f b : L a s t C e l l O f b)}
$$

> When finished typing, hold down the <ctrl> and <shift> keys and while holding these two keys down, hit <enter>

### Visual Diagram: Mathematical Matrix for $M/E_3/1/2$ Steady-State Probabilities
- **Component Type**: System of linear equations in matrix form ($A \cdot x = b$).
- **Logic**: Numerical implementation of global balance equations derived from node isolation, used to calculate the exact probability of each system state.

---

#### 1. Matrix Structure and Variables
The matrix columns represent the variables to be solved (the steady-state probabilities $p_{n,x}$), while the rows represent the balance equations for each node:
*   **Columns**: $p_0$ (idle), $p_{11}, p_{12}, p_{13}$ (1 job, phases 1-3), and $p_{21}, p_{22}, p_{23}$ (2 jobs, phases 1-3).
*   **Column $b$**: The right-hand side of the equations. Most are set to 0 (equilibrium), while the last is set to 1 (norming condition).

#### 2. Parameter Inference from Coefficients
Based on the coefficients in the matrix, the system parameters used for this specific calculation are:
*   **Arrival Rate ($\lambda$)**: $3$ (seen in the coefficients for arrivals).
*   **Phase Service Rate ($3\mu$)**: $18$ (seen in the coefficients for service completions). This implies an individual phase rate of $6$ and a total mean service rate of $\mu = 6$.
*   **Utilization**: $\rho = \frac{\lambda}{\mu} = \frac{3}{6} = 0.5$.

#### 3. Row Logic
*   **Equations 1-6 (Global Balance)**: Each row corresponds to the flow equilibrium of a specific state. For example, **Equation 1** ($3p_0 - 18p_{13} = 0$) represents the idle state balance: $\lambda p_0 = 3\mu p_{13}$.
*   **Equation 7 (Norming Equation)**: The row of 1s ensures that the sum of all probabilities equals exactly 1 ($\sum p_{n,x} = 1$). This is a necessary constraint to solve the system since balance equations are linearly dependent.

#### 4. Calculated Numerical Results
The **result** column provides the final stationary distribution for the system:
*   **$p_0 = 0.5574$**: The system is empty more than 55% of the time.
*   **Probabilities of 1 job**: $p_{11} \approx 0.1265$, $p_{12} \approx 0.1084$, $p_{13} \approx 0.0929$.
*   **Probabilities of 2 jobs (Full)**: $p_{21} \approx 0.0211$, $p_{22} \approx 0.0391$, $p_{23} \approx 0.0546$.
*   **Total Blocking Probability ($P_{block}$)**: $p_{21} + p_{22} + p_{23} \approx 0.1148$ (approx. 11.5%).

---

#### 5. Engineering Conclusion
With a utilization of 0.5 and a service process divided into 3 Erlang phases, this workstation maintains a high idle rate and a relatively low blocking probability, demonstrating the stability provided by reducing service variability.

# Solution

Average number of jobs in the system:

$$
W I P s = p _ {1 1} + p _ {1 2} + p _ {1 3} + 2 p _ {2 1} + 2 p _ {2 2} + 2 p _ {2 3} = 0. 5 5 8 \mathrm {j o b s}
$$

V Average number of jobs in the queue:

$$
\mathrm {W I P q} = \mathrm {p} _ {2 1} + \mathrm {p} _ {2 2} + \mathrm {p} _ {2 3} = 0. 1 1 5 \mathrm {j o b s}
$$

Throughput

$$
\mathsf {T H} = \lambda (1 - (\mathsf {p} _ {2 1} + \mathsf {p} _ {2 2} + \mathsf {p} _ {2 3})) = 2. 6 5 5 \mathrm {j / h}
$$

Average cycle times:

$$
\mathsf {C T s} = \frac {W I P s}{T H} = \left(\frac {0 . 5 5 8}{2 . 6 5 5}\right) = 0. 2 1 \mathrm {h o u r s}
$$

$$
\mathrm {C T q} = \frac {W I P q}{T H} = \left(\frac {0 . 1 1 5}{2 . 6 5 5}\right) = 0. 0 4 3 \mathrm {h o u r s}
$$

# Exercise

Consider an M/E3/1/3 model with an arrival rate of 4 j/h and a service rate of 8 j/h. Compute the system performance measures of TH, WIP, WIPq, and CT, given the steady-state probability vector

$$
\begin{array}{l} p = \left[ p _ {0}, p _ {1, 1}, p _ {1, 2}, p _ {1, 3}, p _ {2, 1}, p _ {2, 2}, p _ {2, 3}, p _ {3, 1}, p _ {3, 2}, p _ {3, 3} \right] ^ {T} \\ = [ 0. 5 2 0 7, 0. 1 1 8 0, 0. 1 0 1 2, 0. 0 8 6 8, 0. 0 3 5 7, 0. 0 4 5 1, 0. 0 5 1 0, 0. 0 0 6 0, 0. 0 1 3 5, 0. 0 2 2 0 ] ^ {T} \\ \end{array}
$$

where p_(m,n)is the state probability,mis the numberof jobs in thefacility and n is the Erlang phase.

# Solution

### Summary of Performance Metrics for Finite Capacity Systems
- **Component Type**: Summary table of system performance indicators (KPIs).
- **Logic**: Applies the results of steady-state probability calculations to determine effective throughput, inventory levels, and cycle times.

---

#### 1. Effective Throughput (TH)
*   **Formula**: $\lambda_e = \lambda(1 - p_{n_{max}})$
*   **Description**: Represents the actual rate at which jobs enter the system. In finite capacity models, the raw arrival rate ($\lambda$) must be adjusted by the probability that an arriving job finds the system full ($p_{n_{max}}$) and is blocked.
*   **Calculation**: With an arrival rate of 4 jobs/hour and a blocking probability of 0.0415, the effective throughput is **3.834 jobs/hour**.

#### 2. Work in Process (WIP)
*   **Formula**: $WIP = \sum n \cdot p_{n}$
*   **Description**: The average number of jobs currently in the system (both in service and in the queue).
*   **Logic**: It is the weighted sum of the number of jobs $n$ multiplied by the probability of being in those states. For phase-type distributions (like Erlang), this includes summing across all phases for each job count (e.g., $p_{1,1} + p_{1,2} + p_{1,3}$).
*   **Result**: The system maintains an average of **0.6941 jobs**.

#### 3. Queue Inventory ($WIP_q$)
*   **Formula**: $WIP_q = \sum (n-1) \cdot p_{n}$ (for $n \ge 1$)
*   **Description**: The average number of jobs waiting in the queue, excluding the one currently being processed.
*   **Calculation**: This sums the probabilities of having jobs in excess of the server's capacity.
*   **Result**: On average, **0.2148 jobs** are waiting in line.

#### 4. Cycle Time (CT) - Little's Law
*   **Formula**: $CT = \frac{WIP}{\lambda_e}$
*   **Description**: The average total time a job spends in the system from arrival to departure.
*   **Application**: By applying Little's Law using the effective throughput ($\lambda_e$) rather than the raw arrival rate, we determine the average stay time.
*   **Result**: The average cycle time is **0.1810 hours** (approximately 10.8 minutes).

# General service distribution M/G/1

> Consider a single-server system with exponential inter-arrival times,with mean rate λ,and a general service time distribution having mean time 1/μ and variance σs2   
V The state-diagram approach can no longer be used to develop equations that define the steady-state probabilities   
> The derivation of these probabilities is beyond the scope of this course

# General service distribution M/G/1

> The Pollaczek and Khintchine,or“P-K", formula for WIP in an M/G/1 queueing system is given by

$$
W I P _ {s} = E [ N ] = \frac {\lambda}{\mu} + \frac {\left(\frac {\lambda}{\mu}\right) ^ {2} + \lambda^ {2} \sigma_ {s} ^ {2}}{2 \left(1 - \frac {\lambda}{\mu}\right)}
$$

where N is the number of jobs in the system,λ is the mean arrival rate,and the service distribution has mean and variance given by 1/μ and σ²， respectively

# General service distribution M/G/1

The relationship between the average number in the system and the average number in the queue is given by WIPs-WIPq =Xe/μ. Since λe => for M/G/1 systems, the expected number of jobs waiting for the processing,E[Nq], is

$$
W I P _ {q} = E [ N _ {q} ] = \frac {\left(\frac {\lambda}{\mu}\right) ^ {2} + \lambda^ {2} \sigma_ {s} ^ {2}}{2 \left(1 - \frac {\lambda}{\mu}\right)}
$$

# General service distribution M/G/1

> The P-K formula for the queue cycle time in an M/G/1 system is given by

$$
C T _ {q} = E [ T _ {q} ] = \frac {W I P _ {q}}{\lambda} = \frac {\left(\frac {\lambda}{\mu}\right) ^ {2} + \lambda^ {2} \sigma_ {s} ^ {2}}{2 \lambda \left(1 - \frac {\lambda}{\mu}\right)}
$$

# General service distribution M/G/1

> The goal is now to rearrange this formula into a form that wil be utilized a great deal in the development of more realistic factory models.   
First recall that the squared coefficient of variation is defined by

$$
C ^ {2} [ T ] = \frac {V [ T ]}{E [ T ] ^ {2}}
$$

Recall the M/M/1 formulas

$$
W I P _ {s} (M / M / 1) = \frac {u}{1 - u}
$$

$$
C T _ {s} (M / M / 1) = \frac {1}{\mu - \lambda}
$$

$$
W I P _ {q} (M / M / 1) = \frac {u ^ {2}}{1 - u}, \mathrm {a n d}
$$

$$
C T _ {q} (M / M / 1) = \frac {u}{1 - u} E [ T _ {s} ]
$$

# General service distribution M/G/1

The P-K formula can be rewritten as

$$
\begin{array}{l} C T _ {q} = \frac {\left(\frac {\lambda}{\mu}\right) ^ {2} + \lambda^ {2} \sigma_ {s} ^ {2}}{2 \lambda \left(1 - \frac {\lambda}{\mu}\right)} \\ = \frac {\left(\frac {\lambda}{\mu}\right) ^ {2} + \lambda^ {2} \frac {C _ {s} ^ {2}}{\mu^ {2}}}{2 \lambda \left(1 - \frac {\lambda}{\mu}\right)} \\ = \left(\frac {1 + C _ {s} ^ {2}}{2}\right) \left(\frac {u}{1 - u}\right) E [ T _ {s} ] \\ \end{array}
$$

# General service distribution M/G/1

1 Relationship between M/M/1 and M/G/1

$$
C T _ {q} (M / G / 1) = \left(\frac {1 + C _ {s} ^ {2}}{2}\right) C T _ {q} (M / M / 1)
$$

# Approximation for G/G/1 systems

> The Kingman diffusion approximation for the G/G/1 queueing system is

$$
C T _ {q} (G / G / 1) \approx \left(\frac {C _ {a} ^ {2} + C _ {s} ^ {2}}{2}\right) C T _ {q} (M / M / 1)
$$

where Ca² and C² are the squared coefficients of variation for the inter-arrival distribution and the service time distribution, respectively

# Approximation for G/G/1 systems

Kingman equation also called the VUT equation

$$CT_q(G/G/1) \approx \left( \frac{C_a^2 + C_s^2}{2} \right) CT_q(M/M/1)$$

# Approximation for G/G/1 systems

> Since the time in the system equals the time in the queue plus the processing time,we also have a good approximation for the system mean cycle time as

$$
C T _ {s} (G / G / 1) \approx \left(\frac {C _ {a} ^ {2} + C _ {s} ^ {2}}{2}\right) \left(\frac {u}{1 - u}\right) E [ T _ {s} ] + E [ T _ {s} ]
$$

# Example

> Consider a system with λ= 4/hr and μ = 5/hr yielding a utilization factor u = O.8. Since this was an exponential system, we had Ca2 = C² = 1 and E[Ts]= 0.2 hr   
Thus,the G/G/1 approximation is

$$
C T _ {q} (G / G / 1) = \left(\frac {C _ {a} ^ {2} + C _ {s} ^ {2}}{2}\right) \left(\frac {u}{1 - u}\right) E [ T _ {s} ] = \left(\frac {1 + 1}{2}\right) \left(\frac {0 . 8}{0 . 2}\right) 0. 2 = 0. 8 \mathrm {h r}
$$

> Whenever the Kingman approximation is applied to an M/M/1 or M/G/1 system, it is exact and not an approximation

# Example

Consider a G/G/1 system with inter-arrival times distributed

according to a gamma distribution with mean 15 minutes and

standard deviation 30 minutes,and with service times distributed

according to an Erlang-4 distribution with mean 12 minutes.

Since the distribution of service times is Erlang, the initial temptation

may be to use the Erlang methodology; however, because the

arrival times are not exponential, the G/G/1 formula has to be used.

The given data yields the following parameters: ^= 4/hr, μ = 5/hr,

$$
\mathsf {C} _ {\mathrm {a}} ^ {2} = 4, \mathsf {a n d} \mathsf {C} _ {\mathrm {s}} ^ {2} = 0. 2 5.
$$

Compute the performances of the system.

# Solution

Utilization u = 0.8   
> Arrival process has more variability and the processing times are less variable with respect to the exponentially distributed system.

$$
C T _ {q} (G / G / 1) \approx \left(\frac {C _ {a} ^ {2} + C _ {s} ^ {2}}{2}\right) \left(\frac {u}{1 - u}\right) E [ T _ {s} ] = \left(\frac {4 + 0 . 2 5}{2}\right) \left(\frac {0 . 8}{0 . 2}\right) 0. 2 = 1. 7 \mathrm {h r}
$$

This cycle time is over twice a large as the exponentially distributed system result; thus, the variability associated with nonexponential distributions can have a significant impact on the expected cycle time

# Solution

Other performance measures

$$
W I P _ {q} = \lambda \cdot C T _ {q} = 6. 8 \mathrm {j o b s}
$$

$$
C T s = C T _ {q} + \mathsf {E} [ \mathsf {T} _ {\mathsf {s}} ] = 1. 9 \mathrm {h r s}
$$

$$
W I P s = C T s \cdot T H = 7. 6 \mathrm {j o b s}
$$

# Exercise

Consider a WS with the following parameters:

> λ= 2.875 jobs/hr = 0.0479 jobs/min   
V Ca= 1 (exponential arrival times distribution)   
E[T]= 20 min = 0.33 h   
Cs=2.5 (not exponential process times distribution)   
u = 0.9583   
Compute the WS performance measures

# Solution

$$
C T _ {q} \left(G / G / 1\right) = \left(\frac {1 + 6 . 2 5}{2}\right) \left(\frac {0 . 9 5 8 3}{1 - 0 . 9 5 8 3}\right) \cdot 2 0 = 2 7. 7 7 \mathrm {h r s}
$$

$$
W I P _ {q} = \lambda \cdot C T _ {q} = 8 0 \mathrm {j o b s}
$$

$$
C T s = C T _ {q} + \mathsf {E} [ \mathsf {T} _ {\mathsf {s}} ] = 2 8. 1 \mathrm {h r s}
$$

$$
W I P s = C T s \cdot T H = 8 1 \mathrm {j o b s}
$$

# Approximation for G/G/c systems

> There are many generalizations of the G/G/1 approximations to account for multiple server systems in the literature   
> Allen and Cunneen have one of the first commonly used approximation based on the Kingman diffusion approximation   
Their approximation was later adjusted by Hall to be a simple extension of M/M/c

$$
C T _ {q} (G / G / c) \approx \left(\frac {C _ {a} ^ {2} + C _ {s} ^ {2}}{2}\right) C T _ {q} (M / M / c)
$$

# Approximation for G/G/c systems

$$
C T _ {q} (M / M / c) = \left(\frac {u ^ {\sqrt {2 c + 2} - 2}}{c}\right) C T _ {q} (M / M / 1)
$$

Thus, the Kingman diffusion approximation extended for a multiserver system is

$$
C T _ {q} (G / G / c) \approx \left(\frac {C _ {a} ^ {2} + C _ {s} ^ {2}}{2}\right) \left(\frac {u ^ {\sqrt {2 c + 2} - 1}}{c (1 - u)}\right) E [ T _ {s} ]
$$

# Example

> Consider again the system except for a two-server system and with a mean service time of 24 minutes   
Thus,server utilization stays the same (namely, u =O.8) and the squared coefficients of variation are still given as Ca² = 4 and Cs2 = 0.25   
Then the expected system cycle time using the approximation is

$$
C T _ {q} (G / G / 2) \approx \left(\frac {4 + 0 . 2 5}{2}\right) \left(\frac {(0 . 8) ^ {\sqrt {6} - 1}}{2 (1 - 0 . 8)}\right) 0. 4 = 1. 5 4 \mathrm {h r}
$$

# 3.1 Variability and Model Simulation

## 3.1.1 From Deterministic to Stochastic Models
In earlier lessons, production systems were analyzed using deterministic times to introduce KPIs and their relationships.  
However, deterministic models are not sufficient to describe real systems.

From this lesson onward, **variability** is explicitly introduced by modeling:
- arrival times,
- processing times,
as random variables.

---

# 3.1.2 Variability in Production Systems

## Definition
Variability is the departure from regular and predictable behavior of a process.

It mainly affects:
- inter-arrival times,
- processing times.

---

## Sources of Variability
Common sources include:
- machine failures,
- material shortages,
- operator availability and skill differences,
- material handling,
- product variety.

---

# 3.1.3 Random Variables
Arrival and processing times are modeled as random variables characterized by:
- distribution type,
- mean value (μ),
- variance (σ²),
- standard deviation (σ).

---

# 3.1.4 Coefficient of Variation

The coefficient of variation is defined as:
```
C = σ / μ
```
and measures variability relative to the mean.

### Classification
- Low variability: C < 0.75
- Moderate variability: 0.75 ≤ C ≤ 1.33
- High variability: C > 1.33

---

# 3.1.5 Example: Travel Times
Comparing two commuting processes shows that standard deviation alone is misleading.  
The coefficient of variation correctly captures relative variability.

---

# 3.1.6 Variability and Queues
Without variability:
- queues are either always empty or diverge to infinity.

With variability:
- average waiting times and WIP are finite,
- queueing theory becomes applicable.

---

# 3.1.7 Single Workstation Behavior

Assume:
- processing time = 10 minutes (constant).

If:
- inter-arrival time > processing time → no queue,
- inter-arrival time = processing time → utilization = 1, no queue,
- inter-arrival time < processing time → infinite queue.

---

# 3.1.8 Effect of Variability
Introducing variability in arrivals causes:
- idle times and congestion,
- formation of queues,
- finite average waiting times.

---

# 3.1.9 Utilization

Utilization is defined as:
```
U = E[TS] / E[TA]
```

With variability, higher utilization increases the probability of congestion.

---

# 3.1.10 Trade-off
High utilization leads to high waiting times.  
The only way to achieve both high utilization and low waiting times is to **reduce variability**.

---

# 3.1.11 Simulation Model
A basic simulation includes:
- source,
- queue,
- processor.

Simulation confirms analytical results.

---

# 3.1.12 Limited Systems
When queue capacity is limited:
- blocking occurs,
- WIP is bounded,
- simulation matches analytical formulas.

---

# 3.1.13 Key Takeaways
- Variability causes queues.
- Coefficient of variation measures variability correctly.
- Reducing variability improves performance.

# 3.2 Limited System – Diagram Model

## 3.2.1 Objective
This section introduces the **limited queueing system** and shows how to:
- model the system using a **state diagram**,
- compute **state probabilities**,
- derive key performance indicators:
  - WIP,
  - throughput,
  - cycle time,
  - queue length and waiting time.

The limited system is used as a **didactic example** because it can be solved exactly using balance equations.

---

# 3.2.2 System Description

- Single machine
- Single job type
- Maximum number of jobs allowed in the system: **3**
  - 1 job in service
  - up to 2 jobs in the queue
- If the system is full, arriving jobs are **rejected**

---

# 3.2.3 Input Parameters fileciteturn10file0

- Arrival rate:  
```
λ = 5 jobs/day
```
- Processing time:  
```
E[TS] = 1/4 day
```
- Processing rate:  
```
μ = 4 jobs/day
```

Both arrival and processing times are assumed **exponentially distributed**.

---

# 3.2.4 State Diagram

Each state represents the **number of jobs in the system**.

## States
- State 0: 0 jobs
- State 1: 1 job
- State 2: 2 jobs
- State 3: 3 jobs (system full)

No additional states are allowed.

---

## Transitions
- Arrival (λ):
  - 0 → 1
  - 1 → 2
  - 2 → 3
- Service completion (μ):
  - 1 → 0
  - 2 → 1
  - 3 → 2

From state 3, arrivals are **blocked**.

---

# 3.2.5 Balance Equations

In steady state:

```
P0 · λ = P1 · μ
P1 · λ = P2 · μ
P2 · λ = P3 · μ
```

Normalization condition:

```
P0 + P1 + P2 + P3 = 1
```

---

# 3.2.6 State Probabilities

Expressing probabilities as a function of P0:

```
P1 = (λ / μ) · P0
P2 = (λ / μ)² · P0
P3 = (λ / μ)³ · P0
```

Substituting numerical values:

```
P0 = 1 / (1 + 5/4 + (5/4)² + (5/4)³) ≈ 0.173
P1 ≈ 0.217
P2 ≈ 0.271
P3 ≈ 0.339
```

---

# 3.2.7 Interpretation of Probabilities

- P0: probability that the system is empty  
  → machine idle
- P3: probability that the system is full  
  → arriving jobs are rejected

---

# 3.2.8 Work In Process (WIP)

Average number of jobs in the system:

```
WIP = Σ (n · Pn),  n = 0…3
```

Numerical result:

```
WIP = 1·P1 + 2·P2 + 3·P3 ≈ 1.776 jobs
```

---

# 3.2.9 Throughput

In a limited system:

```
TH ≠ λ
```

Effective arrival rate:

```
TH = λ · (1 − P3)
```

Numerical result:

```
TH = 5 · (1 − 0.339) ≈ 3.305 jobs/day
```

---

# 3.2.10 Cycle Time

Using Little’s Law:

```
CT = WIP / TH
```

Numerical result:

```
CT ≈ 0.537 days
```

---

# 3.2.11 Queue Performance

## Average Queue Length
Maximum queue length = 2 jobs

```
WIP_Q = 1·P2 + 2·P3 ≈ 0.95 jobs
```

---

## Queue Cycle Time

Method 1:
```
CTQ = CT − E[TS]
```
```
CTQ ≈ 0.537 − 0.25 = 0.287 days
```

Method 2:
```
CTQ = WIP_Q / TH ≈ 0.287 days
```

---

# 3.2.12 Summary of Results

| Metric | Value |
|------|------|
| WIP (system) | 1.776 jobs |
| WIP (queue) | 0.95 jobs |
| Throughput | 3.305 jobs/day |
| Cycle Time | 0.537 days |
| Queue Cycle Time | 0.287 days |

---

# 3.2.13 Key Takeaways

- Limited systems allow **exact analytical solutions**.
- State probabilities are central to performance evaluation.
- Throughput is reduced due to **job rejection**.
- Little’s Law still applies using **effective throughput**.
- This example is the foundation for **unlimited system models**.

# 3.3 Queuing Systems – Kendall Notation and M/M/1 Formula

## 3.3.1 Introduction to Queueing Theory
Queueing theory was first developed by **A. K. Erlang (1917)** to analyze waiting times in telephone systems.
Today it is applied to many contexts:
- banks and post offices,
- hospitals and healthcare systems,
- transportation systems,
- production systems and workstations.

In this course, queueing theory is applied to **production systems**, where jobs arrive at workstations, wait in queues, and are processed by machines.

---

# 3.3.2 Elements of a Queueing System

A queueing system consists of three main components:

## Arrival Process
- Describes how jobs arrive at the system.
- Characterized by:
  - arrival rate (λ),
  - inter-arrival time distribution.
- Jobs may arrive individually or in batches.

## Service Process
- Describes how jobs are processed.
- Characterized by:
  - processing rate (μ),
  - processing time distribution.
- One or more **parallel machines** may exist.

## Queue
- Place where jobs wait if machines are busy.
- Can be:
  - unlimited,
  - limited (maximum number of jobs allowed).
- Service order (FIFO, LIFO, etc.) is not relevant for this course.

---

# 3.3.3 Limited vs Unlimited Systems fileciteturn11file0

- **Unlimited system**: no limit on queue length.
- **Limited system**: a maximum number of jobs is allowed in the system.
  - If the system is full, arriving jobs are rejected.

Each **workstation** is modeled as:
- one queue,
- one or more parallel machines.

---

# 3.3.4 Kendall Notation

A queueing system is summarized using **Kendall notation**:

```
A / S / m / K / discipline
```

Where:
- **A**: arrival process distribution
- **S**: service process distribution
- **m**: number of parallel machines
- **K**: maximum number of jobs in the system
- **discipline**: queue rule (usually omitted)

---

## Distribution Symbols
- **M**: Markovian (exponential distribution)
- **G**: General distribution
- **D**: Deterministic
- **Eₖ**: Erlang distribution

Examples:
- `M/M/1` → unlimited system
- `M/M/1/3` → limited system with max 3 jobs

---

# 3.3.5 The M/M/1 System

The simplest and most important model:
- exponential inter-arrival times,
- exponential service times,
- one machine,
- unlimited queue.

Assumption:
```
λ < μ
```
(otherwise the system is unstable).

---

# 3.3.6 State Probabilities

Probability of having *n* jobs in the system:

```
Pₙ = (1 − ρ) · ρⁿ
```

Where:
```
ρ = λ / μ
```
is the **utilization factor**.

---

# 3.3.7 Performance Measures for M/M/1

## Utilization
```
U = ρ = λ / μ
```

## Throughput
```
TH = λ
```

---

## Work In Process (WIP)
```
WIP = ρ / (1 − ρ)
```

---

## Cycle Time
Using Little’s Law:
```
CT = WIP / TH = 1 / (μ − λ)
```

Equivalent form:
```
CT = E[TS] / (1 − U)
```

---

## Queue Cycle Time
```
CTQ = CT − E[TS]
```

---

## Queue WIP
```
WIP_Q = U² / (1 − U)
```

---

# 3.3.8 Interpretation

- As utilization approaches 1:
  - waiting times grow rapidly,
  - WIP explodes.
- High utilization without variability reduction leads to congestion.
- These formulas are **valid only for M/M/1 systems**.

---

# 3.3.9 Example (Solved)

Given:
```
λ = 4 jobs/hour
μ = 5 jobs/hour
```

Utilization:
```
U = 0.8
```

Results:
- WIP = 4 jobs
- CT = 1 hour
- CTQ = 0.8 hours
- Probability server idle = 1 − U = 0.2

---

# 3.3.10 Key Takeaways
- Kendall notation compactly describes queueing systems.
- M/M/1 is the reference model for queueing theory.
- Performance depends strongly on utilization.
- These formulas form the basis for more complex models.

# 3.4 M/M/c Systems with Non‑Identical Service Rates

## 3.4.1 Scope of the Lesson
This section extends queueing analysis from **M/M/1** to **M/M/c** systems and then addresses the realistic case of **non‑identical parallel machines**.

Assumptions:
- exponential inter‑arrival times,
- exponential processing times,
- parallel servers at the same workstation.

The focus is on:
- state diagram construction,
- balance equations,
- computation of WIP, throughput, cycle time, and utilization,
- comparison with simulation results.

---

# 3.4.2 Review: M/M/c with Identical Machines

## System Description
- Arrival rate: λ  
- c identical machines  
- Service rate of each machine: μ  

Total service capacity:
```
μ_total = c · μ
```

---

## State Diagram Logic
- State *n*: number of jobs in the system.
- Forward transitions (arrivals): rate λ.
- Backward transitions (service completions):
  - for n < c → n · μ
  - for n ≥ c → c · μ

---

## Queue Cycle Time Formula (Identical Machines)
For M/M/1:
```
CTQ = U / (1 − U) · E[TS]
```

For M/M/c:
```
CTQ = (U^(√(2c+2) − 1) / c) · CTQ(M/M/1)
```

---

# 3.4.3 Non‑Identical Parallel Machines

## Assignment Rules
- First arriving job goes to the **fastest machine**.
- If only one machine is idle, the job goes to the idle one.
- Jobs do not switch machines once assigned.

Parameters:
- λ (arrival rate)
- μ (fast machine)
- γ (slow machine), γ < μ

---

# 3.4.4 Limited System with Two Machines

## States
- 0, 1F, 1S, 2, 3, 4

Arrivals blocked in state 4.

---

## Balance Equations (Structure)
```
P0·λ = P1F·μ + P1S·γ
P1F·λ = P2·γ
P1S·λ = P2·μ
Σ Pi = 1
```

---

# 3.4.5 Numerical Example

Given:
- λ = 3 jobs/day
- μ = 3 jobs/day
- γ = 2 jobs/day
- WIPmax = 4

Results:
- WIP ≈ 1.36 jobs
- TH ≈ 2.79 jobs/day
- CT ≈ 0.49 days
- Utilization ≈ 55%

---

# 3.4.6 Key Takeaways
- Identical vs non‑identical servers require different models.
- State diagrams are mandatory for non‑identical machines.
- Limited systems reduce throughput via rejection.
- Simulation validates analytical models.

# 3.5 Erlang Processing Time (M/Eₖ/· Models)

## 3.5.1 Motivation
So far, queueing models assumed **exponentially distributed processing times**.  
This section generalizes the analysis by introducing **Erlang-distributed processing times**, which:
- reduce variability compared to exponential times,
- approximate more deterministic behaviors,
- serve as an intermediate step toward general distributions.

---

# 3.5.2 Erlang Distribution

## Definition
An **Erlang-k distribution** is defined as the sum of **k independent and identical exponential random variables**.

Parameters:
- **k**: number of phases
- **β**: mean processing time

Each phase has:
```
mean = β / k
rate = k / β
```

---

## Key Properties
- Mean:
```
E[TS] = β
```
- Variance:
```
Var(TS) = β² / k
```
- Squared coefficient of variation:
```
C² = 1 / k
```

Special cases:
- k = 1 → exponential distribution
- k → ∞ → deterministic processing time

---

# 3.5.3 Impact on Variability
Increasing **k**:
- reduces variability,
- reduces queueing and waiting times,
- improves system performance for the same utilization.

---

# 3.5.4 Modeling Erlang Processing Times

An Erlang-k process can be represented as:
- **k exponential phases in series**,
- each phase corresponding to a state in the diagram.

This preserves the **Markov property**, allowing:
- state diagrams,
- balance equations,
- analytical solutions.

---

# 3.5.5 Example: M/E₂/1/3 System

## System Description
- Arrival process: exponential (M)
- Processing time: Erlang-2 (E₂)
- One machine
- Maximum WIP = 3 jobs

Notation:
```
M/E₂/1/3
```

---

## State Representation
Each state is denoted by:
```
(n, p)
```
where:
- **n** = number of jobs in the system
- **p** = Erlang phase (1 or 2)

States:
- (0)
- (1,1), (1,2)
- (2,1), (2,2)
- (3,1), (3,2)

Arrivals are blocked when n = 3.

---

## Transition Rates
- Arrivals: λ (if n < 3)
- Phase transitions: 2μ
- Completion of phase 2 → job departure

---

# 3.5.6 Balance Equations (Node Isolation)

Each node is isolated to write balance equations.
Example structure:
```
λ·P0 = 2μ·P(1,2)
λ·P(1,1) + 2μ·P(1,1) = λ·P0 + 2μ·P(2,2)
...
Σ Pi = 1
```

This guarantees:
- no missing states,
- complete probability system.

---

# 3.5.7 Performance Measures

## Effective Throughput
```
TH = λ · (1 − P_full)
```

---

## Work In Process (WIP)
```
WIP = Σ n · P(n,p)
```

---

## Queue WIP
```
WIP_Q = Σ (n − 1) · P(n,p)   for n ≥ 2
```

---

## Cycle Time
Using Little’s Law:
```
CT = WIP / TH
```

---

## Queue Cycle Time
```
CTQ = WIP_Q / TH
```

---

# 3.5.8 Numerical Example (Solved)

### Given
- λ = 3 jobs/hour
- μ = 6 jobs/hour
- Erlang-3 processing time
- Maximum WIP = 2 jobs

### Results
- Average WIP ≈ 0.58 jobs
- Queue WIP ≈ 0.115 jobs
- Throughput ≈ 2.66 jobs/hour
- Cycle Time ≈ 0.40 hours

Low queueing is due to:
- low utilization,
- reduced variability (k = 3).

---

# 3.5.9 Solving Balance Equations via Matrix Form

Balance equations can be written as:
```
A · P = B
```

Where:
- **A**: coefficient matrix
- **P**: vector of state probabilities
- **B**: constant vector

Solution:
```
P = A⁻¹ · B
```

This approach is:
- efficient,
- suitable for Excel or numerical tools,
- preferable for complex state diagrams.

---

# 3.5.10 Exam Notes

In exams:
- you may be asked to **draw the state diagram** and write equations, or
- probabilities may be **given**, and you compute KPIs only.

You will **not** be required to solve large systems manually.

---

# 3.5.11 Interpretation
Erlang distributions model:
- processes composed of multiple sub-operations,
- series of similar exponential tasks,
- reduced variability compared to M/M/1 systems.

---

# 3.5.12 Key Takeaways
- Erlang processing times reduce variability.
- Erlang-k is modeled via k exponential phases.
- State diagrams remain Markovian.
- Performance improves as k increases.
- Matrix methods simplify solution of balance equations.

# 3.6 M/G/1, G/G/1 and G/G/c Systems

This chapter generalizes queueing models by **relaxing the exponential assumption** on arrival and/or processing times.
Instead of exact state-diagram solutions, we rely on **approximations** based on variability.

---

## 3.6.1 From Exponential to General Distributions

Up to now, we analyzed systems with:
- exponential inter-arrival times,
- exponential processing times.

We now consider:
- **M/G/1**: exponential arrivals, general service times
- **G/G/1**: general arrivals, general service times
- **G/G/c**: general arrivals, general service times, *c* parallel machines

For general distributions, the **mean alone is not sufficient**:
- we also need the **variance** or the **coefficient of variation**.

---

## 3.6.2 Notation and Variability

### Arrival Process
- Arrival rate:
```
λ
```
- Mean inter-arrival time:
```
E[T_A] = 1 / λ
```
- Squared coefficient of variation:
```
C_A² = Var(T_A) / E[T_A]²
```

---

### Processing Time
- Processing rate:
```
μ
```
- Mean processing time:
```
E[T_S] = 1 / μ
```
- Standard deviation:
```
σ_S
```
- Squared coefficient of variation:
```
C_S² = σ_S² / E[T_S]²
```

For exponential distributions:
```
C_A² = C_S² = 1
```

---

## 3.6.3 Utilization

### Single Machine
```
U = λ / μ = λ · E[T_S]
```

### c Parallel Machines
```
U = λ / (c · μ)
```

Utilization refers to the **whole workstation**, not to a single machine.

---

## 3.6.4 M/G/1 System – Pollaczek–Khinchine Formula

For an **M/G/1** system (unlimited queue, one machine):

### Total WIP
```
WIP =
λ/μ
+ λ² · σ_S² / (2 · (1 − λ/μ))
```

This formula is **given**, not derived.

---

### Queue WIP
Since:
```
WIP = WIP_Q + U
```

We obtain:
```
WIP_Q =
λ² · E[T_S]² · (1 + C_S²)
--------------------------------
2 · (1 − U)
```

---

### Cycle Time in Queue
Using Little’s Law:
```
CTQ = WIP_Q / λ
```

After simplification:
```
CTQ =
(1 + C_S²)/2 · U/(1 − U) · E[T_S]
```

---

## 3.6.5 Interpretation of the M/G/1 Formula

- The structure is identical to **M/M/1**
- The difference is the **variability factor**:
```
(1 + C_S²)/2
```

Cases:
- `C_S² = 1` → M/M/1
- `C_S² < 1` → less variability → lower waiting
- `C_S² > 1` → more variability → higher waiting

---

## 3.6.6 G/G/1 System – Kingman (VUT) Approximation

If arrivals are also **general**:

### Cycle Time in Queue
```
CTQ ≈
(C_A² + C_S²)/2 · U/(1 − U) · E[T_S]
```

This is known as:
- **Kingman approximation**
- **VUT equation**:
  - **V**ariability
  - **U**tilization
  - **T**ime

---

### Total Cycle Time
```
CT = CTQ + E[T_S]
```

⚠️ These formulas are **approximations**, not exact values.

---

## 3.6.7 Example – G/G/1 System

### Given
- Mean inter-arrival time:
```
E[T_A] = 15 min
σ_A = 30 min
```
- Mean processing time:
```
E[T_S] = 12 min
```
- Erlang-4 processing time:
```
C_S² = 1 / 4 = 0.25
```

---

### Variability
```
C_A² = (30 / 15)² = 4
```

---

### Utilization
```
U = E[T_S] / E[T_A] = 12 / 15 = 0.8
```

---

### Cycle Time in Queue
```
CTQ =
(4 + 0.25)/2 · 0.8/0.2 · 0.2
≈ 1.7 hours
```

---

## 3.6.8 Performance Measures

Once `CTQ` is known:

- Total cycle time:
```
CT = CTQ + E[T_S]
```

- Throughput:
```
TH = λ
```

- WIP:
```
WIP = λ · CT
```

- Queue WIP:
```
WIP_Q = λ · CTQ
```

---

## 3.6.9 High Variability Example

Given:
- `U ≈ 0.95`
- `C_S² = 2.5`

Results:
- Very large `CTQ`
- Very large `WIP`

Interpretation:
> **High utilization + high variability ⇒ explosion of waiting and WIP**

---

## 3.6.10 Extension to G/G/c Systems

For **parallel machines**, the Kingman approximation is extended.

### Cycle Time in Queue
```
CTQ ≈
(C_A² + C_S²)/2
· [ U^(√(2c+2) − 1) / (c · (1 − U)) ]
· E[T_S]
```

This generalizes:
- M/M/1
- M/M/c
- G/G/1
- G/G/c

---

## 3.6.11 Key Takeaways

- Exact solutions require exponential assumptions
- General distributions require approximations
- Variability strongly affects performance
- The **VUT equation** is the core tool
- One general formula covers all special cases

Now we start lesson three. That is the single workstation analysis. Okay. So here so until the last lesson, consider that all the times were fixed values, so were deterministic values.
And, okay, this was fine just to illustrate the the basic concepts to define the KPIs and to show the relationship among them. But then it's now it's it's not enough to consider the times as deterministic. Also, because the so they they tend to reach the wrong results. So from now on, we include the probabilistic behavior in our models, especially for the arrival processing and the processing times. So we will see so at the beginning, we consider the these times as exponentially distributed.
And then because by doing these assumptions, it's possible to derive and to demonstrate the basic formulas to compute the the KPIs, so the WIP and the cycle time. And then we also see how the formulas change by considering other types of distributions. So basically, we are now introducing the variability in our model. K? So the times here are our the the variables under analysis are mainly times because we are talking about arrival times of items at the the workstation and of processing times, the time that the machine spends processing the items.
And now we are considering that these times have a variability, so are not deterministic. So the variability is defined as the not uniformity of class of entities because there is a departure from the regular behavior and its predictability. In the slides are also reported some examples of variability, such as, for instance, the machine failures. So the fact that the processing time needs to consider also the failure of the machine, so the time spent in the breakdown state. And this has an effect on both the average time and its variability.
And then other examples such as the material shortages or the operator unavailability or also the different skills level, because, different operators with different skills level, can execute the same operation with different times. So, again, there is this is another cause of variability. And other things such as material handling or product variety. So we will see later in the course how to address the fact that in the same plant, there are different product types, and each product type as follows its routing and has different characteristics with respect to the others. So by inserting the variability, we are now introducing the concept of random variables.
And so for us, random variables are the arrival times and the processing times of the machines. And a random variable is characterized by, firstly, the type of the distribution. So the distribution can be exponential, normal, log normal, and so on, and the parameters of the distribution. So, basically, the mean value indicated by the mu letter and variance that is sigma squared, the standard deviation that is the root square of the variance, and the other index such as the skewness and the and so on. In addition to these parameters, we have to define another parameter that is the coefficient of variation, and it's indicated by the c letter.
The coefficient of variation is a measure of the amount of variability of a random variable, and it's computed as the ratio between sigma and mu. The standard deviation divided by the mean value. And in the same way, it's defined also the square, the coefficient of variation, c squared, sigma square divided by mu square. So this quantity basically evaluates how the standard deviation is in relation to the mean value. This ratio is usually divided into three intervals to classify the variable as low variable, moderate variable, or high variable.
So by definition, we define c to be as to be a low variability index if its value is under 0.75, or if c is between zero point seventy five and one point thirty three, the random variable has a moderate variability. So if c is around one, it means that the standard deviation is almost equal to the mean value. And if c is higher than 1.33, then the variable is considered to have a high variability. Then let's clarify this concept by using this small example. So here we have two two processes of two students going to the school.
And so let's, assume that we are able to record all the times that, the two people spend, traveling to the school. So the first one takes twenty six minutes on Monday, then eighteen minutes on Tuesday, then nineteen in Wednesday, and so on. So we are able to compute the mean value that is twenty five minutes and the standard deviation that is 5.65 for this first example. Then we have the second one. So the second person that takes eighty five minutes on Monday, then sixty one on Tuesday, seventy four on Wednesday, and so on.
And, again, we can compute the mean value, 73.6, and the standard deviation that is 8.4. So the idea is that only computing the mean and the standard deviation is not enough to quantify the variability of these two processes. Because if we only look at the standard deviation value, we could conclude that the second process has an higher variability with respect to the first one because the standard deviation is higher. Instead, if we compute the coefficient of variation, so the value of c as the ratio between the standard deviation and the mean value, we obtain the first case 5.65 sorry, zero point two hundred and twenty six, and in the second, zero point one hundred and fourteen. So this means that, okay, both of the processes have a low low variability because c is under 0.75.
But the second one is less variable with respect to the first one because its coefficient of variation is lower. So remember that in order to quantify the variability of a process, it's not enough to only consider the standard deviation because the standard deviation is higher if the mean value is also higher. So let's do the ratio between these two values and obtain the coefficient of variation. And this is the correct index to use to measure the variability of a process. Okay.
Now why are we talking about the variability? Because the variability is the reason for which we have the queues in our system. We have the items accumulating in our system, and we we have to quantify the variability in order to use this value then to compute the performance measure of our system. So to compute the cycle time and the and the throughput. Now to better understand the effect of variability, let's consider this example.
Here we have a single so a machine represented by the the box on the rectangle with a process time of ten minutes. And before the machine, we have the queue represented by the triangle, so the inventory. So we have the item arriving at the machine. And remember that the pair machine queue is the workstation. So inside the workstation, we also have the queue and one or more parallel machines.
So we we call all these set of items the workstation. So we have the items arriving at the workstation. Then if the machine is free, the item is processed. Otherwise, the item waits in the queue before being processed. The process time is ten minutes.
We want to see which is the effect firstly of the arrival time and processing time on the the item waiting, the number of item waiting in the queue, and also on the utilization of the machine. And then understand what happen if we insert the variability in this process. So let's, as usual, redo this graph step by step by hand. Okay. So here we have the workstation that is rectangle.
And before the workstation the machine, sorry, before the workstation, we have the queue. And then we have the arrival of items. And then the item are processed. So wait in the queue, then are processed, and then exit the system. Here, let's also introduce the terms, the name of the so the the right terminology.
So we have seen that the processing time is indicated as e of t s. So the average processing time, in this case, we start with the fixed value. So here, it's a fixed value. And by using the same notation, we also insert the expected value of the arrival time. So we define by using the same notation also the average arrival time e of TA.
TA stands for arrival time. Okay. So now let's see which is the effect of changing the arrival time and the processing time on the number of items waiting in the queue and also on the utilization of the workstation. Here, let's also introduce the formula to compute the utilization of the work station. So the utilization of the work station is given by the processing time over the total time that in this case is the arrival time.
So let's define the utilization as e of t s divided by e of t a. And we see in a moment how we use it and we compute it. Then let's draw the graph where we want to represent on the x axis the utilization of the machine. So let's just write here utilization. And on the y axis, we have the items waiting for processing.
This is the number of items waiting waiting for processing so that they are in the queue. Okay. Now let's fix some values for the times. In this example, we consider the processing time fixed to ten minutes. And let's see how the utilization and the number of items waiting change by changing the arrival time.
Let's start with the first case a, where the inter so the arrival time is better called interarrival time because it indicates the time between two arrivals. Okay? So the interarrival time in the first case is thirty minutes. Let's consider that e of TA is thirty minutes fixed deterministic. Okay.
So if we have a new item arriving every thirty minutes and the processing time is ten minutes, so which is the utilization of the machine? Well, the machine works ten minutes every thirty minutes. So its utilization is 10 over 30, that is 0.33. And which is the number of items waiting in the queue? Here, when a new item arrives, it always find the worst the the machine free.
Because the new item that then it is processed for ten minutes, then the machine is free for the other for other twenty minutes until the next item arrives. Okay? So in this configuration with an inter arrival time of thirty minutes and the processing time of ten minutes, we have an utilization here of 0.33 and a number of items waiting equal to zero. So this point here is called point a. It represent the situation the situation.
Then now let's decrease the interarrival time. It means that we are increasing the rate, so the rapidity in which the items arrive at the system. So now let's consider that e of t a now is twenty minutes. So each twenty minutes, a new item arrives. So in this case, which is the utilization of the machine?
Well, the first item arrives, it is processed for ten minutes. Then there is a waiting time of ten minutes until the second item arrives. Then there is a processing time of ten minutes and so on. So the utilization is 10 over 20, so 0.5. And again, when the new item arrives, the machine is always available, so no item waits.
And here we have a point b, 0.5, and this is point b. Then now let's consider that the times are the same value. So both the arrival time and processing time are ten minutes. So here we have the first item arrives. It is processed.
Then as soon as it exit the machine, the new item arrives, it is processed, and so on. So we expect an utilization of one, ten over ten, one. So the utilization is a value between zero and one, also expressed in percentage, so between 0100%. So here, we insert the point to see there where the utilization is one. Then now what happen if we gone and we insert an interarrival time lower than the processing time?
So e of t a is any value lower than 10, even 9.999. K? Even even this this value works in the same way as all the other values lower than 10. In this case, well, the utilization cannot be computed by using the formula because for the workstation, it's not possible to reach a utilization higher than 100%. The machine cannot work more than its capacity.
So the utilization remain one. But the effect is that the queue start growing. So we start accumulating the items in the queue. And here, in this case, can we estimate which is the number of items in the queue? So do you think that the number of items in the queue reaches a steady state value?
Well, let's think about what happened. We have the first item arriving, then one minute or zero point one minute before it finishes the processing, the second item arrives. So then the first item finishes the processing, the second items starts the processing. In the meantime, zero point two minutes before the second item finishes the processing, the third item arrives and so on. So this behavior, since we have this condition where the machine is slower than the arrival of the items, causes the queue to tends to infinite because the items start accumulating and never stop until we stop the arrivals.
So here the effect on our graph is that the point d is there. So where the number of items waiting tends to infinite and the utilization remains one. Okay? This this example make so let us understand that if we don't have the variability, so in this case, we are only considering considering fixed values. And if we don't have variability, then we cannot apply the q theory to the production systems because or we don't have any queue, so we don't have any items waiting, any waiting times, the queues goes to infinite.
And thus again, it's not possible to compute the waiting time or the cycle time of the items because it is always increasing as soon as we increase the number of items arriving to the line. So this is the first point. If we don't have any variability in our processes, then we cannot apply the q theory because the q are all zero, always zero, or always tend to infinite. So here we have so let's introduce the variability only in the arrival time. Okay?
So let's just consider that the processing time is constant, fixed at ten minutes, but we add the variability in the arrival time. It means that now the items, the the time between the arrival of one item and the following item is always different from the previous one. Now let's now consider, the the figure. Well, we reported in the table the arrival time and the start of process for the first six items. So we have the first item a that arrives at time zero.
The machine is available, is free. So it's it starts the processing. So the processing start at time zero and ends at time ten. And this is also represented here in the in the figure. Product a started time zero and end at time ten.
Then the second items b arrives at time twelve. So we have two minutes where the machine is idle. This is the blue part in the figure here. Then at time twelve starts the processing of part b, and it ends at the time twenty two. Then item c, the third item, arrives at time twenty.
But at time twenty, the machine is busy processing the previous item. So the third item waits for two minutes in the queue, and then start the processing at time twenty two, and set time thirty two, and so on. Then other items arrive. So if you see if you compute the interarrival times, you see that between the second and the first, we have twelve minutes. Between c and b, we have only eight minutes.
Bif between d and c, we have fourteen minutes and so on. So it means that we are we have we added the variability in the arrival process. So in this case, the items arrives at different times. Which is the effect of the workstation? The workstation sometimes is free and sometimes is occupied.
And this causes the fact that we have the items in the queue sometimes when the item found finds the workstation, the machine busy processing the items. Okay? And so this is our case application study. Because even if only if we have the variability, we are able to compute and to estimate the average number of items in the queue and the average waiting times. And in the following of the course, we see which are the formulas to compute this quantity.
Then if we come back to our graph, by adding the variability, which is the effect, The effect is that we move from the original graph with the point a, b, c, and d to this second graph, where the effect is that if we increase the utilization, so as much as we increase the utilization, if we have the variability, then the number of items waiting in the queue start increasing. Why? Well, before, if the utilization is high, it means that the machine is occupied for the majority of time. And, thus, it's more probable that the item arriving at the machine find it busy. So this is the effect of adding the variability.
We have we start increasing the number of items in the queue if the utilization increases. This is the effect on the graph. Then here in the first graph, you can see that the utilization so the the number of items waiting increases if the variability increases. Instead, if the variability decreases, then the the graph tends to the original one, the one that goes until 100 with a very low number of items waiting. So here, the idea is that since in order to optimize the the performances, we want both to maintain a high utilization.
For instance, being in point x, so having a high utilization, but usually this is associated with a high number of items waiting. Instead, we also want a low number of items waiting. So being in point y, even if the drawback is that here, we needed to decrease our utilization rate. So it means not exploiting very well the machines that we have if we we don't use them for the 100% of their capacity. So it means losing money, the investment.
So the idea is try to obtain both by reducing the viability. So instead of following this cure over here, if we are able to decrease the viability, maybe we are able to follow this other cure over here and thus being in point zed. So obtaining both high utilization, so utilization more than 90% with a very low number of items waiting. Okay? So this this graph is to fix this concept.
So in the real cases, in the real world, we have the variability. The variability is the reason for which we have the cues, and we can apply the q theory. And in general, we need to reduce as much as possible the variability of our processes in order to obtain better performances. So in order to be able to reach a high utilization but maintaining low the waiting times. Okay?
This is the concept that you need to to remember and maybe also to rethink about it to be to be sure to be convinced that this is the case. Anything any points here? From time to time, I try to read the chat. So if you write something, I I read I read from time to time. Okay.
Let me show you a simulation model that is this one that basically represent the system that we have seen at the beginning. Here in the model, we have the source, so the generation of items, and the processor, and the queue. So the items are generated by the source. They with a specific inter arrival time that follows a distribution. And so let's set it at the beginning to be a deterministic value, such as twenty minutes.
So now I am fixing an interarrival time of twenty minutes. And the processor here, in the processor, I set a process time of ten minutes, such as the case b in the in the graph that we have seen last time. And then if I reset and run the simulation, We see here in the dashboard that the utilization is 50%. So we have 50% of time that the machine is processing, and the 50% of time it's idle. And then we don't have a whip in the queue and neither waiting time in the queue.
So in the whip and cycle time objects, we see that inside the queue, have zero items and zero waiting time. Then, we have seen that if here I insert a number equal to the processing time. Again, so here I obtain a utilization of 100% and, again, zero and zero items and waiting time in my system. And then if I stop the simulation and insert a number that is lower, so now the items are arriving faster than the processing time, so 9.5. And then let's run the simulation again.
And here you can see that the number of objects in the queue start way start increasing, and it goes on and tends to infinity. So now we have simulated the deterministic case. Now let's introduce the variability now. So let's stop system and introduce the variability. So here in the interarrival time, I insert a distribution instead of a deterministic value.
So here I select statistical distribution. And for instance, I keep this function, log normal mean and standard deviation. So I can set we can see the effect of the variability by using a distribution with a mean and the standard deviation. So here, let's keep an interarrival time higher than the processing time. And a very low standard deviation.
So it means that the variability of this process is low, low variability. The variability, remember, that is defined by the ratio of the standard deviation and the mean value. The coefficient of variation is the index that we use to evaluate the variability of a system of a process. So this is the so log normal with the mean value twelve minutes and the standard deviation three. And so here, if I run the system well, and I leave the system run for for a long time, we see that, the average WIP and the average stay time in the queue start increasing.
So here, the utilization is always the same value of the deterministic case. So the utilization is computed only by using the average value. So in this case, it's 10 divided by 12, the average values of the processing time and the interarrival time. Instead, here we see that the waiting time, the average waiting time started to, being 0.15. And, here, if I increase the variability, so if I increase the standard deviation, so here I put 10, for instance.
Let's see the effect. You see now the the average number of items waiting is 1.2, and the average waiting time is fourteen minutes. So you see that if I increase the variability, the effect is that the waiting time is increasing and also the number of items waiting. So this is why we we say last time that the variability is something that it's better trying to reduce it. And here, we can also observe that if we increase the utilization so in order to increase the utilization, we fix here the average interarrival time near to the processing time.
For instance, we decrease at, let's say, 10.5. And here, so if we maintain the same variability, here the effect is that you see the utilization increased. And, also, the average WIP and the average waiting time increases. Because if you remember the graph of our example, so this one, we are here around point x. So with the high utilization and average variability.
Instead, if we decrease the utilization and maintain the same variability, we are around point, here, y. And as we say that in order to obtain a better trade off, so trying to optimize both the waiting time and the utilization, our best option is trying to reduce the variability in order to maintain the same high utilization, but also low waiting times. So here, if I want to maintain the same utilization, but reduce the number of items waiting and the waiting times, Here, I I I have to try to reduce the variability. For instance, he's if here I put a variability of three instead of 10, Here, the effect is that the utilization is the same, and the waiting time and the average number of items waiting is lower. And thus this correspond to point zed in our original graph.
Okay? So this is just to summarize and clarify the things that we have already seen by hand last time. You can also develop a very simple simulation model and try in order to be convinced that how these concepts are related. Okay. Then let's stop it and close it.
And then here, I have another model. So if you want, I can also upload these models in FlexSim if you want to have a look at them. This is instead is the model of the limited system. If you remember also last time, we analyzed and we we solved the we computed by hand the WIP and the cycle time of a limited system. So here, the limited system is given by the fact that we limit the number of items in the queue.
So inside the queue, we insert the maximum number of items at two. So we have at maximum two items in the queue and one item in the processor. So the maximum whip is three in this case. Then I inserted here the parameters of the source. The source follows an internal an exponential distribution with average time 0.2.
And the processor, the process time follows an exponential distribution of average processing time is 0.25. So if you remember, we had the the rate in the text that was four and five jobs per day. So they were translated into the corresponding times. And here, again, if you reset and run the model, here you obtain the performances that we obtained analytically by using the formulas. So the psych the total cycle time, that is the sum of these two terms.
The cycle time in q, 0.28. And then the total WIP, that is the sum of the two terms and the WIP in q.

Starting by computing the parameters, so the WIP and the cycle time by considering a small example. Here, this is a simplified example, and it's a limited system. So now we are limiting the number of items that can enter into the systems and being inside a system at the same time in order to be able to use the formulas and solve them in this small example. So let's read together the text. We consider a facility with a single machine that is used to service only one type of job.
The company policy is to limit the number of orders accepted at each time to three. So this is a limited system because we cannot accept more than three jobs in the system. If, in this case, if a new job arise, it is discharged, so it cannot be accepted. Then we know the input parameters. The input parameters are the arrival rate and the processing rate.
And remember that the rates are the inverse of the times. So here we have the mean arrival rate of orders called lambda. That is five jobs per day. And the mean processing time for job is one fourth of a day. Thus, the processing rate, from now on, we call the processing rate as more of four jobs per day.
Both of the processing and the interarrival times are assumed to be exponentially distributed. Okay? So as I say before, at the beginning, we assume that the distribution are exponentials. Because in this way, we can apply the formulas and derive the final ones. Let's represent this example in this way.
Okay. So here, we wanted to represent this system by using the state diagram. So it means that we represent each possible state of the system. And for a state so each state is identified by the number of items inside the system. So here are the step.
We start representing the state diagram. So by identifying the states and then representing the graph that link all the states by starting the arcs that represent the movement from one state to another. Then our objective, our final objective is to find the probabilities of being in each state because this probability is used to compute the average WIP, so the average number of items in the system. Okay? So let's do as usual all the steps together in the board.
And let's start by defining, the state diagram. Well, firstly, let's record the input data. So for this example, we have WIP level. So the maximum WIP WIP level equal to three, And we have the arrival rate indicated with lambda as five jobs per day, and the processing rate that is indicated with the letter move as four jobs per day. This is our starting point.
So first thing is to draw the state diagram of this system. So we start one node for each state, and the state means the number of items in the system. So in this system, we have a state zero because at the beginning, we have zero items in the system. Then we can have a state one when we have one item in the system. Then state two, two items in the system, and state three with the three items in the system.
Then since the whip level is three, so we limited the number of items in the system, we cannot have other states. Now let's insert the arcs to represent the movement from one state to the other. Here, if we are in state zero, the only thing that can happen is that the new item arrives. Okay? So state zero is connected with an arc, with state one.
And inside the so near the arc, insert rate at which this movement occurs. That in this case is the arrival rate lambda. So here we insert lambda on this arc. Okay. Now we are in state one.
In state one, what can happen? Well or a new item arrives when the machine is still processing the previous one, and thus we move in state two. So at this point, we have two items in the system. The system is always composed by the machine, one normal machine, and the queue before the machine. So we can move from state one to two again with rate lambda, or it can happen that the items finish the item finishes the processes, and thus from state one, we move back to state zero.
And here, the rate at which we move from one to zero is more. That is the processing rate. And so nothing else can happen from state one or the movement to state two or the move back to state zero. Now let's address the state two. State two, the same reasoning.
So when we are in state two or a new item arise and thus we move in state three with rate lambda, or we move back to state one with rate move. And if we are in state three well, if we are in state three, it cannot happen that the new a new item arrives because the new item is discharged if the system is already full. So the only thing that can happen is that we move back to state two, again, with rate move. Okay? So this is the state diagram, the diagram model of the system.
So we insert all the possible states as nodes of the system, then we insert the arcs. And then we insert the rates. And this is so this is why we use the the exponential distribution because this model of the system is possible only because the processing time and the arrival times follow the exponential distributions. So it means that the next state only depends on the current state and not of all the other previous states. So this is the reason for which in this example we are able to draw the state diagram.
Instead, if we add other distributions, it's this is not true, this assumption. Okay? Okay. Now now that we have the state diagram, our aim is to find the probability of being in each state. In order to find the probabilities, we need to cut the graph and write the balancing equation.
Okay? So here, for instance, we can cut this graph here and write the balancing equation that is the probability of being in state zero multiplied by lambda. That is the rate at which we move. So the probability of staying in of being in state zero multiplied by the rate of movement from zero to one should be equal to the probability of being in state one multiplied by the rate of movement from one to zero. If this equation is true, it means that our system reaches the steady state.
So the equation are balanced, and thus the probabilities reach the daily steady state values. Then we repeat the same procedure for the other cuts. So we cut again the graph here, and so we wrote that p one multiplied by lambda is equal to p two multiplied by mu, and another cut here. So p two multiplied lambda is equal to p three multiplied mu. And now, so we have four unknown variables that are p zero, p one, p two, and p three, but only three equations.
So in order to be able to solve the system, we add the norming equation. So the equation that is valid for all the probabilities, that is that the sum of the probabilities is equal to one. So let's write this final equation. So p zero plus p one plus p two plus p three is equal to one. So the sum of all the probability is equal to one.
And this is the system that we have to solve in order to find the probability values since lambda and mu are known variables. So we know in in this example the value of lambda and mu. So now let's express the first equation in this way as p one in function of p zero multiplied by the coefficient lambda over mu. So we can rewrite the first equation in this way and all the others. So also p two can be written as lambda over mu p one, and this is equal to lambda over mu squared multiply p zero.
Then we write also p three in the same way. So p three is lambda over mu multiplied p two and can be rewritten as lambda over mu at three power multiplied p zero. So now that we have expressed the p one, p two, and p three in function of p zero, we can insert them in the last equation and then solve by finding p zero. So we have p zero plus lambda over mu p zero plus lambda over mu square p zero plus lambda over mu three power multiplied p zero equal to one. And from this equation, we obtain p zero as one divided by one plus lambda over mu plus lambda over mu squared plus lambda over mu three power.
K. So now by substituting the numerical values, we obtain the value of p zero for this example. So let's compute p zero as one divided by one plus in our example, we have lambda equal to four five and the mu equal to four. So plus five over four plus five over four squared plus five over four three power. And the result of this computation is 0.173.
Then we can go on and inserting this value also to compute the other probabilities. So p one is equal to five over four multiplied p zero, zero point one seven three. So the result is 0.217. Then p two is five over four multiply p one, zero point two one seven. And the result is 0.271.
And p three is five over four multiplied 0.271, so 0.339. Okay. So we are able to find the probability of being in each state. So p zero zero point one seven three represents the probability that there are zero items in the system. So it also represent the probability that the machine is idle.
So probability that there are zero items in the system does, the system is idle. Then p one is the probability of having one item in the system, p two the probability of having two items in the system, and three the probability of having three items in the system. And this quantity also represent the probability that the system is full probability that the system is full. Okay? Okay.
Now now that we have these probabilities, we can we are able to compute the average WIP of the system because the WIP is the average number of items in the system. Now we have the probability of having each number of items in the system. So the formula of the whip by using this probability can be expressed as the whip is the sum for n from zero to three, in this case, of n multiplied p n. So we multiplied n, that is the number of items in the system, for its probability, and then we sum all these terms, and we compute the average numbers. This is the standard formula to compute an average value.
So we multiply the value by each probability by its probability. So in this case, we have p zero multiplied by zero. So this term is excluded. Then we have p one multiplied by one plus two p two plus three p three, and stop. So p one is 0.217 plus two that multiplies 0.271 plus three that multiplies 0.339.
And the sum of all these terms is 1.776 jobs. Yeah. This is the average number of jobs inside the system. Then then what about the other performance measures? Well, now let's analyze the throughput value.
So the throughput value in this case so usually the throughput is equal to the arrival rate of lambda. But in this case, no, because this is a limited system. Okay? So for the if we are talking about unlimited system unlimited systems, the throughput is equal to lambda because all the items that enter also exit the system. So the throughput is equal to lambda.
Instead, for the limited system, the throughput is not equal to lambda, but is lower because we have the items arriving at the system. But if the system is full, then the item cannot enter the system, and thus it's discharged. So after the system, so the number of items waiting from the system is lower than the number of items and arriving. And how we can compute this quantity? Well, this quantity is called lambda effective, abbreviated as lambda e, lambda effective, and it's computed as the total arrival rate minus the arrival rate that is related to the system full.
So the arrival rate multiplied by the probability that the system is full. Okay? This is these terms represent the rate of jobs lost. K? This is the rate of jobs lost because the system is full.
So in this case, lambda is five, and we we do five minus five multiplied 0.339. So the probability that the system is full. And the result is 3.305 jobs per day. Here, the time unit is the day. Okay?
So we have computed the throughput of the system. And then let's compute also the cycle time. The cycle time can be computed by using the little slow. Since we have the true the WIP and the throughput, so the cycle time is equal to WIP divided by throughput. So the WIP is 1.776, and the throughput is 3.305.
So the cycle time is zero point five three seven days. Then now we have computed the whip whip is the the average number of item in the system. And the system is composed by the machine and the queue where the items wait. Now if we want to compute not only the total whip, but also the whipping queue, that is the average number of items waiting in the queue, how can we do it? Now we want to compute the weeping queue.
It is the average number of items waiting in the queue. Okay? So here in our system, so we have here we have the queue and the machine that's represented there. If we have zero items, then each both these elements are empty. When we have one item, then it is processed by the machine.
So this is state one. Then if a new item arrives, it waits in the queue. So this is the representation of state two. And when if a new item arrives, when the first one is still processing, then it waits in the queue. So this is the representation of state three.
And we have already computed the probability of being in each state. Now we want to compute which is the average number of items in the queue. So we use the same formula. So the sum, let's change here the index, use k instead of n, from k from zero to which is the maximum number of items in the queue. It's true because we have a maximum of three items in the system, and in the machine we have only one item at maximum.
So here the sum is four k from zero to two. Do the multiplication k multiplied p k. Well, in this case, k is the number of items in the queue, and p k is the probability of having this number of items in the queue. Queen. So probability of having k items in the queue.
Okay. So let's now expand this expression in our example. Okay. Zero items in the queue. The first term doesn't matter.
Then if we have one item in the queue, which is the probability of having one item in the queue? So one item in the queue, we are in this situation. One item here and one item in the queue. So the probability of having one item in the queue is the same of having two items in the system. So here I write one multiplied p two.
And then we sum two, that is the probability of having two items in the system, that is this graph here, that corresponds to the probability of having three items in the system. So two multiplied p three. Okay? So by using the probabilities that we computed previously, we are also able to compute the average number of items in the queue by solving this equation. So we have p two that is 0.271 plus two multiplied 0.339.
And the result is 0.95 jobs. So 0.95 jobs is the average number of items in the queue. Instead, 1.77 is the average number of items in the whole system. And then how to compute also the cycle timing queue. So the cycle time in q well, to compute the cycle time in q, we can remember the first formula that we have seen together.
That is cycle time is equal to cycle time in q plus processing time EOTS. In our exam so the cycle timing queue is cycle time minus EOTS. And in our example, which is the value of the processing time, it's the inverse of the processing rate. So one over four zero point twenty five days. So we can use this formula and compute also the cycle time in queue.
The cycle time is zero point five three seven days minus zero point twenty five days, and we obtain a value of zero point two eight seven days. Or, the same value could be computed again by using the little slow. So the throughput is always the same. Here, we have computed the whipping queue. So another way of computing cycle time in queue is doing whip in queue divided by throughput.
From 0.95 divided by the throughput that was 3.305. And, again, the same result, zero point two eight seven days. So these are our performance measures that we we want to find in all the examples. K? So here, the idea was by using this small example, the limited system.
So using the limited system in order to be able to solve numerically the exercise. Okay? And to see how to write the formulas. So we can write the formulas, and then we will see next time how to extend these formulas also in the unlimited system. So we can extend the same formulas.
So try to understand while the formulas and all the steps in this small example so that the next time when we see the formula for the unlimited system, everything is already clear. And then we solve it numerically. So in this in this case, it's possible to write the system of equations and then solve the system by substituting the values and find all the probabilities. And once that we have the probabilities, we are able to compute the WIP and the and also the throughput. And then by using the WIP and the throughput, we compute the cycle time.
Then when we talk about the performances of the system, it's not enough to compute WIP throughput and cycle time, but we also want to compute the WIP in queue and the cycle time in queue. Because in this way, we can compare the total cycle time with the cycle time in queue. So here, the total cycle time is 0.537, and the cycle time in q is zero point is that the cycle time and the processing time are are very similar. And so a medium result, let's say, not not very good, but neither. Okay.
So let me come back for a minute to to the slides. So here we are at the state. Then the building of the graph, the cutting of the graph to obtain the balancing equations. Here are all the equations. Then they know also the norming equation to have four four equations for four variables.
And then the numerical solution of the probabilities. Then the computation of so the meaning of the probabilities. So p zero is the percentage that the server is idle because there are no items in the system. And p three is the probability of having three items in the system, thus that the system is full. And then the formula to compute the whip by multiplying the number of items by the probability of having this number of items, and then summing all the terms.
And we obtain this WIP value. Then the number of job of jobs lost per hour, that is lambda multiplied p three, so the probability that the system is full. And we obtain this number of jobs lost per hour, so the lost job rate. And then the throughput computed as the original throughput minus this quantity, so 3.305 jobs per day. And finally, by using the WIP and the throughput, we can compute the cycle time.
Then again, the definition of the arrival rate, so more formally, as a lambda that multiplies one minus p over n max. Okay. This is the formula valid for each system. Also, if we have a different number of dates. And and stop.
Here, it's not reported the formulas to compute the weeping queue and the cycle time in queue. Okay? But you have it on the on the recording.

Okay. So let's just go on by introducing the queuing system. Here, this theory was developed in 1917 by mister Erlang that firstly applied this theory to the telephonic sector in order to estimate the waiting time of a call. But then the the theory can be applied in a lot of different context, such as the customers that wait at the bank or the post office, then also the patients that arrive at the doctor and wait to be served, or the people waiting for the taxi. Okay.
So now we we just see a specific application that is the arrival of jobs or components, items needed to be processed by the workstations. But the theory can be applied in every context where we have an arrival rate and a processing rate with that basically delay the items. Here you have description of the main elements of the queuing system. So the queuing system is composed by an arrival process. So in our case, we have the arrival process of the items to the first workstation.
At the beginning, we consider only single jobs, and then we see how the formulas change if we consider the batches. And we have seen that the times can be deterministic or stochastic. K? So we have the arrival process characterized by the distribution of arrivals from which we derive the average arrival times or the average arrival rates. Then the second element is a service process or a production process.
So the machine that processes the items. The machine can be single or parallel. So, again, we start by considering a single machine, and then we see how the formulas change if we consider more parallel machines inside the same workstation. And again, the service time, the processing time can be deterministic or stochastic. And finally, we have the queue.
The third element is the queue. The queue is a place where the items can accumulate and wait until the machine one of the machine is available to process them. The queue can have a rule to insert and destruct items, such as FIFO, LIFO, first come, first served, or last come, last served. But this this rule, this logic is not involved in the theory, so we can assume that the order is first come, first served. And the other parameter is that it can be limited or unlimited.
K? So when we wanted to define a limited system, we fix a maximum number of items that can wait in the queue. K? This is the way in which we define a limited system, because in the machine, only one item at a time can enter. So in order to limit the number of items in the system, we limit the number of items in the queue, the maximum number of items in the queue.
Yes? Yes. No. 10 plus one. So if we limit the queue to 10 and we have one machine, the system is limited to 11 items.
Machines, you mean? No. Okay. No. No.
No. No. No. Here, one system so one system defined as a queue system is one arrival process, one queue, and one or more parallel machines. Okay?
If we have multiple systems, so each workstation is modeled as one queue and one or more parallel machines. If you have another workstation, again, the second workstation is one queue one or more parallel machines. So you cannot have a parallel queue inside the same workstations. It's another they they are two different systems. Okay?
Okay. Then each system can be defined, can be so characterized by using the Kendall notation. The Kendall notation is a sort of summary of the system because it specified specifies five better four elements of the system. So it's a string, a list of characters separated by the bar. And in the first element, specify which is the type of arrival arrival process.
In the second term, we specify the type of the service process, so the the processing type. In the third element, we specify the number of parallel machines in our system. In the fourth, maximum number of elements allowed in the system. And in the fifth, but the fifth is we we never use it, is the q discipline. So if you want to specify that the q is not first in, first out.
An example of the Kendall notation is m m one three. So one letter to identify the arrival process, one letter to identify the service process, one number to indicate the number of parallel machines, and another number to indicate the maximum number of items allowed in the system. Okay. So in the first two positions, we have a letter. What is the meaning of the letter?
The meaning is the type of distribution. If we write m, it means that the process follows exponential distribution, where m stands for Markovian distribution. That is, in this case, a synonym of exponential. So if the first symbol is an m, it means that the arrival rate follows an exponential distribution. If the first letter is g, it means that the arrival rate follows a general distribution that is not exponential.
Okay? So the distinction is between m and g, m for exponential distributions, and g for all the others. Because in our cases, the formulas are different if we are in the exponential case and in all the other cases. So we don't have a specific formula for each type of distributions. Okay?
We only have one more simple formula for the exponential distributions, and this is the one that we will derive in a minute. And for all the others, we have other formulas, only one general formula. Okay. So we use then d if the arrival rate or service rate are deterministic, and e of k if they follows an Erlang distribution, and we will see later what is the meaning of the Erlang. The Erlang is a specific function given by the combination of exponentials, and we will see why it's important.
But in general, the main distinction is between m, so exponential distributions, and g, so general distribution, not exponential. Okay. Then the q rules are not relevant for the course, so it doesn't matter. Another thing is that so no. Sorry.
Come back to the example of the other slide. So this example, m m one three means that we have a system in which the arrival rate follow an exponential distribution. The processing rate follows an exponential distribution. We have one machine in the system and a limit of three items, a total of three items in the system. Okay?
It's an a limited system. For the unlimited systems, the last number is infinite. In this case, we can omit it in the string. So if instead of m m one three, we only write m m one one, it means that the system is unlimited. Okay?
And this is what is written here. Okay? So now the procedure that we follow is this one. We start with the simple case, and the simple case is m m one infinite. So consider an unlimited system, So the queue is not limited.
We can have as many items waiting as needed. And both the arrival times and the processing times follows exponential distribution. Okay? Thus, considering this system, let's repeat the procedure that we have seen before to derive the formula of the WIP. In this case, we cannot use the system of equations and then substitute one equation in the other because the system is infinite.
But the procedure is the same. So now let's do together step by step the analysis of this case in order to write the final formula to compute the WIP and then the cycle time, and and that's it because the throughput is equal to lambda. Okay? Let's do it together. So now we are in the unlimited system.
Of type m m one. K. So in this case, the diagram is unlimited. So zero, one, two, and so on. And the structure is always the same.
Lambda, we move forward with rate lambda, and we move backward with rate move. Here, so if you remember from the equations of before, so from the system, Okay? So we start from the system here, and we generalize the formula of p. So p one is written as lambda over mu multiply p zero. Then p two is lambda over mu square multiply p zero, and so on.
So we can extend this formula by writing p n equal to lambda over mu at n power multiply p zero. K? So if we go on by applying these these formulas so from here, we can write p n as lambda over mu at n power multiply p zero. This is the generalization of the previous rule. Then the other formula that we have seen, p zero, so by using the norming equation we obtain that p zero was equal to one plus lambda over mu plus lambda over mu squared plus, and so on.
So also here we have the same formula that we have seen before. Before it finished at the power of three, here it goes on. This sum of terms at the denominator can be rewritten as the sum for n from zero to infinite of lambda over mu at n power. And if we rewrite this formula in this way, we can recognize that this is the geometric series, and thus we know the value of this sum. This is the geometric series, and the value of this limit is equal to one divided one minus lambda over mu.
If lambda over mu is lower than one this is a property of the series of the geometric series. We are in the unlimited system. Why? We are sure that the lambda over mu is lower than one. Why in this in the unlimited system, we have lambda lower than mu?
Okay. Let's not answer now. Let's think about it. We will see later. Okay.
So p zero saw can be written as one divided by one divided by one minus lambda over mu. So solving the equation, we obtain one minus lambda over mu. Okay. So now we use this value here in the first equation of this page, and we rewrite p n as lambda over mu at n power multiplied by one minus lambda over mu. Right?
So we are able to define the probability of of being in each state by using this formula. Now let's apply the formula to compute the WIP as before. So before we wrote the WIP is equal to the sum for n from zero in this case to infinite, so for all the possible states, of n multiplied the probability of being in each state, the same formula for the limited system. Now let's expand this formula by using this value of p n that we computed. So we rewrite the formula, n equal from zero to infinite of n that multiplies one minus lambda over mu multiplied lambda over mu.
K. Sorry. I just inverted the two terms. Let's extract this term from the sum since it's independent from n. And this formula is rewritten as one minus lambda over mu that multiplies the sum from zero to infinite of n multiplied lambda over mu at n power.
Now these are just algebraic steps. Okay? Just because in this way, for the first formula, we can see the complex demonstration. Okay? Then for the others, we we don't do it because it's too complex.
But for at least the first one, let's do it. Now let's express this other term here as so this is a quantity to n power. I want to decrease the power of one. And so this term can be rewritten as lambda over mu multiplied lambda over mu at n minus one. In this way also this first coefficient can be moved outside the sum.
So let's rewrite the formula as one minus lambda over mu that multiplies lambda over mu that multiplies the sum from zero to infinite of n multiplied lambda over mu n minus one. Okay. So all these steps in order to have this final sum, because again this is a known term. So we know that the result of this sum is one divided by one minus lambda over mu squared. Always see if lambda divided by mu is lower than one.
The same condition of of the geometrical series. Always under this condition. So if the condition is yes. Yes. This is you you are answering my previous my previous question.
Okay. Let's see it in a moment. Yes. Yes. Okay.
Then let's go on solving the the steps. We have one minus lambda over mu that multiplies lambda over mu that multiplies one divided one, one minus lambda over mu at two power. So this simplifies with this one. And we can rewrite the formula as lambda over mu divided one minus lambda over mu. Now lambda so let's come back for a minute to this quantity lambda over mu.
If you remember, at the beginning of the lesson, defined the utilization. Do you remember? The utilization was defined as E divided E. Here we have have said that the processing time is the inverse of the processing rate, and the processing rate is mu. So E of ts is equal to one over mu, and the same for the processing time.
So this is equal to one over lambda. So another way of calling the utilization is lambda over mu. This is the utilization. K? Can be computed by using the times or the rates.
So if we compute the utilization of the workstation, then we can write the WIP, so the average number of items in the system, as utilization divided by one minus utilization. Then in the unlimited system, which is the throughput? The throughput is equal to lambda, the arrival rate for the unlimited system. So we have the WIP and the throughput, and we can compute the cycle time. Cycle time is WIP divided by throughput.
So the whip by using lambda and mu, so we can simplify something. So lambda over mu divided one minus lambda over mu divided by lambda. So lambda simplifies. And then if you solve the computation, so one divided mu that multiplies one minus lambda over mu, and this is equal to one divided by mu minus lambda. Okay.
So in this case, we have written the formula of the WIP and of the cycle time and also the throughput. But in the unlimited system, the throughput is always equal to lambda, so we don't have other computations to do. So we have written the shorter formulas because these formulas are simple, but they are valid only for this kind of system m m one, where we have the exponential distributions. Okay? So this formula of the WIP and the other formula of the cycle time are valid for systems described by the Kendall notation m m one.
Now let's come back to the slides. Okay? Can I change? Yes. K.
So in the slides, you have all these things. So the formulas. Okay. The property of the geometric series, then the the the definition of the utilization factor, and then the final formula of the WIP, u divided one minus u, and cycle time by using the little slow. Okay?
Now let's see an example of application of these formulas. K. Now we have just seen the demonstration, but I don't ask you to repeat the demonstration. Okay? Just to see one demonstration for the simple formula.
Let's see this example. So we have a single server system with exponentially distributed interarrival times and exponentially distributed service time. Four jobs per hour arrive for service, and the mean service time is one over five hours. I don't understand the second sentence. It's there is something missing at the beginning.
Maybe consider again. So consider four jobs per hour and so on. Compute the workstation performance measure. K. So when the question is to compute the performance measure, which are the performance measures that we want, performance measures of the system.
Throughput, WIP, cycle time. Okay? This is the meaning. Performance measures, throughput, WIP, and cycle time. So let's solve together.
We have a single server system. So example m m one With lambda, what is the value of lambda? Four? And is five jobs per hour. And so remember that from the rates, we compute the times.
So e of t a is one over lambda, one over four, and e of t s is one over mu. Okay? Remember that the rates are the inverse of the times. Then let's compute the performances. So let's start by computing the utilization.
So the utilization of the workstation. Also, the utilization can be seen as a performance measure. The utilization is lambda over mu, so four over five, zero point eight, and then the WIP. From the utilization we compute the whip by using the formula that we have seen, u divided one minus u. So 0.8 divided by one minus 0.8.
That is four jobs. Then the throughput, which is the throughput, lambda, four jobs per hour, and the the cycle time by using the little slow. WIP divided by throughput, so lambda. So four divided by four, it is one hour. These are the performance of the systems.
Now let's compute also the corresponding value of the queue only, so the cycle time in queue and the weeping queue. What is the cycle time in queue? Or no. Cycle time is one minus so cycle let's write cycle time minus e of t s. So, yes, one minus 0.2.
Correct? Zero point eight hours and the weeping queue by using the little slow throughput multiplied cycle time in queue. Four multiplied 0.8, 3.2 jobs. K. So in a system of type m m one, so with exponential distribution of times and one machine and unlimited system, we use these formulas to compute the performance measures.
Here, in the next slide, you have also the answers of other questions, such as which is the probability that the server is idle. Also in this case, when we addressed the problem of the limited system, we compute the the probability of being in each state. So p zero, p one, p two, and p three. Also in this case, we can compute these probabilities. For instance, the probability that the server is idle can be computed by doing one minus the utilization factor, because the utilization represents the probability that the server is busy so that the machine is running and does that the system is empty is not empty, is not zero.
So if we want the probability that the system is empty and does that the server is idle, we only do one minus the utilization. So in this case the utilization is 0.8, and thus the probability that the server is idle is 0.2. And then for the other probabilities we use the general formula of Pn that we have written. So Pn is lambda over mu, that is the utilization at n power divided by multiplied by one minus u. And in this way we can also compute the probabilities of being each state.
Remember that in the unlimited system we cannot do the system of equations and solve the system because the number of equation is unlimited. So we cannot use the same process as before. Okay. Now it's your turn. So let's read together the exercise and solve it by your own.
You have an m m one system with an arrival an average arrival rate of 2.875, and an average processing rate of three jobs per hour. Considering the consider that this follow exponential distribution. Okay? So the system is m m one. Let's answer to the questions.
Which is the utilization factor of the workstation? What is the probability that there are no jobs at the workstation? What is the average number of jobs lost per hour? What is the average throughput rate per hour, what is the average WIP, what is the average cycle time in hours, and what are the average cycle time in queue and WIP in queue. Okay?
Just repeat the procedure that we have seen together, And ask if you have questions or you have doubts on something. Okay. So let's see the solution. First point, the utilization, lambda over mu. So the utilization is 0.958.
Correct? Let's check together the numbers. Then point two, the probability that there are no jobs in the workstation. So p zero one minus u, so 0.042. Correct?
Okay. Then the number of jobs lost so zero. This is the unlimited system, so no jobs lost. Then for the point, the throughput is equal to lambda. Then the whip, we use the formula, utilization divided one minus utilization, 22.81.
Correct? Mhmm. Then six point cycle time, whip divided by throughput by using the little slow, seven point nine three four hours cycle time. Yes. Then seven cycle time in queue.
Cycle time minus e of t s. Seven point six hours, and the WIP in queue, Throughput multiplies cycle time in queue. 21.85 jobs. Correct? So here, we can see that in this case, we have the arrival rate that is very similar to the processing rate.
So we expect an utilization near to one. It means that the the machine is almost full, almost processing. And as if the utilization is higher near to one, we expect a large number of items in the queue and also an higher waiting time. And in fact, if you see the cycle time in total is seven point nine, but seven point six hour are spent waiting in the queue. So this is why this is because the utilization is near to one.
If we are able to decrease the utilization maybe by increasing the processing rate sorry, increasing the arrival rate, then the performance measure will improve. So the cycle time can be reduced. So the proportion between cycle time in queue and cycle time. Let's summarize all the performance measures for the m m one system. Summary of performance measure.
Now the formula that you have in the slides, in the last slide of today, these formulas are a little bit different from the ones that we have demonstrated until now. Okay? So let's just do this final step to write the formulas in another way. That is the standard way. So it is more easy than to understand the most complex ones.
M m one. Exactly. So now okay. Remember that these formulas are only valid for the m m one system. Then we will see the more complex formula that is valid for all the systems.
Okay? But this one is more specific and is valid only for the m m one system. Okay? Not for the general distribution. So the summary of performance measure, the utilization the utilization is lambda divided by mu, and the throughput is always equal to lambda.
Okay? Then we have seen that the WIP is utilization divided by one minus u, And the cycle time is whip divided by lambda. So u divided one minus u divided by lambda. That is one divided by minus lambda. K.
Now let's rewrite the cycle time. The cycle time is one divided minus lambda. This quantity, if we divide the numerator and the denominator by mu, we obtain one divided by mu, divided mu minus lambda, divided by mu. That can also be rewritten, so the numerator is equal. The denominator is written as one minus lambda over mu.
Then let's remember that one over mu is E, and that lambda over mu is the utilization. So this quantity is e of t s divided by one minus u. Also written as one divided one minus u multiplied by e of t s. Okay. This is another way of writing the cycle time, starting from the quantity that we computed before that comes from this formula of the WIP.
This equation so remember this equation because when we see the other systems, start from this basic equation to compute the cycle time, also for other systems, so not only MM1. Okay? So this is the core of the formula that is valid only for system MM1. Then from the next week we see how this formula changes for the other systems. So when we have parallel machines and where the distribution are not exponential.
So this is the core of the formula, and then we see how to integrate the other parts for the cycle time. And let's also see the cycle time in queue. K? So cycle time in queue is a cycle time minus e of t s. And the the cycle time, so let's substitute the the value of the previous formula.
So e of t s divided one minus u minus e of t s. So let's do the common denominator, one minus u, and write e minus e plus u multiplied e. And here we derive u divided one minus u multiplied e. Again, this is a part of the formula that will be extended for the other systems, general systems. Let's also compute the weeping queue as a throughput multiplied the cycle time in queue.
No. No. No. No. No.
These are used only for m m one system. We see how this formula changes when we change the system, but we will see so it's more easy to recognize this portion of the formula in the complex formula. So weeping q is throughput multiplied cycle time in q. So lambda multiplied utilization divided one minus utilization multiplied E of TS. Then now let's express E of TS in function of lambda and mu.
So the utilization is lambda divided by mu. So lambda multiplied E of ts. And from here we have that E is utilization divided by lambda. So let's use this formula here, and we have lambda multiplied by u multiplied by u divided lambda divided by one minus u. So we simplify lambda, and the formula remains u squared divided by one minus u.
Okay. And these are the formulas that you have listed in the final slide, in the slide with the summary of performance measures. K? Since they are a little bit different from the ones we derived, I prefer to to do with you all the steps. And this size solution, this one.

See how these formulas change when analyzing a system of type MMC. So if you remember the notation, MMC means that we have again the times exponentially distributed, both the inter arrival times and the processing times. But the third parameter is the number of parallel machines. So here we are extending the system, allowing to have more than one machine inside the workstation. Now let's firstly considering that the machine are identical with the same processing time.
And then we see also how to address the problem of having different processing times so for the non identical machines. So here, let's just compute, represent together the state diagram so we can see if everything is fine. And then we have a look at the formula without demonstrating it in this case. So let me take the other board. M m c system.
So here we have a system with, as usual, lambda is the arrival rate, average arrival rate of item. And then here in the workstation, we have the queue and c machines in parallel. And each machine has a processing rate of Okay? So if each machine has a processing rate or a capacity of mu, which is the capacity or the total processing rate of the workstation. Well, since these machines are in parallel, the total processing rate of the workstation is three mu.
This is the capacity of the workstation. Now let's represent the state diagram. This is an unlimited system. Okay? So we cannot draw the the complete state diagram, but let's just show the first nodes.
So at the beginning, the system is empty, so we are in state zero. Then from state zero, a new item can arrive, and thus we move in state one, which is the rate at which we move from state zero to one. It is the arrival rate of items, so lambda. So when we have only one item in the system, it means that the item is inside one of the machines. So it can happen that a new item arrives from state one, and as we move in state two, again, at rate lambda, or we come back in state zero if the processing of the item is finished, which is the rate at which we move from one to zero.
Since we have only one machine occupied, the rate is the processing rate of the machine. So move. Then from state two, we can if a new item arrives, we move in state three with the rate lambda. Or if one of the two item finishes the processing, we move that back to state one. But here, being in state two means that two machines are occupied and are processing.
So which is the total processing rate at which we move to state one? In this case is two the two machines processing. Then from state three or a new item arrives and we move to state four, or one of the three machines finishes the processing and as we move back to stage two. And in this case, the rate of this movement is three move. Then in state four means that we have the three machines full and one item waiting in the queue.
So if the new item arise, we move to the next state. And here the pattern go on goes on. And if one of the machine finishes the processing, we move back to state three. And here the rate is always three move because this is the maximum capacity of the workstation. Okay?
So this is the pattern. Again, three move for the backward propagation and always lambda for the forward propagation. This is the state diagram for the MMC system. Well, here we start from one one multiply by mu, then two multiply by mu until c multiply by more, and then always the c multiply by more. Okay.
Then for these kinds of system, there is formula. We don't derive it, but we we take it as it is. That specifies that cycle time in q for the system, so for system MMC, is equal to the utilization at a power of root square of two c plus two, then minus two outside the root square divided by c. And this term multiplies the cycle time in q of system m m one. So we can compute the cycle time in q for an MMC system starting from the cycle timing q of a system m m one and multiply it by this coefficient.
So let's remember which is the cycle timing q of the of system m m one. It it is written as utilization divided one minus utilization multiplied e of t s. Okay. So if we go on with the formula, here we have the utilization that multiplies utilization at this power. So the effect is that we sum one at the explanation.
So we have utilization at root square of two c plus two minus one outside the root square divided by c that multiplies one minus u. And this coefficient is multiplied by EOTS. Okay? So we have seen how the formula of the cycle time in queue changes when we have multiple machines in parallel. If we have only one machine, we can use this simplified formula.
If we have c parallel machines, we use this formula here. So we have seen so we have developed together the state diagram in this slide, and and then we have this formula to compute the cycle time in queue. This formula is valid for the case where the machines are identical, so have the same processing rate. Now let's address the problem in which we are the machines with non identical processing rate. So let's consider as an example.
Here we have a workstation with the two machines with non identical service rate. So there is one machine that is faster and the other that is slower because their service rate are different. If a job arrives to the system and finds that only one machine is busy, then the job is assigned to the idle machine regardless of the speed of the machine. So at the beginning, if the system is empty, so both the machines are empty, and when the first job arrives, then it is assigned to the fastest machine. Instead, when an item arrives and only one machine is available, then it is assigned to the available machine.
Okay? So this is the rule. Then once a job is assigned to a machine for processing, it remains on that machine until its processing is complete. Okay? So the the item cannot change the machine after a period of processing.
Once it starts the processing on a machine, it also finishes it on the same machine. Then the inter arrival times are exponentially distributed with the mean arrival rate of lambda. And the mean service rates of mu and gamma for the two distinct machines are gamma is lower than mu. So it means that mu is the faster machine. Let's consider that we have a limit of four jobs in our system at each time.
So here, the idea is to address this problem with the nonidentical service rate. Let's start again from the limited system so that we can write so represent the state diagram and use the system of equations to find the probabilities. Okay. So let's represent the state diagram of this system together. So the non identical service rate.
This is a system where we have lambda as, the interarrival rate. And then we have, again, the queue and two machines that, have a different processing rate. One is mu and the other is gamma. And is the faster machine. F.
And the gamma is the slower machine s. So mu is higher than gamma. Okay. So first thing, which is in this case the total capacity of this workstation. If we have two machines, one with processing rate mu and the other with processing rate gamma, the total processing rate is the sum of mu plus gamma.
This is the total capacity of the machine. Okay. Now let's derive the state diagram for a maximum WIP of four. So max WIP equal to four. So a maximum of four items in the system.
Okay. So let's start with the empty state, so state zero. From state zero, if a new item arrives, we go we say that if both the machines are available, the job is assigned to the faster machine. So here, it's not enough to indicate the state one because the state one can mean that all the machine faster is occupied or machine slower. So we needed to differentiate these two states.
So state one instead is divided into two state, one f and one s. So state one f mean mean that the faster machine is occupied. So from state zero, we move to state one f a trade lambda. Because if both the machines are available, the item is assigned to the faster machine. Okay.
Then from state one f, what can happen? Well, if a new item arrives, then also the second machine is occupied. And so we move to state two. State two means that both the machines are occupied. So two f s.
But we only have one state two, so again, we can call it only two. So we move from one f to two with the rate lambda. Or from state one f is the machine if the machine ends the processing, then we move back in state zero. So from node one f, we move to state zero with the rate move that is the processing rate of the faster machine here. Now let's analyze the state two.
If a new item arrives in state two, then we move to state three with two items in the machines and one in the queue, always with rate lambda. Then when we are in state two, since both the machines are occupied, things can happen. Or that the faster the faster machine finishes, and if the faster machine finishes, we move to state one s because the faster ends the processing and it's empty, and we have only one item in state in the machine slower. Okay. So from state two, if the faster machine ends the processing, we move in state one s.
So here, let's make up here the new state with a rate of So the processing rate of the faster machine. Because if the faster machine finishes the processing, then it is empty. And we have only one item in the slower machine. So we move in state one s. Or from state two, maybe the slower machine finishes before.
Because in general, we don't know which of the machines fin starts before. So when we are generally in state two, it can also happen that the slower machine finishes before, and thus we move in state one f. We saw which is the rate of this movement is the processing rate of this lower machine. So gamma. Okay.
So now we finish the the movement of state two. Now let's analyze state one s. We are in state one s, it means that only the slowest machine is occupied. What can happen? Well, if a new item arrives, then we move back to state two.
So if we have in state one s, a new item arrives, then we move to state two with rate lambda. Or the machine finishes the processing and does we come back to state zero with rate gamma. That is the processing rate of this lower machine. Okay? So we'll finish the analysis of state one s.
So let's come back to state three. In state three, if a new item arrives, we move to state four with rate lambda. And if instead a new an item is processed, then we move to State 2. Here, from State 3, we have both the machines occupied. So the total processing rate is mu plus gamma.
So here, the rate of the movement from three to two is mu plus gamma. And then let's finish State 4. In State 4, since the maximum whip is four, a new item cannot arrive, cannot enter the system. So the only possible thing is that one item is processed. So the only movement is from four to three, again, with the rate mu plus gamma.
Okay? So we developed the state diagram for this MMC system, limited system with non identical service rate. Now tell me, everything is clear. If you want, I can repeat something if you miss some steps or if there is something that doesn't convince you. Okay.
So let's suggest yes. Can you please repeat the one f? Yes. One f is the state. So let's represent in this way.
We have the q and we have and we have the two machines, the faster and the slower. So at the beginning, we are in state zero. This is state zero without items. Then from state zero, we move in state one f at rate lambda because when the first item arrives, it is placed here. And so we move this is state one f.
So one item in the system and the item is in machine f. Then if the machine finishes, so we come back to state zero. We we add this arc from one f to zero, And here, the rate is the processing rate of the faster machine. So then if the second item arrives, it is placed here in the second in this lower machine. And this state is called the state two.
So two items in the system and the both the machines occupied. So we are in state two. Then from this state so let's not don't consider that here we are at the beginning of the system because at the beginning, the fastest finishes before the slowest. So at the beginning from state two, we always move to state one s. But since the times are exponentially distributed, maybe instead the faster machine finishes after the slower machine or because the faster machine is was occupied later.
Okay? So in general, when we are in state two, both things can happen. Or the faster machine finishes before. So if from state two, we have that the faster machine finishes, so the queue is always empty, And then the faster finishes. And the faster finishes at rate move.
So we move back. So we move in state one s. This is state one s because only the slower machine is occupied. So from state two with the rate move, we move to state one s. Or from state two, another thing can happen.
That the slowest finishes before and thus there is a movement from state two to state one f. And this movement here is represented by this arc and, of course, at rate gamma. That is the processing rate of this lower machine. Okay? So one f is the state in which we are one item in the system and the desired stem is in processing in the faster machine.
Is it more clear now? So if you have other questions, just write to them. Now the next step is as we did last time for the m m one, limited system m m one, we need to derive the equations to find the probabilities of being in each state and then use the probabilities to compute the WIP and the cycle time. So here, we need to cut the graph, this our state diagram in different points in order to derive five equations since we have six unknown variables. So we need five equations from the graph and another and the norming equation.
Okay. So let's do the first cut of the graph here. So we divide node zero and all the other nodes. And let's write the corresponding equation. So the first equation is p zero multiplied lambda.
So here so we write from one side of the equation, the exiting flow, such as this one. So p zero multiply lambda. And on the other side, the entering flows. We have this flow here and this other here. And these flows needs to balance in order to reach the steady state.
So we have p zero lambda equal to p one f multiplied mu plus p one s multiplied gamma. Then let's do another cut. For instance, by dividing a node one f and zero from the other nodes. So this is the first cut. This is the second cut.
So here, let's write again the exiting flow. We have only one, this flow here, exit from the left part of the graph. So for the second equation, we have p one f multiplied lambda. That is equal to the entering flows. The entering flows are this one and this one.
So p two multiplied gamma plus p one s multiplied gamma. Then let's add another cut here. The third cut and the right of the third equation. Here we have four arcs, two entering and two exiting. So p one f multiplied lambda plus p one s multiply the lambda equal to p two multiplied gamma plus p two multiplied mu.
And then the last two cuts, here the fourth, and the other here to obtain also the probability p three and p four. So let's write also the fourth equation. It's easy. So we have p two multiplied lambda equal two p three multiplied mu plus gamma. Then the fifth that is similar, so p three lambda equal to p four multiplied mu plus gamma.
And then let's add the the norming equation. So the sixth equation is the sum of all the probabilities is equal to one. So p zero plus p one f plus p one s plus p two plus p three plus p four equal to one. Okay. So now by solving the system of equations, we are able to find the probabilities of being in each state.
Now let's do a numerical example in order to obtain these numbers. So go on finding the probabilities, but with a numerical example. Okay. So let's read together the text of a practical case. We have facility for helicopters that is open twenty four hours a day, seven days a week.
And the helicopters arrive to the facility at an average rate of three per day according to a Poisson process. Poisson process means that the inter arrival times are exponentially distributed. One of the areas within the facility is for degreasing one of the major components. And there is only room in the facility for, four jobs at any time. And there are two machines that, do the degreasing.
The newer of the two degreasing machines take an average of eight hours to complete the degreasing. And the older machine takes twelve hours for the operation. Because of the larger variability in helicopter conditions, all times are exponentially distributed. Okay. So this is an example where we have these two machines, the the greasing machines.
One is the newer and the other is older, and thus the new one is the faster that takes only eight hours to complete the degreasing. Instead, the older ones takes twelve hours. So we use these values. We need the the rates instead of the times. So we have okay.
Lambda, we have the rate, so three per day, so it's three. Then mu is the rate of the faster machine. So in this case, it's three per day. Twenty four hours in a day divided by eight hours, so three helicopter per day. And the gamma is only two per days because the processing times of the second machine is twelve hours.
Okay? So now let's use this numerical example to go on solving the equations. Okay? These diagrams these diagram represent this example. And in the equations, we substitute the numbers.
And the numbers are lambda equal to three job per day, and mu is three jobs per day, twenty four hours divided eight hours, and gamma is two jobs per day. So now let's rewrite the equations by using these numbers instead of lambda, mu, and gamma, and then solve the system and find the probabilities. So let's do it together. The first equation we have three p zero equal to three p one f plus two p one s. Then the second equation is three p one f equal to two p two plus two p one s.
Then the third equation is three p one f plus three p one s equal to two p two plus three p two. Then the fourth is three p two p three, sorry, equal to three p two equal to five p three. And the fifth is three p three equal to five p four. And finally, we have the norming equation. P zero plus p one f plus p one s plus p two plus p three plus p four equal to one.
So this is the system of equation that we have to solve to find the probabilities. So these are mainly algebraic steps. So for instance, from the second equation, we obtain p one f equal to two p two plus two p one s divided by three. And from the third so let's use this result and substitute it in the third equation. So we have a three that multiplies two p two plus two p one s divided by three plus three p one s equal to five p two.
So the three simplifies. And from here by grouping p one s on one side and p two on the other side, we obtain that p one s is equal to three over five p two. So now we are expressing all the probabilities in function of p two. So we obtain p one s in a function of p two. And from this result, we can also here compute p one f by using instead of p one s three over five p two.
And by solving the computation, we obtain p one f equal to 16 over 15 p two. Then from the fourth equation, we obtain p three in function of p two. So p three is three over five p two. And for the fourth, use this result. So we write three multiplied three over five p two equal to five p four.
And from here we obtain that p four is equal to nine divided 25 p two. And from the first one, so finally, we, insert into the first equation the value of p one f and p one s. So from here, we obtain that three p zero is three multiplied 16 over 15 p two plus two multiplied three over five p two. And as p zero is 22 over 15 p two. Okay.
So let's just rewrite all these results. So from the first equation, we have p zero equal to 22 divided 15 t two. Then from the second, we have p one f equal to 16 over 15 p two. From the third p one s equal to three over five p two, then p three, v over five p two, and p four nine over 25 p two. And so the last equation becomes so we sum all the coefficient.
So 22 divided 15 plus 16 over 15 plus three over five plus one, that is p two, plus three over five plus nine over 25 p two equal to one. So from the last equation, we derive p two equal to one divided all these numbers. And p two is so one divided by 5.093. That is 0.196. And from p two, we compute also all these others.
So we have p zero is 22 over 15 multiplied 0.196. The result is 0.288. Then p one f, 16 over fifteen, zero point one nine six, 0.209, p one s, three over five, zero point one one eight, Then p three, three over five, so it's the same. Three is the same as p one s, 0.118. And p four is nine over 25 multiplied zero one nine six, that is 0.071.
So we computed all the probabilities, and then let's apply the formula to compute the WIP. Can I change the page? The is the same formulas. So the sum for n from zero to four, in this case, of n multiplied p n. So zero multiplied p zero, the first term doesn't matter.
Then one multiplied p one f, p one f, plus one multiplied p one s, plus two multiplied p two, plus three multiplied p three, plus four multiplied p four. So if you do all the computations, you obtain the whip of 1.356 jobs. Then let's compute also the waiting queue as the sum for k from zero to two in this case. Okay. So the weeping queue is the average number of items in the queue.
And in the queue, we can have zero, one, or two items because in the system, we have a maximum of four items. So the maximum number in the queue is two of k multiplied pK, where k is the number of items in the queue. And the p k is the probability of having k items in the queue. Probability of having k items in the queue. Let's write the numbers.
When I have one item in the queue, it means that I am in state. Our system is the queue and the two machines. Fast and slow. If I have one item in the queue here, it means that both the machines are occupied. Okay.
So the probability of having one item in the queue is equal to the probability of having three items in the system. So one multiplied p three plus two two items in the queue multiplied by the probability of having two items in the queue. So if I have two items in the queue, it means that I have four items in the system. So two multiplied p four. So p three is 0.118 plus two multiplied 0.071.
The sum is 0.26 jobs. This is the average number of items in the system. Then let's compute also the other performances. So in order to compute the cycle time, we need the throughput. Then if you remember, the throughput for the limited system is not equal to lambda, is equal to lambda effective.
So the throughput is equal to lambda effective, and the lambda effective is lambda that multiplies one minus the probability that the system is full. That in this case is p four. So the lambda effective is lower than the original lambda because of some items are discharged by the system. So in numbers, we have three that multiplies one minus 0.071. So 2.787 jobs per day.
So this is the throughput, the real throughput of the system. And then with the throughput, we are able to compute the cycle time. The cycle time is divided by throughput. So the is 1.356 divided by 2.787. And the result is zero point four eight six days.
Then if we want to compute also the cycle timing in queue, so the average waiting time, we use the same formula, but within the weeping queue instead of the whip. So cycle time in queue is equal to whip in queue divided by the throughput 0.26 divided by two point seven eight seven, 0.093. K. Now let's come back to the slides. So example, here the system of equations and the solution in numbers.
And here, the average number of jobs in the system. So the average WIP, average WIP in queue, cycle time, cycle time in queue, and the effective arrival rate. Then here, let's also perform another computation that is since here we have two parallel machines, we can compute, let's say, the the average processing time, again, by using the formula that the cycle time is the cycle timing q plus the processing time. So let's do also this computation together. Put the average processing time of the workstation.
Average processing time of workstation. It is e of t s. And it is computed as cycle time minus cycle time in q. So 0.486 minus 0.093. That is zero point three nine three days.
And, another thing to compute is the average number of busy servers. So let's also compute the average number of busy server servers. So the average number is computed by using the same formula of the whip and the whipping queue. So let's call this average number e of b s. That is the sum for let's again change the index for j of j from zero to two because we have two machines, so two servers of j multiplied p j, where j is the number of busy servers of busy machines.
The server of the machine servers. And the p j is the probability of having k busy servers. Probability of having j busy servers. So this sum can be expanded into. So one one busy server multiplied by the probability of having one machine occupied, and this probability is p one f plus p one s.
Plus two, So two number two two machines busy multiplied by the probability of having two machines busy. And this probability is p two plus p three plus p four. And so if we, insert the numbers of the probabilities, we obtain an average number of busy servers of 1.097. So it means that 1.1 machine is occupied on average. And this number can be used to compute the utilization of the workstation.
So the utilization of the workstation can be computed as the expected number of busy server, so EOBS divided by two, because we have two machines. And this quantity is 0.5485. So it means that on average, the machines are are reused for the 5055% of time. So the the the faster is most used, the slower less used, but the average utilization is 0.55. K.
So we are here. We computed the average. Okay. Here, we also have the quantity in hours of the processing time. And then this last thing about the expected number of busy servers and the the utilization of the machine.
Mhmm. Okay. Any question? No? Okay.
So we can do the break. Ten minutes of break now, and then we go on for the second part. Okay? So see you in ten minutes. Okay.
So let's start again. Also, in this case, I have prepared the simulation model of this system. So let me share it here. So you see, in this case, we have the source of items with the inter arrival time as inverse of the the arrival rate, so one over three. And then the two so the q with the limit of two items as maximum content of the queue.
And then the two machines. So the faster machine with an exponential time with the average time of eight over 24, And of the slower machine, again, the exponential with the average of 12 over 24. And here, if we reset and run the simulation, we can compare the results with the the ones that we computed. So for instance, here we computed an average utilization of 0.554. And here you see we have one machine 59 and the other 50.
So the average is around 54 something. And then also the cycle time, that is the sum of this quantity. So the q and the average between faster and lower. The WIP, that is the sum of all the WIPs. That the total is 1.36, or less.
And here, you also see the okay. In the throughput, you don't have the throughput, but you only have the output. So the number of items that leave the system, because it's always increasing, this number. But with this number, you can compute the throughput because you have here also the total run time. So here you have the total unit of time for the length of the simulation.
So you can divide the output by this quantity to have the throughput. And another thing that you can see from the dashboard is the difference. Let me stop for a moment the simulation. So you see that the source, now that I stopped the simulation, the source generated a total of 2,000,604 five fifty eight thousand and so on of items. But in the sink, we only have No.
But, in the queue, we only have, less number of items because some of them find the system busy, and thus they are discharged. So not all the items go to the q one, but some of them go to the q two. And if you compute the probability, so the percentage, you obtain the probability that the system is full, so the p four, for instance. Okay? So here, I I showed you some models in FlexSim because sometimes I I prefer to present you some data in this form.
So instead of writing all the things in the text, I do a screenshot of the the simulation program. And from the screenshot, you can you can read some parameters that then are useful to solve an exercise. So now let's come back to the slides, and let's solve this exercise that present the the data in the form of a screenshot of the simulation model. So let's read together the text. By analyzing the report and simulation model with the two servers with the non identical service rate and the maximum weight of four items, find the following parameters.
Arrival rate, lambda, process processing rate of the faster machine, mu, and of the slower machine, gamma. Then find the probability that a job is rejected, and find the average utilization of the workstation. Okay? So now you have to answer to these questions only by looking at the data present in the dashboard. Okay?
So this is a dashboard very similar to the ones that I have already shown. It's very similar to the exercise that to the example that we did together. And the the things are reported in the dashboard. So in the dashboard, you can see the state diagram that is the percentage of, time spent in each state by each machine. So the faster machine is 36.48% in state processing, and the slower is in 25.8% of time in state processing, and the rest are idle.
And then in the tables, you have the cycle time, the WIP, and the output for each object in the diagram. Now I leave you a few minutes so you can solve the exercise by your own, and then we check together the solution. Okay? K. So let's see the solution.
Okay. So from the dashboard, we can see the cycle time of the two machines. So we know that rate is the inverse of the time. And thus we can compute we can use this information to compute the processing rate. So from the dashboard, we know that the cycle time of the faster machine is zero point twenty five days, and does more is one divided by 0.25, so four job per day.
The same, we read the cycle time of the slower machine that is zero point five days. And from here, we derive gamma one over 0.5, so two jobs per day. Then in order to compute lambda instead, we can do, we know, the, cumulative output of source. So we know that the cumulative output of the source is this number. So one million five two two and then nine five five.
This is the number of jobs generated and the the run time. We also know that the run time that is written at the top of the window is, seven six one six zero two days. So this is in jobs. This is in days. And as lambda is computed as the ratio between these two numbers, 1,522,000 and so on divided by seven hundred sixty one thousand six zero two.
And the result is two jobs per day. This is the total number of items generated by the source divided by the total length of the simulation. Then the probability that the job is rejected, Here we know the number of items that arrive at the sink. So the cumulative output of sync is 17,890. And so the percentage of lost item is the ratio between this number and the total number, the total items generated.
It is 1,522,955. And this number is 0.0117. So this is the percentage of lost item. The percentage is 1.17%. And then the last question is the utilization of the workstation.
Yeah. So we needed to compute the average utilization of the two machines. So we know the utilization of the faster is 36.48, and the utilization of the slower is 28.85. Thus, the utilization of the workstation is the average. So thirty thirty six point forty eight plus 28.85 divided by two.
And the result is 32.67%. These are percentage of utilization. Okay. So here in this kind of exercises, you need to be able to understand the meaning of the dashboard of the simulation model and use this data instead of having them directly written in the text. Okay?
So this is another example of exercise that you can find also in the exam.

And now let's see what happen if instead of having times that follow exponential distributions, We have times that follow a combination of exponentials. So this is an attempt to generalize the system, and let's approximate the times by combination of explanations. This is an intermediate step before considering the general distribution. So to this aim, we use the Erlang distribution.
So the Erlang k distribution is defined as the sum of k independent and identical distributed exponentials. And then let's have a look at this function. So let's say an Erlang distribution have a two, has a two parameters, k and the beta. And definition is that the Erlang is the sum of k independent exponential variables, each with a mean that is beta over k. So here in the slides, you also have some so in the picture, you have some example of Erlang distribution.
So the shape of the Erlang distribution depending on the number of k. So if k is equal to one, it's a single exponential. So the the shape is as an an exponential. And then if k is equal to two, it's like the the solid line. And if you increase the k, then you move towards the dotted line.
Here, you also have the the function, but we don't go into the details of the function. The only thing that we needed to remember are the expected value. So the mean value of the air lung is called beta. Its variance is computed as beta squared divided by k, and its square coefficient of variation is one over k. Okay?
So we have we define an Erlang that is the sum of k independent exponentials, and its square coefficient of variation is equal to one over k. Then let's, for instance, consider a system for which the notation is m e two one three. It means that the arrival times follows an exponential distribution, the first m. Instead, the processing time follows an Erlang two distribution. And we always have one machine, and this is a limited system with a maximum width of three.
Here, since this is a limited system, let's proceed as usual by drawing the state diagram. Then let's read the other parameters. So we have the interarrival times, exponential distributed with a mean arrival rate of lambda, and the processing time described by an Erlang distribution with a mean rate of boom. Okay. So here, the idea is to model so in the state diagram, since the is a sum of can be seen as a sum of, in this case, two exponential distribution, so let's consider two different nodes to represent the two phases of the air lung.
So when dealing with the air lung, in the state diagram, we have some nodes that are, let's say, duplicated because we separate each phase of the Erlang, one for each exponential distribution. Now so let's do together as usual the diagram. So we so now we are developing the Erlang case. And we consider a system with max width of three jobs. Then the arrival rate, lambda.
And the processing time is an Erlang two Airlungitude distribution with mean rate. K. And, for the Erlang, we consider, so to represent in our state diagram, not as a single node, but as two nodes that are executed in series. So we have two phases of the Erlang. For instance, at the beginning so let's consider as usual, not just to understand that.
At the beginning, the state is zero. Then at rate lambda, we move to the first state of the Erlang. So in this case, Erlang two, it means that it's the sum of two exponentials. So each Erlang is divided into two nodes. If we add Erlang three, then it means that this is the sum of three exponentials, and thus we have three phases of the Erlang.
So in this case, we have two phases. And as state one, instead, is called state one one and the state one two. And the the meaning of the state of each number inside the state is the first number represent the number of job in the system as usual. So the first number, the first one is number of jobs in the system. And the second one is the phase of the air lung.
This is the phase number of the air lung. So the the Erlang is seen as being composed by two phases in series that corresponds to the two exponentials so that the the the total Erlang is the sum of these two exponential distribution. So from state zero, we move with the rate lambda in state one one. Okay? Then this is the first phase of the Erlang.
So from state one one, we can move in state one two. So here there is the rate lambda. And from one one to one two, the rate of moving is two instead of only move. Because is the total rate. And it corresponds to a certain processing time.
But if we consider that the Ehrlang as the sum of two exponentials, it means that each phase is takes half of the time half of the time of the entire process. And thus, half of the time corresponds to the double rate. So from state one one, we move to state one two at rate two mu. And then from state one two, when the process is finished, we move back to state zero at rate again two moo. Okay.
So this is how we represent the Erlang distribution as a sum of two exponentials executed in series. And thus, each phase takes half of the time of the total time, and thus, the corresponding rate is two times the processing rate. Now let's expand this processing to represent the system with maximum width of three. So let me redo again the diagram. We start in state zero and at rate lambda, we move in state one one.
Then when we are in state one one, we can or move to state one, two, at rate two, move. Or if there is the item that is under processing and it arrives another item, we move to another state in which we have two items in the system, but we still are in the first phase of the Erlang of the processing. So from one one at rate lambda, I move in state two one. State two one means that I have one item in the queue and one in processing. And the item in processing is in the first phase of the air lung.
Then if we are in state one two, it means that we have one item in the system, and the item is processed by the second phase of the air lung. So in this case, which are the things that can happen? Or that the item finishes the processing, and thus we come back to state zero with rate chew more. Or even if we are in this state, the new item can arrive. And as we move in the state where we have two items in the system and the item in the machine is doing the second phase of the Erlang.
So we move in state two two. So two items in the system and second phase of the air lung. Then let's analyze first with the node two one. If we are in node two one or a new item can enter the system, and thus we move in state three one because we have three items in the system and we are still in the first phase of the airline. Or the new item goes on processing and does a moving state to to reiterate.
This is a lambda. Then from node choo choo or a new item arrive, and as we move to state three two with rate lambda, or the item finishes the processing. So if we are in state choo choo, it means that we have one item in the queue. And here, let's represent the choo state of the air lung. So two two means that the item is here in the second phase.
And so this is a state two two. If this item exit the system, we move in the state where the item in the queue start the processing, so it's here, and the other exit. So this state here is state one one. So we have one item in the system and the first phase of the Erlanger. So from state two two, we move back to state 11, always with rate two moo.
Then since the maximum whip is three, when we are in state 31 or three two, we don't have other arcs going to new states. But the only thing that can happen is that the item goes on the processing. So from three two one so from three one to three two with rate two more. And from 3 two, the same situation as 2 two. So here we have in 32, we have three item in the system.
So two in the queue and one here in the second phase. So three item in the system and the second phase. This is state three two. If the new if the item finishes the processing, this exit the system and one in the queue goes to the first phase. So after state three two, we have a state where we have two items in the system, first phase.
So this is date two one. So from three two, we move back to two one with the problem with the rate to So here, in case of Erlang, since the Erlang can be seen as a sum of exponential, we can model each the Erlang as phases in series. And so we separate each state into multiple nodes, each representing a phase of the air lung. And then we model the movement from one phase to another. Remembering that the rate of movement is increases because they takes lower time in processing the item.
Now once we have the graph, then we can proceed as usual, so deriving the equation. Here, I show you now another way of cutting the graph. Instead of doing the cuts as we did before, so trying to separate the nodes in order to obtain all the probabilities in the equation. So instead of cutting the the graph in an arbitrary way, there is another procedure that is called the node isolation. That means cutting each node from all the rest of the graph.
Okay? In this way, we are sure not forgetting any nodes. And we derive so in this case, we have the possibility of cutting each node. So we have a total of seven nodes and seven probabilities. Okay?
But one equation is the norming equation. Okay? So we just cut six nodes and add as the seventh equation, the norming equation. Okay? So let's write the equations.
So let me just erase the here the the examples, so I can use the same page also to write the equations here. So let's now cut the graph by isolating each node. So let's start with node zero. So let's let's isolate this node from the rest of the graph and write the corresponding equation. Here, the equation is lambda multiplied p zero equal to two mu multiplied p one, two.
Then let's proceed by isolating the other nodes. So let's isolate node one one. We always consider the exiting arcs on one side and the entering arcs on the other side. So here we have lambda multiplied p one one plus two mu p one one equal to lambda p zero plus two mu p two two. Then the third node is one.
Here we have lambda p one two. So here we have two exiting nodes, this one and this one. So lambda p one two plus two mu p one two equal to the entering arc. It is this one. So two mu p one one.
Then the next node, this one. Here we have lambda p two one plus two mu. P two one. Here is p one two. Sorry.
Not two one. The exiting arcs are the same probability. Equal to lambda p one one plus two mu p three two. Then let's choose the other two nodes. So one at our choice, we don't consider one node at our choice, so I decided not to consider two two.
So I go on with the three one, and the equation is two mu p three one equal to lambda p two one. And the last one. Now the three two. Two more p three two equal to two more p three one plus lambda p two two. And finally, the norming equation.
So p zero plus p one one plus p one two plus p two one plus p two two plus p three one plus p three two equal to one. So also in this case, are able to derive the system of equation to solve in order to have the probabilities. Then once you have the probabilities, you use them in order to compute the WIP, the throughput, the cycle time. The WIP in queue and the cycle time in queue. So let's write also the equations for the performance measures.
The whip is the sum for n from zero to three. Of n multiplied. Here we have for each state except zero. We have so let's just start with the one instead of zero. So in this case, since it is an error language two, we have two probabilities.
So n multiplied p n one plus p n two. So we would once we find the p one one and p one two, we multiply both quantity by one. Then we sum two, multiply the p two one and p two two and so on. Then once we know the WIP, we can we we compute also the throughput in order to compute the cycle time. So the throughput is lambda effective.
So lambda that multiplies one minus the probability that the system is full. And here, the probability that the system is full is when we have three items in the system, and we have three items in state three one and the state three two. So we sum these probabilities, p three one and p three two. And this is the formula to compute the throughput. Then we can compute the cycle time as divided by throughput.
And then as usual also the weeping queue, that by using the same formula, in this case, the weeping queue is one multiplied p two one plus p two two. So this is multiplied by one. So one item in the queue corresponds to the probability of having two items in the system, in the first and in the second phase, two. So the probability of having two items in the system corresponds to p three one plus p three two. And then the cycle time in queue as we put in queue divided by throughput.
Okay. So in these kinds of exercises, the important thing is to compute to to be able to draw correctly the diagram, the state diagram. Okay? So this one. You see that we are seeing several examples for the limited system in which we are able to draw the diagram.
Sorry. Sorry. We have a problem here with my daughter. So so once you are able to define the the graph, then you follow the same procedure. Okay?
So you derive the equations, and then you solve the system, and you obtain the probabilities. And then once you have the probabilities, then you can use always the same formulas to compute the WIP, the throughput, the cycle time, WIP in q and cycle time in q. Okay. So let's come back to the slides. And so here you have the diagram as we did together with the two phases for representing the air lung two.
Then you have the partitioning of the graph. Here you have above the the partition with the with the first procedure, let's say. So you divide for one so different portion of the graph. So here you divide the zero and you write the first equation. Then you divide the state zero and one two from the rest of the graph, and you write the second equation.
Then this is the third graph, the third cut, then the fourth, the fifth, and the sixth, and then the norming equation. Or as I told you, this is a better way of cutting the graph to be sure not to forget some probabilities. And this is a method that you could have apply also for the other graph. So now that we know this method, we can apply it also. So for each each diagram, okay, this is more more easy, more simple.
And so here you have the equations that we did together. And then the summary of the the formulas that, again, are valid are always valid. They just needed to be applied on the different states and the probabilities that you have. Now after that, there is an exercise. So here, I just read the text with you, and then I leave you the time.
But we don't solve it today because I want you to think about how to represent, especially the state diagram, Because I know that it takes time understanding how to create this diagram, so you need to spend some time by your own thinking about it. Okay? But let's just read together the text, then you have time to solve it today, and then we check we see the solution tomorrow together. Here we have a maximum number of jobs allowed in the system equal to two. So only two jobs in the system.
So one in the queue and one in the machine. The interarrival times are exponentially distributed with a mean arrival rate of lambda equal to three jobs per hour. And the processing time are described by an Erlang three with a mean rate of mu equal to six jobs per hour. Okay? So here, let's try to generalize the state diagram that we have seen for the Erlang two for the Erlang three.
Okay? So let's think about how the diagram changes. And then draw the state diagram and derive the balance equations by using the node isolation technique that we have seen together. And then stop it. Because when the system becomes so complex, I don't want you to solve it manually.
So next time, we will see another way of solving this system by using Excel and so in the matrix form. And then once we have the probabilities, we compute the performance of the system. Okay? So now I leave you this text. You have time, solve it.
Try to solve it, at least the first two questions. And then if you want also the formulas to compute the performances. And then tomorrow, we go on and we we see the solution. Okay? So let's start as usual with the empty state, state zero.
Let's also report here the input data. So exercise. We have a max of two jobs. Then the arrival rate, lambda, is three jobs per hour. And we have an airline, three with processing rate move of six jobs per hour.
So having an Erlang three means that the Erlang is represented as three phases. So each state is divided into three nodes. So phase one, phase two, and phase three, and which is the rate of movement from one phase to the other. Yesterday, we had only two phases, so the rate was two. Instead here, we have three phases, and thus the rate is three.
Okay? Because the three phases are in series, and thus the processing time is one third of the original processing time of the whole whole machine. Okay. So let's now draw the state diagram. So we start from node zero.
The system is empty. And then when the new item arrives, we move in state one first phase. So one item in the system and first phase. So we move in state one one. Remember that here for the air lung, in each state except the the zero state, we have two numbers.
The first one is the number of items in the system, and the second is the phase of the air lung. Then when the rate here is lambda, the arrival rate, Then when the first phase finishes, we move in state one two. So always one item and the second phase. One, two, with a rate of three as we said. Then after also the second phase is completed, we move to phase three.
And so the state is one three. Again, the rate is three move. And then when also the third phase is finished and so we move back to state zero again with rate three. Okay. Now, in each of these state, it can also happen that a new item arrives.
Okay? So, for each, of this state, we add an arc to the next state, where the phase remains the same, but we increase the number of items in the system. So from state one one, if a new item arrives, we move to state two one. It means that now we have two items in the system, one in the machine and one in the queue, and the processing phase is always the first one. And the rate is lambda.
The same for state 12. So in state 12, the other thing that can happen is that a new item arrives, and thus we move to state 22 always with rate lambda. And the same for the third state. So if we are in state 13 and a new item arrives, we move to state 23 with the rate lambda. Now we have these new three states.
So let's add also the movement from state 21 to 22 and then two two three, representing the evolving of the phases of the air lung. So from chew one, we move to chew chew with rate three move. Then from two two, we move to two three, again with rate three move. And then what happen to state 23? So if we are in state 23, it means that we have two items in the system and the first one is in the third phase.
So when the third phase finishes, so the item exit the system. So we decrease the number of items in the system. So the first number is one. And we restart from the first phase. So from state two three, we go back to state one one.
So one item in the system and the first phase. So from two three, we move to state one one with rate three more. And then we stop because the maximum WIP is two jobs. Okay? So we don't insert other states.
Now any question? Have you tried doing this diagram by your own? Do you have a question about the nodes, the arcs, the transition from one state to another, the labels of the arcs or the value of the rates? Brighter if you have any doubts. Okay.
Now let's okay. So the question, why we go back to one one instead of one two from two three? Okay. Someone wants to ask to the question. So let's represent the state two three means that we have the queue at the beginning and then the three states of the Erlang.
So state two three means that we have two items in the system. So one in the queue and the other in the third phase. This is phase one, phase two, phase three. So this is the state, the representation of State 23. Okay?
Is it clear? What is the meaning of the state? Two three. Two items in the system and the third phase of the Erlang. So remember the meaning of the two numbers inside each state.
The first number is the number of items in the system, And the second number is the phase number of the air lung. So this is the visual representation of state two three. Then when this item exit the system, we have that the remaining one, the one in the queue, start the first phase. So from state two three, we move to state So the item now is here, is in the first phase. Okay?
So the corresponding state is one item in the system, first phase. So the state is one one, not one two because one two means that we are we are already in the second phase. Okay? So to reach State 12, we needed to pass through State 11. We cannot access State 12 before passing State 11.
Okay. Is it more clear now? K. Other things? Okay.
So now let's go on and proceed with the definition of the balancing equations by using the isolation technique. So let's start writing the first equation by isolating node zero. And the first equation is lambda multiplied p zero, the exiting flow, is equal to the entering flow. That is three multiplied by p one three. Then let's analyze the second node one one, for instance.
As I said, you can choose all the nodes except one, and you can decide which one to exclude. So here, let's write, the exiting flow that are lambda multiplied p one one plus three mu multiplied p one one equal to the entering flows. So one is from zero, so lambda multiplied p zero. And the other is from state two three, so plus three mu p two three. Then, let's just keep node one two and analyze one three.
Here we have three mu p one three plus lambda p one three equal to three mu p one two. Then the next node, two one. Here we have three mu p two one equal to lambda p one one. Then the next node, two two three mu, p two two equal to lambda p one two plus three mu p two one. And the last node, two three.
So three mu p two three equal to lambda p one three plus three mu p two two. Now we have six equations, and we add the norming equation. So the sum that all the probability is one. So p zero plus p one one plus p one two plus p one three plus p two one plus p two two plus p two three equal to one. And this is our system of equation.
Everything fine until here? Okay. So at this point, we are ready to solve the system because we know lambda that is three and the mu, that is six. And thus, we inserted the numbers and we solved the system. Last time, we solved the system by substitution.
Okay? That is the usual way to solve this kind of system. Now let's just see for a moment another way for solving the systems that is using the matrix form. So I can show you also as a solve of the system with Excel. And as so you have also a tool more more easy and more rapid, more fast to solve these systems.
So to solve this system, to to use the matrix form to solve the system of equation, let's write the system in the form a of x multiplied by x equal to b, where I a is the matrix of the coefficient of our unknown variables. So the coefficients of p zero, p one one, and so on. And the b x are the unknown variables, so p in our case. And the b is the vector of terms without the coefficient, without the the variables. So in order to solve so we can rewrite our system in forms of matrix in this matrix form.
And then to solve this system, we invert the relationship, and, we can write that x is equal to the inverse of a, a minus one multiplied by the vector b. Okay. So let's define the matrix a. It is a matrix where we have, in the columns, all the unknown variables. So we have p zero, p one one, p one two, p one three, p two one, p two two, p two three.
And then in the rows, we have all the we have the different equations. And in the cell of this matrix, we have the coefficient of each variable. So here in the rows, we have the equations. So we have one, two, three, four, five, six, seven equation. And here, let's report the numbers.
So the coefficient that multiply the probabilities. So in the first equation, p zero is multiplied by lambda. So here we have lambda that is three. And then p one one and one two are not in the in the equation. So here we have zeros.
Then p one three is on the on the right part. Let's move it on the left part in order to have all the probabilities on the left and all the other terms on the right part. So p one three is multiplied by minus three multiplied by mu. So three multiplied by six, so that is 18. So the coefficient of p one three is minus 18.
And then zero for the other probabilities. Then let's write the coefficient for the second equation. So in the second equation, we have lambda p zero on the right part. So we move on the left, and thus the value is minus three. Then p one one p p one one is lambda plus three mu.
So lambda plus 18, it is 21. Then p one two is zero, also one three, also two one, and two two. And the coefficient of p two three is minus 18, and so on. Okay. So you build this matrix.
So for the third equation, we have zero zero minus eighteen, twenty one, zero, zero, zero. Then for the fourth equation, we have zero, minus three, zero zero eighteen, zero zero. Then for the next equation, we have zero zero minus three, zero minus eighteen, eighteen zero. Then for the sixth, we have zero zero zero minus three zero minus eighteen and eighteen. And for the last one, we have all ones.
Okay. So this is our matrix a. Then let's write also the vector b. So b is the vector with all the terms that we left at the right part of the equation. So b is always zero, except the last one that is one.
Okay? So at this point, we have written the matrix and the vector b. Now we needed to find the inverse of the matrix and then multiply the inverse of the matrix with the vector b. And this is the solution of our system. To do this computation, let's use Excel.
Here. Okay. So this is the matrix a with the numbers that we have written together, and this is the column b. Then here, we needed to select a row sorry, a column of the same length of b. So these are the number of our unknown variables that we wanted to find.
And here, we insert the formula. So equal to the product of the matric matrix that let me say let me check here. In Italian is matro.producto. In English, it's m for the multiplication, matrix multiplication. So find something such as m.
So it's the product of two matrices. And then here, we insert the first matrix that is matrix a. No. Sorry. Before inserting the matrix, needed to invert it.
So let's call the function to invert the matrix. That is matro dot inversion in Italian or minver m inverse in English. Okay? So then here we select a. So we are doing the inverse of this matrix.
Then the second parameter is the b vector. So here we select the b vector. Then we close the parenthesis. And then instead of just pushing the enter tab, we select control shift and enter. So all these three tabs.
So control shift, And so this is the result of the product. So here we obtain these are these are the values of the probabilities. So this is p zero. This is p one one in the same order as we started in the table. One two, p one three, p two one, p two two, p two three.
Okay? So in order to check if the computations are fine, if you use the substitution or if you want an alternative method, Perhaps at the in the practice, then you will see also other methods to to solve the the system. But, okay, I don't care. If you know if you know this method, it's fine for you. It's more fast, and you can solve more easily the exercises.
Otherwise, just use the substitution. In any case, I won't give you these complex systems in the exam because it's not a point of this course to teach you solving the system of equations. Okay? So don't worry. Okay.
So now we have the probability values. So let's just copy them on our here, paper. So we obtain as a solution of this exercise that p zero is 0.557, then p one one is 0.127, p one two is 0.108, p one three is 0.093, p two one is 0.021, p two two is 0.039, and p two three is 0.055. Okay. Now we have the probabilities.
Now let's go on and compute the performance of the system. So weep, weeping weeping queue, throughput to cycle time, and cycle timing queue. Let's write the formulas. So the weep is the sum of n multiplied p n. So in this case, we have one item multiplied by the probability of having one item, And we have one item in three states of our system that are p one one plus p one two plus p one three plus two multiplied the probability of having two items in the system that is the sum of p two one, p two two, and p two three.
And the result of this sum is 0.558. This is the average number of jobs in the system. Then let's compute also the weeping queue with the same formula. The sum of the number of items in the queue multiplied by the probability of having that number in the queue. Here we only have since the maximum whip is two, we can only have one item in the queue at maximum.
So we have one multiplied by the probability of having two one item in the queue that corresponds to the probability of having two items in the system. So one multiplied by p two one plus p two two plus p two three. And the result is 0.115 jobs. Then let's compute also the throughput that is lambda effective. That is so lambda three multiplied by one minus the probability that the system is full.
And this probability, again, is the sum of the three probabilities, p two one, p two two, and p two three. And the result is 2.655 jobs per hour. Then finally, let's compute the cycle time as divided by throughput. So 0.558 divided by 2.655. The result is zero point twenty one hours.
And the cycle time in queue, We put in queue divided by the throughput, 0.115 divided by 2.655. The result is zero point zero forty three hours. Okay. So here we have computed the performances, and this was the the questions of the exercise. Here, we can also notice that the cycle time in queue is quite low because if you analyze the system, here we have so an arrival rate of three jobs per hour.
But so the machine has a processing rate of six jobs per hour. So it means that the utilization is not very high. And, thus, we expect not to have high an IQ, a large number of items waiting. Then, regarding the question, so an example of a real situation in which such function with these different phases apply. Well, you k.
This is a good question, but you you cannot so you have not to imagine this exercise. So in the real case, you just know that, okay, you have the your processing data that can be approximated by a distribution of type Erlang three, and then and then that's it. So in the real case so the real case is not dividing the the Erlung. So it's not possible perhaps to divide the process and see it as the sum of exponential distributed process. Or you have a real process in which you can identify three sub processes, so three different operations.
So you have three operators that work in series, and each of them takes so the the processing time follows an exponential distribution with the same average of all the others. And in this in this case, you can represent the total distribution of the series of these three operation as an Erlang distribution. And in this case, you can visualize this example. Okay? So imagine that you have three operators.
Each of them execute an operation on the item. They are in series, and they can they are they have the same average time. And all of them follows an exponential distribution with the same average time. So in this case, you can model the total process as the the three phases of the air lung because the total process is the sum of these three independent and identical exponential variables. Okay?
This is a way to visualize what it happens. Otherwise, this is just an example to familiarize with the state diagrams. And because in this way, we are considering the exponential distributions. And so we can represent the state diagram where each state so the the movement from a state to the following only depends on the current state. It doesn't consider the past of the state.
So only in the case of exponential or Erlang seen as the sum of exponentials, we are able to represent the state diagram and the movement from one state to the other. Instead, if we have the other distribution, that's not possible. But then this is a very specific example of a limited system with a small amount of items allowed. So we are able to do this exercise by hand. So representing the small diagrams and write small numbers of equations, solve the system, and compute the WIP and the cycle time in this way.
In general, when you have a unlimited system, you directly use the formulas. Okay? So independently of the type of distribution, independently on how you represent the state diagram, you just use the formulas or implement a simulation model to to compute the performance in the of the system. Okay? But for this case, for the Erlang three, as in this example, you can visualize it in this way.
So consider three operations in series with the same the same average time. Okay. So our exercise, then the state diagram, then the nod isolations. So regarding these, these kind of exercises that you can find, in the the exam, since I don't want you to lose time solving the system, this kind of exercise is divided into two types. Or I write you the text, and I ask you to compute to draw the state diagram and to write the equations.
Okay? So the first part, the text, and I expect you that you are able to derive the diagram and write the corresponding equation. Or the other types is that I directly give you the probabilities, and I ask you to compute only the performance measures. Okay? So in both cases, you don't have to spend the time solving the system.
Okay? So or the system is very simple, and then you can just solve it by substitution. Or I won't ask you to solve the system, but I directly give you the probabilities if I ask you to compute the performance. Then here you have also the the Excel code to compute the inverse of the matrix and derive the performance, the probability values. And this is the the final computations.
Okay? So this is the solution that then I will upload. Then here, I prepared today. So I extracted an exercise taken from the past exam of last year where you have an example of the second type of this exercise. For instance, here, you have the text.
So consider an m e three one three model with an arrival rate of four jobs per hour and a service rate of eight jobs per hour. So I ask you to compute the system performance measures of throughput, WIP, WIP in queue, and cycle time given the steady state probability vector. Okay? So in this case, don't ask you to develop the diagrams or to write the balancing equation, but I directly give you the probability vector. So these in this vector, you have the probabilities of being in each state.
And I ask you to find to compute the performance measure. Okay? Okay. So the throughput is equal to lambda effective. So lambda multiplied by one minus the probability of, let's call, n max, the probability of having the maximum number of items in the system.
And in this case, four that multiplies one minus 0.0415. This should be the sum of the three probabilities, and the result is 3.834 jobs per hour. Then the whip is the sum of p one one plus p one two plus p one three plus two multiplied p two three plus p two sorry. Two one, two two, and p two three plus three multiplied p three one plus p three two. One one, one two, and three.
Mhmm. You plus p three three, and the result is 0.694 jobs. Then the weeping queue is p two one plus p two two plus p two three plus two that multiplies p three one plus p three two plus p three three, 0.2148 jobs. And the cycle time is whip divided by throughput. 0.694 divided by 3.834.
Zero point one eight one hours.

Ok, so now, until now we have a sin only the case the cazes of exponicial or erland distribution of a times. Now, let's generalize the concepts that we have seen, in order to derive the formulas to computer the performances is of system of types of type MG1. So where M, so di Arrival Times follow always exponation distribution, in stead the processing times follow generic distribution. So we mantane the same parameter, so lamda is always the minerate of the arrivals, and the moo is the minrate of the processing. So the service the everage service time is one over mu, and we call it's variance Sigmas squared.
So seans now we have general distribution is not an uf to indicate the mean value as for the exponational, because for the exponation we only need one parameter for the exponation distribution, so the average. In Stade for a General Distribution, we have two value, the average and the standard deviation, or devariance, Sigma S, or Sigma Square. So in this case we don't use the state diagram approach because the sistem are unlimited. And we don't derive the formulas that list we take some formulas as given. For instance this is the formula from witch we start the polla, zek and the kincine, pk formula, to compute in the whip in NMG1 System.
So the whip of the system that we know we is the expected number of items in the system is given by this formula. Where the parameter sard the one that we a valority defined, so lambda, mu, sigma, square and stop. Let's rewrite this formula and the see how this formula can be changed a little bit, so combined with other formulas, to optain the final formula to use to computer the performance of an MG1 System. So, let me take again the otherboard. Reprite it.
So, here we have the performance of MG1 system, unlimited system, always one machine in the workstation, arrival exponation distributid and processing time generic, following generic distribution. So, we take the PK formula that compute the WIP at this the expected number of jobing the system, you of an, è lambda divided by mu, plus, lambda divided by mu, squared, plus, lambda s squared divided by two that multiplies one minus lambda overboom. This is the PK formula. And the we don't to derivit. Then from this formula, let's compute the weep in q.
Let's remember that as for the cycle time, the formula for the total cycle time, is the summ of cycle time in Q, plus the everage processing time. So, so for the weep we can write e similar formula. So, the total weep is the summ of weep in Q, so di everage number of items waitining the q, plus di everage number of items in the workstation in the machine that can be breaten as expected value of NS. The expected number of items in the machine. This quantity here corresponse o so to the utilizzation of the machine.
Utilization. And does can be breathen as lambda over moo. So I furie member, lambda overmou is they utilizzation. The utilizzation is a value between 0 and one. Four istant sifity 0 point five.
It means that the machine is used at fifty percent of time, and it means that the ever age number of items inside the machine is 0 point five. Ok. So the total weep is the sum of the average number of items in the que and the average number of item in the machine, in the server. End this last term corresponse today utilizzation facture. End that can be rebreat ne slam dover who.
This quantity is use the here mecause if we want to compute the weep in q, then we can write it as weep minus the utilizzation, so lambda over moo. Then let's use the pic ary formula to express the whip. And you see that the first term this one is the same of this one, so, he we do the whip minus they utilizzation, we optain the second term o the formula. So, lambda overmut squared, plus, lambda squared, divided by two that multiplies one, minus, lambda overmu. These is the expression of the weep in q.
Then, let's use the weep in q to compute the cycle timing q. Cycle timing q by use in delit slow is given by wip in q, divided by the thruput. Here the thruput, wech is the thruput. The thruput for NMG1 system, so unlimited system is equal to lambda. So the thruput is equal to lambda in this sistems.
So, let's divide the weep in q, computing before by lambda. So, we obtame lambda overmue squared, my juster repright, plus lambda squared, sigma s squared, divided by two, one minus lambda overmove, multiplied lambda. Ok, Naulets Gone, Solving disequation, and Naulets Revrite Determa Sigma Square S, in function of the coefficienti of variation. So, I furiemember we defined, sì, as aderation between Sigma and the mean value. In this case is io ts, because we are talking about the processing times.
So, cs is equal to Sigma S divided by EOTS. So in this case, iovts is the inverse of moo. The processing times e inverso of the processing rate. And as, sees, che non so bevritten as sigma s multiplied by mu. E from here widerive sigma s as, cs, divided by mu.
C'è una use this formula in our main one. So the first term is the same, so, lambda square divided by moo square, plus, lambda Square that multiplies CS Square divided mu Square. Divided by the denominator. Two lambda multiplied one minus lambda over mu. Ok, than, let's do the commond enuminator at the numerator of this expression.
Town let's write here. So we have lambda squared, divided my move squared, and this is multiply by one plus CS squared, and thanet the denominator we have two lambda one minus lambda over mu, So we semplify lambda. And then here. Let's write at the beginning of this expression one più CS Square divided by two. Then this therm multiplies.
The other therms let's all sto recald that lambda divided by moo is the utilizzation. So, let's write utilizzation, divided by one, minus utilizzation. And then we avelor re the last term remaining is one, divided by mu, and one divided by mu, is e qual to e-ofts. Ok, so, in the end we find that this this this this mg one is equald to one più cs squared divided by two that multiplies you, divided one-u that multiplies you this. E'm.
And this expression is very similar to the one of the cycle timing qeue of type of system MM1 di fiore member. Mh? Because this part here is the same of the cycle timing q for system MM1. So, weekend conclude that the cycle timing q for system in wich the processing time follow a generic distribution is this cycle timing q for type m1, software exponation systems, multiply by this coefficienti. End this coefficienti depense on the variability of the processing time.
Ove CS Squared. So in case of exponation, so one this therm this coefficienti is one. Discoefficienti is one for MM1 System. Ok? So the formula of MG1 is also valid for MM1 System.
Because the first coefficienti is reduced to one. And does we obtain the formula that we have sindulast time can be voth heire or lower or equal to the corresponding system with the same parameter, so the same utilizzation, the same processing time of a system of type MM1. Becaused depends on the variability of the distribution, of the processing time. If the variability is lower than one, so if CS is lower than one, then the first the the coefficienti isloweden one, and does the cycle timing queue is lower. In stead if the variability is haire, so cs is here than one, the coefficienti is lower than one, is so, is here than one, and does the cycle timing q is here than the corresponding system with exponation times.
Ok? Your we follow the steps that we did together and we obtain the cycle q and recalling the formula of the variability and the formulas of the MM1 System. We obtain the cycle timing q è this expression, one plus cs square over two, multiply by u, divited by one-u, multiplyed iots. E this expression che mi breat nast the coefficienti one plus CS Square dividied by two multiply by le cycle timing q of system MM1. And then let's do also the next step.
That is generalize also the system for type GG1. Ok? So, as we generalized for type gm one, where we introdust in the formula of the cycle timing q alls of the effect of the variability of the processing time, Here if in state of aving the exponational arrival rate, we have generic distribution. Here let's see that we including the formulas of the variability of the arrivals. End as the final formula is CA squared più CS squared divited by two.
Where CA n CS ard the coefficienti of variation for the interarrival distribution and the service time distribution. This is the Kingman equation and if he are we substitute the formula o the cycle timing q of system MM1, we obtain this equation, that is also call the vee uthie equation. Because it the moltiplication of three terms. The first one is an expression of the variability of the system. The second one is and expression of the utilizzation, and the thered term is the time, the process time.
So di acronim is V-U-T. V-U-T equation. Ok from the psicle sto at this is the quassion for the cycle time than we know that to obtain the total cycle time we start from the cycle time in q e nd we some the processing time. So the expression for the total cycle time can be all soverytten by summing to deve you tee equation that processing time, the average processing time. Weekend noties that in this formula we don't have the e qual symbol because this formula sar approximations.
Ok? So, when we don't have only exponations the formulas formulas give us only approssimation of the le performance measures. Ok? So, in our exercizes and, in our cases this approssimational fine. So remember that this are not exact value.
No, I think that this point. Ok, let me read the questions. So what is CS? Yes, CS, is the coefficienti o variation of the service time, so of the processing time. So, Cs is computies desideration between Sigmas, this the standard deviation of the processing time, and EOTS, that is the average value of the processing time.
We defined the coefficienti of variation at the beginning of this set of slides, when we talk about the variability. End we say that in order to compute and index that measured the variability of a distribution. It's not an af to consider only the standard deviation and the devarions. Buttits better to considerer Sì, that is the ratio between the standard deviation and the mean value. So, CS is the variability of the processing times and CA is the the same therms therms but computed on the arrival times.
Ok? Rewrite the Ok. And this formula is that. Cycle timing q of system GG1 is allmost equal to CA Square più CS Square divided by two multiplied cityq of system MM1. Multiplide Utilization, Divided One, Minus Utilization, Multiplide by Processing Time, IoTS.
Mh? End this is cold the VUT equation. End the VUT from the acronim of variability. The first term, is the everage variability, between the arrival and processing in times, thank you eas for utilizzation and that third term is the time. Mhmm.
Variability, utilizzation, time. V-U-T equation. End from the formula aud the cycle time. Week end derive ors the formula of the total. From the formula of the cycle time in que.
With derive the formula aud the total cycle time of the system, lo cycle time gg one is equald to cycle time inq, gg one, plus eofts. End remember alls that this formulas were define for GG1 system but are valid all so four the specific asystem, so are valid all so four MM1. Because for MM1 the first coefficienti of CA and CS easy quat to one. It's enouf to remember the final formula, the more complex one, and this formula is always applyable, all so to the morsed simple cases. Ok.
No, let's see the examples. Sono a we are here, let's see the example, the numerical examples. So, considery system with lambda equal to four jobs per hour, and moo five jobs per hour, yelding utilizzation factor of UA0 0.8. Sist this was an exponation assistant we had, CANCS square equal to one, and iovts equal to 0 point two hour. Ok, so this is the example of applying the general formula all so four the exponation cazes.
So here in the example we have. And sims the distribution are exponations, weekend 6 that sia isquare is equald sias square, that is equald to one. Because the exponation distribution as the standard deviation equal to the minvalue. So there is equal to one. So the utilizzation computid is lambda divided by moo is 0 point 8.
E so and so the e-ofts. Is the inverse of the processing rate 0 point to hours. So buy using this input parameters we are able to computer the cycle timing q. Mhmm. Orso by applying the formula for the general system.
Recause the first term is one plus one, divided by two, so one. Bene, utilizzation, divided by one, minus, utilizzation, multiply by the processing time. So the cycle timing quedsystem is 0 point 8. And then from here we can computo all the other performance measure, so the cycle timing by summing the cycle timing cuue and processing time, and then the then this equal to lambda, and then the cycle time and cycle timing cuue by using the little slow. Let's seely other example.
Here we have, è GG1 System, with interarrival times, distributied according to a gamma distribution, with minutes and standard deviation thirty minutes and width service times distributies d'according to a Nearland 4 distribution width minutes. Syns distribution of services no, ok. So this hard e input data. Hear the next sentasies that, I benefit is breat and that, that reas and erlang distribution, since this is and unlimited system, you can not use the state diagram, ok? So don't be confused by the example where we develop the state diagram and we compute the probabilities, ok?
Because that prosiedure can be applied only for the limited system. Here in stead, it doesn't care that type ob the distribution, so, all sto in this example, we have gamma distribution, and and erline distribution. But here the things that are important are only the value of the mean and the standard deviation. GG1. With the reinter arrival times distributies that accordi in 2 gamma distribution with the min, fifteen minutes.
So hear we have the min time between arrival, so heavetheas fifteen minutes and a standard deviation, so sigma a, of thirty minutes. End the service time is distributies thought in here lang four distribution, with a mean of twelve minutes. And the distribution is and erlang for. Four the processing time. So from this data we al relieve the min value, so we need to compute CA and CS, squared, so the coefician to variation.
In order then to insert them in the formulas. So here the CA squared is sigma A Squared divided by EOFTA. So, thirty divided fifteen is two than square it is four. So, sia is square is four. Here you, you see, we have a high variability, o di arrival, so, the standard deviation two time the minvalue.
E reguarding the processing time, CS Square is one divided by key this is the property of the ERLANG? It was breathening day one of the preview slide, software di ERLANG we know that cs square is one divided by key, where key is this number. So in this case is one divided by four, so 0 point twentyfive. Ok? So in general we have in this kines of exercises the value of the average time and standard deviation, or directuly the average time and the coefficient of variation, and by using this parameter we are able to apply the formula.
So, here we compute they utilizzation. The utilizzation is lambda over mu and che no so beveryten as day inverse, so iofts, divided eofta. Twelve divided fifteen this 0 point eit. And then let's apply the formula. No that we have all the formula, so the cycle timing q for this system is CA Square Plus, CS Square, Divided by two, Multiplyed Utilization, Divided One, Minus Utilization, Multiplide by EOFTS.
So, in numbers, four più 0 point twenty five, divided by two, multiplied 0 point two, multiplied 0 point two. There is one point seven owers. Ok. So you see this is the same so, è an exemple simil or to the preview one? All so in the preview one, in the exemple here we have lam dow four and the move five.
Detto expressid in minutes are the same value as this exemple, infatti the utilizzation is 0 point 8. And here the cycle time was 0 point 8. In stead here that meas that we have and here variability, in the arrival time. So, the effect is that we have this here than point is not that we that gg one system we have always more variability than the m and one system. In In this case yes.
Mhmm. Vat. I depense on the value of the standard deviation or the coeficient of variation. Mhmm. Vat we can see that the variability as and I impact as we have seen all so before, I fuer a membering, the simulation model, I show you effect o the variability on the system.
Our not, because sometimes, I I'm confused. I don't remember, I show you the simulation model of the system by changing the variability. Tu si dette, if if if if and yes the other performance measure, so ones we have so in this kind of exercise we usually start by computing the cycle time, Ok? So you computer the cycle time in q of the system, and then from the cycle time in q, uals derive the total cycle time, by summing the processing time, and then the whip and the whipping q, by upline the little slow. By multipling the cycle time and the cycle time in q for the threat it is yequal to lambda.
One exercise for you. So, that's just uply the formula by using this data. So, we have a work station we we station we have and an everage processing time of twenty minutes, so 0 point twerty three hours, and a coefficienti of variation of two point five. So the second proceses not exponation distributid. So computer the performance measure.
Computer firstly the utilizzation to check the value there and then the performance measure. Vai applying the formula O del GG One System. Ok, so let's apply the formula. Tuo computer this cycle time in q. One, CA Square is one, plus, CS Square, six point twenty five, divided by two, multiplice deutilization 0 point nine five eht three, dividid by one, minus 0 point nine five eht three, Rootty ply by twenty minutes.
If we want to to express the cycle timing minutes. Other why see use the hours. End the resut is twenty seven point seventy seven. Hours. So, you fudo the computation, you obtain a number that is in minutes and then you converte it in hours.
Then the weep in q is thruput multiply by this icon timing q. And the thruput, so let's remember that the thruput of the system is easy quat to lamda. So two point height seven five. So the whip is thruput multiplied cycle timing que and the resout is have than then the total cycle time, this the cycle timing Q più the processing time, UTS, so' twenty-have punto one hours, end the total wheap thruput multiply the cycle time. Let is at one.
So here you see that. In this case we have an I utilizzation 0.96. And we also have a high variability and the number of items waiting is ahighty. Ok, everything fine. Having finish the exercise.
Then let's see the final formula that is the approssimation for GGC Systems. Ok? So until now we we have start from the system MM1, so one one machine and times exponation distributid. Then we have sin the formula of MMC System, with times exponation distributid but multiple machines in parallel. Then we have sind the system GG1, soy get one machine and general arrival and processing time, neolats, see the approximation for GGC System, where we have alse of paralend machines.
Soy here again we don't dimostrate formula but we apploud we use the hallen and canin formulas, that is base on the Kingman equation, and then was adjusted by hal to be an extension of the MMC System. So the important relationship is that the cycle timing q of GGC System is equal to the coefficient that we introduce for the g g system multiply by the sicle timing q of MMC system. So let's right together the formula. So, this is contining q for GGC system, is equal, allmost equal, approximates, CA Square più CS Square, divired by two, that is the coefficienti in case of variability, That multiplies the cycle timing q of system MMC. Then, in fuer a member this value, so the cycle timing q for MMC System is given by they utilizzation at power of route square of two c più two there -one outsider route Square, divided by two this End this term multiplice EOFTES.
Ok? So the final formula to computer the cycle timing q for the general system is CA Square più CS Square divided by two that multiplies you at that can mee uplyed all so in all di other systems. Because if in stead of g g we have m or both m or only one m, for the arrival or for the processing, we modifify they CA Square and CS Square, and If we don't have a see, see is equal to one than this a term here reduced to you divided one minus you. If see is equal to one. If see is equal to one this a term is you divided one minus you.
So, buy using this formula we can solve all the problems. And this is one of the formula that I will provide you doing the exam. Ok? So, I don't provide you all the specific formulas for reach specific case, ma that I provide you the general formula that you can apply in all the cases. Ok?
So, you have to understand the mining of the variables in the formulas. But then the formula you have it. You don't have to memorize the formula. So here we have the final formula, tycle timing q of time GGC, the last one, here, and let's see the final example. So here we considerer the system, so the same So, we have the same parameter, so, lambda is four, jobs per hour, and CA Square, CA Square is four.
Then. Than, you of ts, twenty four minutes this is the new date, thank you thank thank you thank thank ok, that you are steel given, this is a gain an other input data. And see that is the number of parallamachines is two. So let's apply the formula, CTQ of this system, we have, CA Square, it is four, plus, CS square 0 point twenty five, debuded buy two, that multiplies. They utilizzation.
He are another thing what is the definition of they utilizzation. Usually day utilizzation is lambda divided by mo. Butter this is the formula where we have only one machine. Because, hee we have morden one machine here at the denominator win eat two insert the to total capacity, the total production rate of the work station, not the single machines. Multiplied by see.
Because this is the total production rate of the work station. Ok? So I they utilizzation is lambda, the arrival rate, divided by the processing rate of the whole work station, ok? Not the single machine, ok? So remember that when computing they utilizzation, he we have more them one lambda four divided by two moo and the moo is in hours is sixty divided twenty four.
So they utilizzation is lambda divided two mou. So four divided two that multiplies moo and the moo is sixty divided twenty four, expressed in hours. So they utilizzation is 0 point eit. Ok, so we use thany utilizzation, key a link the formula. So 0 point height power of route square of two multiplied c più two, so six, -uno, upside the road square, divided by C two, that multiplies one, -utilization 0 point 8.
That multiplice youf this. Here are use the ours, so 0 point four ours. Ok, so in this exercises we only need the everage value of the times and the coefishing to variations of the arrival time and the processing time from this data we compute they utilizzation and then we apply the formule of the cycle timing q. And then from this formula we compute all the other performance measure.

## Bridge Notes:

When modeling a single workstation with heterogeneous servers (where $\mu_{fast} \neq \mu_{slow}$), the following rules must be strictly followed to ensure the accuracy of the Continuous-Time Markov Chain (CTMC).

1. State Space Definition (Micro-States): To avoid the error of "over-aggregation," do not use a simple integer $n$ (total jobs) as the state. Instead, use micro-states that explicitly identify which specific machines are occupied.

0: The system is empty.
  $1f$: One job is being processed by the fast machine.
  $1s$: One job is being processed by the slow machine.$2fs$: Two jobs in service (one on fast, one on slow).
  $2ss$: Two jobs in service (both on slow machines), with the fast machine idle.
  $3$: All three machines are occupied.
  $n > 3$: All machines are occupied, plus $n-3$ jobs waiting in the queue.

2. Routing Logic & Reachability: The modeling must reflect the "Fastest-Free" assignment policy while accounting for service-driven transitions.
   Fastest-Free Rule: If the system is in state $0$ and a job arrives, it must be assigned to the fast machine ($0 \to 1f$).
   Service Transitions: States like $1s$ and $2ss$ are often unreachable via arrival arcs but must be included because they are reachable via service     completions.

   Example: From state $2fs$, if the fast machine finishes first, the system moves to $1s$ ($2fs \xrightarrow{\mu_f} 1s$).
   Example: From state $3$, if the fast machine finishes, the system moves to $2ss$ ($3 \xrightarrow{\mu_f} 2ss$).

3.KPI Calculations (Performance Metrics): Performance metrics must be calculated by weighting the steady-state probabilities ($\pi_x$) of the specific micro-states.
  Work-In-Process (WIP)The total WIP is the weighted sum of the number of jobs $n(x)$ in each micro-state $x$:
  
  $$WIP = \sum_{x \in S} n(x) \cdot \pi_x$$
  
  Throughput (TH)For systems with a finite capacity $K$, the throughput must account for the blocking probability at the maximum state:
  
  $$TH = \lambda \cdot (1 - \pi_K)$$
  
  Cycle Time (CT)Calculated using Little’s Law:
  
  $$CT = \frac{WIP}{TH}$$

  
