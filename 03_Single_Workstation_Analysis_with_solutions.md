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

