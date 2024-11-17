
#include <iostream>
#include <vector>

using namespace std;

// Function to calculate CGPA
double calculateCGPA(const vector<int>& grades, const vector<int>& credits, int numSubjects) {
    double totalWeightedGradePoints = 0;
    int totalCredits = 0;

    for (int i = 0; i < numSubjects; i++) {
        totalWeightedGradePoints += grades[i] * credits[i];  // Sum of grade points * credits
        totalCredits += credits[i];  // Sum of all credits
    }

    return totalWeightedGradePoints / totalCredits;  // CGPA = Sum of weighted grade points / total credits
}

int main() {
    int numSubjects;

    // Input the number of subjects
    cout << "Enter the number of subjects: ";
    cin >> numSubjects;

    vector<int> grades(numSubjects);
    vector<int> credits(numSubjects);

    // Input grades and credits for each subject
    for (int i = 0; i < numSubjects; i++) {
        cout << "Enter grade for subject " << (i + 1) << " (0-10): ";
        cin >> grades[i];

        // Validate grade input
        while (grades[i] < 0 || grades[i] > 10) {
            cout << "Invalid grade. Please enter a grade between 0 and 10: ";
            cin >> grades[i];
        }

        cout << "Enter the number of credits for subject " << (i + 1) << ": ";
        cin >> credits[i];

        // Validate credit input
        while (credits[i] <= 0) {
            cout << "Credits must be positive. Please enter valid credits for subject " << (i + 1) << ": ";
            cin >> credits[i];
        }
    }

    // Calculate CGPA
    double cgpa = calculateCGPA(grades, credits, numSubjects);

    // Output the calculated CGPA
    cout << "Your CGPA is: " << cgpa << endl;

    return 0;
}
