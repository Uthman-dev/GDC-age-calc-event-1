# GDC age calc event 1
 age calc

/*
Breakdown of the JavaScript Code:
1. Input Value Retrieval:
const day = parseInt(document.getElementById("Day").value);
const month = parseInt(document.getElementById("Month").value);
const year = parseInt(document.getElementById("Year").value);

 * document.getElementById("Day").value: This part accesses the input field with the ID "Day" and retrieves its value.
 * parseInt(): This function converts the retrieved string value (from the input field) into an integer. This is necessary for mathematical operations.
 3. Input validation :
if (month < 1 || month > 12) {
    alert("Month must be between 1 and 12.");
    return;
  }

  if (day < 1 || day > 31) {
    alert("Day must be between 1 and 31.");
    return;111111111111111111
  }

  if (day < 0 || year > 2024) {
    alert("year must be current.");
    return;
  }

3. Getting Current Date and Time:
const today = new Date();
const currentYear = today.getFullYear();
const currentMonth = today.getMonth() + 1; // Months are 0-indexed
const currentDay = today.getDate();

 * new Date(): Creates a new Date object representing the current date and time.
 * getFullYear(), getMonth(), getDate(): These methods extract the year, month, and day from the Date object. Note that getMonth() is 0-indexed, so we add 1 to get the actual month.
4. Calculating Age:
let ageYears = currentYear - year;
let ageMonths = currentMonth - month;
let ageDays = currentDay - day;

 * Initial Calculation: Calculates the difference in years, months, and days between the current date and the input birthdate.
5. Adjusting for Negative Differences:
if (ageDays < 0) {
  ageMonths--;
  ageDays += new Date(currentYear, currentMonth - 1, 0).getDate();
}

if (ageMonths < 0) {
  ageYears--;
  ageMonths += 12;
}

 * Handling Negative Days:
   * If ageDays is negative, it means the input birthdate's day is greater than the current day.
   * We decrement ageMonths by 1.
   * We add the number of days in the previous month to ageDays using new Date(currentYear, currentMonth - 1, 0).getDate().
 * Handling Negative Months:
   * If ageMonths becomes negative after the previous adjustment, it means the input birthdate's month is greater than the current month.
   * We decrement ageYears by 1.
   * We increment ageMonths by 12.
5. Displaying the Result:
const outputYear = document.querySelector(".output h1:nth-child(1)");
const outputMonth = document.querySelector(".output h1:nth-child(2)");
const outputDay = document.querySelector(".output h1:nth-child(3)");

outputYear.textContent = ageYears + " Years";
outputMonth.textContent = ageMonths + " Months";
outputDay.textContent = ageDays + " Days";

 * Selecting Elements: Uses document.querySelector() to select the three <h1> elements within the .output div.
 * Updating Text Content: Sets the text content of each <h1> element with the calculated age in years, months, and days.
By following these steps, the code accurately calculates and displays the user's age in years, months, and days.
 * https://github.com/kiptimemmanuel/ip2
 * https://github.com/TomeRoque/digital-portfolio
    */





