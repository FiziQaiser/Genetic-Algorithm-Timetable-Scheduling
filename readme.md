# Timetable Scheduling System Using Genetic Algorithm

## Project Description

Timetable scheduling is a classical problem in university environments, where a timetable is created for each semester, ensuring minimal clashes between sections, professors, and rooms. This project aims to solve the timetabling problem by assigning time slots to each section in specific rooms with designated professors for particular courses.

Each week includes:
- Two classes per theory course, each lasting 1 hour and 20 minutes.
- One lab session per lab course, lasting 3 hours.

## Features

### Hard Constraints

These constraints must be met without any compromises:
- **Classroom Availability**: Classes are scheduled only in available classrooms.
- **Classroom Capacity**: Classrooms are categorized into two types based on capacity: standard (60 seats) and large halls (120 seats).
- **Professor Scheduling**: A professor cannot be assigned two different lectures at the same time.
- **Section Scheduling**: A section cannot be scheduled in two different rooms simultaneously.
- **Room Allocation**: A room cannot be assigned to two different sections at the same time.
- **Professor Course Load**: No professor can teach more than 3 courses.
- **Section Course Load**: No section can have more than 5 courses in a semester.
- **Lecture Distribution**: Each course must have two lectures per week, not on the same or adjacent days.
- **Lab Scheduling**: Lab lectures must be conducted in two consecutive slots.
- **Transition Time**: A 15-minute break is allowed between consecutive classes to ensure sufficient transition time.

### Soft Constraints

These constraints should be implemented as best as possible, with some room for compromise:
- **Session Timing**: Theory classes should be held in the morning, and lab sessions in the afternoon.
- **Minimized Movement**: Minimize the number of floors teachers and students need to traverse.
- **Consistent Classrooms**: Classes should ideally be held in the same classroom throughout the week.
- **Teaching Blocks**: Teachers may prefer longer blocks of continuous teaching time to minimize interruptions and maximize productivity, except when the courses are different.

### Additional Details
- **Timetable Coverage**: The timetable covers all 5 days of the week, with morning sessions from 8:30 AM to 2:30 PM and afternoon sessions from 2:30 PM to 5:30 PM.
- **Chromosome Encoding**: Chromosomes are binary encoded with the following information:
  - Course
  - Theory/Lab
  - Section
  - Section-Strength
  - Professor
  - First-lecture-day
  - First-lecture-timeslot
  - First-lecture-room
  - First-lecture-room-size
  - Second-lecture-day
  - Second-lecture-timeslot
  - Second-lecture-room
  - Second-lecture-room-size
- **Fitness Function**: The fitness function is the inverse or negative sum of all conflicts/clashes.

### Foundational Code

The project follows the classical genetic algorithms’ cycle with the following steps:
- **Reproduction**
- **Crossover**
- **Mutation**

## Getting Started

To get started with this project, clone the repository and follow the setup instructions.

### Prerequisites

- Python 3.x
- numpy
- pandas

### Installation

1. Clone the repository:
   ```sh
   git clone https://github.com/FiziQaiser/Genetic-Algorithm-Timetable-Scheduling-.git
   ```
2. Navigate to the project directory:
   ```sh
   cd "Genetic Algorithm (Timetable Scheduling)"
   ```
3. Install dependencies:
   ```sh
   pip install numpy pandas
   ```

## Contributing

Contributions are welcome! Please fork the repository and submit a pull request.

## For More Details

For more details, please refer to the [full report](./Report.pdf) and [question](./Question%20-%20Timetable%20Scheduling.pdf).
