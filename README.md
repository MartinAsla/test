# Gym log
#### Video Demo:  https://youtu.be/MuVjvI4grYw
#### Description:
Gym log is an application ment to keep track of previous workouts.
This is done by creating custom templates, which contain different exercises of choise complemented by weight and repetitions.
When starting a workout, you will be prompted to update the values of repetitions and weight.
These updated values will then be showed the next time you start the same template/workout.
All templates are stored as csv-files, in the same directory as the project.py file.

When starting the program, a menu will appear showing the available options.
The options are as follows:

##### C - To create a new template.
This gives the user the option to create a custom template in which multiple exercises can be grouped.
The different exercises will also be complemented with repetitions and weight used for each one.

It starts by asking the user to give the template a name, for which we will be refering to later.
Then it gives the user the option to either enter in an exercise, or enter in "h" to show a list of available exercises.
If entering in "h", it will first ask the user which body part to show the selection from, before presenting the list.
Say as an example i choose to see all available excersises for Chest, i will then get a list of all available exercises targeting that muscle group.

After the user enters in a valid excersise, it will be prompted to input repetitions and weight for that exercise.
The amount of repetitions will be required to be inputted as a number, weight on the other hand will also require a number,
but also supports measurements at the end. Available measurements are "kg", "kgs", "lbs", "pound", and "pounds".

When the first exercise has been added to the template you have the option to add more, or choose to save the template.
If you choose to save the template, all the exercises will be written to a new csv-file with the name of the template.

##### S - To Start a template.
