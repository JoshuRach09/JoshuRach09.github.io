[Back to Portfolio](./)

Lab 04 - Bowling Scores
===============

-   **Class: CSCI 301** 
-   **Grade: 93** 
-   **Language(s): Perl** 
-   **Source Code Repository:** ([lab04](https://github.com/JoshuRach09/CSCI-301-code-repository/tree/master/lab04))  
    (Please [email me](mailto:jrachel@csuniv.edu?subject=GitHub%20Access) to request access.)

## Project description

This Perl script processes bowling scores from a text file named 'scores.txt', where each line contains a player's name followed by their score. It calculates the average score, identifies the player with the highest score, and sorts the players by their scores in ascending order. The results are written to three output files: 'average.txt' for the average score, 'winner.txt' for the winner's name and score, and 'sorted.txt' for the sorted list of players and scores.

## How to run the program

The perl script does not require compilation. To successfully run the program, please ensure that 'scores.txt' is present in the same directory and is formatted "name score" on each line. To proceed with executing the program, you will need to do the following.

```bash
cd ./lab04
perl lab04.pl
```

This program will generate three output files: average.txt, winner.txt, and sorted.txt

## UI Design

This is a command-line script without an interactive user interface. The user runs the script in a terminal, and it processes the input file silently, producing output files. Users can view the results by opening or using the Linux command "cat" to view the output files. The program execution starts in the terminal (see Fig 1). After running, the example output can be viewed in the generated files, such as the sorted scores (see Fig 2). If an error occurs, such as a missing input file, Perl will display an error message in the terminal (see Fig 3).

![screenshot](images/dummy_thumbnail.jpg)  
Fig 1. The launch screen

![screenshot](images/dummy_thumbnail.jpg)  
Fig 2. Example output after input is processed.

![screenshot](images/dummy_thumbnail.jpg)  
Fig 3. Feedback when an error occurs.

## 3. Additional Considerations

Sed ut perspiciatis unde omnis iste natus error sit voluptatem accusantium doloremque laudantium, totam rem aperiam, eaque ipsa quae ab illo inventore veritatis et quasi architecto beatae vitae dicta sunt explicabo. 

For more details see [GitHub Flavored Markdown](https://guides.github.com/features/mastering-markdown/).

[Back to Portfolio](./)
