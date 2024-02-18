# Gym log
#### Video Demo:  https://youtu.be/MuVjvI4grYw
#### Description:
Gym log is an application ment to keep track of previous workouts.
This is done by creating custom templates, which contain different exercises of choise, complemented by weight and repetitions.
When starting a workout, you will be prompted to update the values of repetitions and weight.
These updated values will then be showed the next time you start the same template/workout.
All templates are stored as csv-files, in the same directory as the project.py file.

#### Menu options
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
Starting a template will make the program run through all the exercises in the given template, and ask for updated repetitions and weight for each one.
Once the user has given all of the exercises new values, the given template will be overwritten with the new set of values.
The name of the template will remain the same.

If you only have one template in the root directory of the program, that template will automatically be started when starting a template.
Should you ever have more than two templates, let's say template1.csv and template2.csv, will the program output all available templates.
From here you can simply just enter in template1.csv, or optionally just template1.
But remember that the inputted templatename must be written as case sensitive.

##### E - To exit the program.
As simple as that, just exits the program.

#### Functions

##### get_csv()
Returns all csv-files in current location, in this case the root directory of the project.
It returns all the files as a list, and returns an empty list if there are no csv-files in the directory.

##### create_exercise()
Takes as input an excersice, repetitions and weight, and returns a standard formatted dictionary.

##### exercise_valid()
Takes an exersice as input and returns True if the exersice is in the list of available exersices.
If the exersice is not in the list, the function returns none.

##### get_repetitions()
Makes sure the user input is a number only, catches ValueErrors, and returns the value.

##### get_weight()
Makes sure the user input contains at least 1 number, and optionally "kg", "kgs", "lbs", "pound", or "pounds".
The value is then returned, and the function also catches ValueErrors.

##### show_menu()
Simply just outputs the main menu.

##### save_template()
Requires a name, and a list of exercises as input.
The function then generates a csv-file with the given name, with the exercises as content.
