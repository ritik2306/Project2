# Project2
#include <iostream>
#include <string>
using namespace std;

int Guess;
int Total;

class Question {
private:
    string Question_Text;
    string Answer_1;
    string Answer_2;
    string Answer_3;
    string Answer_4;
    int Correct_Answer;
    int Question_Score;

public:
    void setValues(string, string,
                   string, string,
                   string, int, int);

    void askQuestion();
};

int main()
{
    cout << "\n\n\t\t\t\tTHE DAILY QUIZ"
         << endl;
    cout << "\nPress Enter to start "
         << "the quiz... " << endl;

    cin.get();

    string Name;
    int Age;

    cout << "What is your name?"
         << endl;
    cin >> Name;
    cout << endl;

    cout << "How old are you?"
         << endl;
    cin >> Age;
    cout << endl;

    string Respond;
    cout << "Are you ready to take"
         << " the quiz " << Name
         << "? yes/no" << endl;
    cin >> Respond;

    if (Respond == "yes") {
        cout << endl;
        cout << "Good Luck!" << endl;
    }
    else {
        cout << "Okay Good Bye!" << endl;
        return 0;
    }

    Question q1;
    Question q2;
    Question q3;
    Question q4;
    Question q5;
    Question q6;
    Question q7;
    Question q8;
    Question q9;
    Question q10;

    q1.setValues("Question :What country has the highest life expectancy?  ", "India",
                 "Denmark", "Hong Kong",
                 "Japan", 3, 10);
    q2.setValues("Question :Where would you be if you were standing on the Spanish Steps? ", "Rome",
                 "Italy", "Greece",
                 "France", 1, 10);
    q3.setValues("Question :What year was the United Nations established? ", "1947",
                 "1945", "1943",
                 "1946", 2, 10);
    q4.setValues("Question :What artist has the most streams on Spotify? ", "Ed Sheeran",
                 "Justin Bieber", "The Weeknd",
                 "Drake", 4, 10);
    q5.setValues("Question : Aureolin is a shade of what color?", "Red",
                 "Yellow", "Blue",
                 "Black", 2, 10);
    q6.setValues("Question : What game studio makes the Red Dead Redemption series?", "CD Project",
                 "EA", "Naughty Dogs",
                 "Rockstar Studios", 4, 10);
    q7.setValues("Question :What country drinks the most coffee per capita? ", "Austria",
                 "Scotland", "Finland",
                 "Switzerland", 3, 10);
    q8.setValues("Question :Which planet in the Milky Way is the hottest? ", "Pluto",
                 "Venus", "Mercury",
                 "Mars", 2, 10);
    q9.setValues("Question : Which planet has the most moons?", "Jupiter",
                 "Neptune", "Saturn",
                 "Mars", 3, 10);
    q10.setValues("Question :Kratos is the main character of what video game series? ", "GTA5",
                  "Cyberpunk 2077", "Portal",
                  "God of War", 4, 10);

    q1.askQuestion();
    q2.askQuestion();
    q3.askQuestion();
    q4.askQuestion();
    q5.askQuestion();
    q6.askQuestion();
    q7.askQuestion();
    q8.askQuestion();
    q9.askQuestion();
    q10.askQuestion();
}

void Question::setValues(
    string q, string a1,
    string a2, string a3,
    string a4, int ca, int pa)
{
    Question_Text = q;
    Answer_1 = a1;
    Answer_2 = a2;
    Answer_3 = a3;
    Answer_4 = a4;
    Correct_Answer = ca;
    Question_Score = pa;
}

void Question::askQuestion()
{
    cout << endl;

    cout << Question_Text << endl;
    cout << "1. " << Answer_1 << endl;
    cout << "2. " << Answer_2 << endl;
    cout << "3. " << Answer_3 << endl;
    cout << "4. " << Answer_4 << endl;
    cout << endl;

    cout << "What is your answer?(in number)"
         << endl;
    cin >> Guess;

    if (Guess == Correct_Answer) {
        cout << endl;
        cout << "Correct !" << endl;

        Total = Total + Question_Score;
        cout << "Score = " << Question_Score
             << " out of "
             << Question_Score
             << "!" << endl;
        cout << endl;
    }

    else {
        cout << endl;
        cout << "Wrong !" << endl;
        cout << "Score = 0"
             << " out of "
             << Question_Score
             << "!" << endl;
        cout << "Correct answer = "
             << Correct_Answer
             << "." << endl;
        cout << endl;
    }
}
