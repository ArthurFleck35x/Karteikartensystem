Von Projekt Karteikartensystem für Projekt Matrixcalc  <br>
MatrixCalc Projekt Git: ( https://github.com/CookieClickr/matrixcalc.offline )  <br>

# Grading Criteria Programmieren T3INF1004
In jedem Unterbereich werden die Punkte (gerne auch Links ins GIT) erklärt, wie das LO erreicht worden ist.  <br>
Alle Kriterien betreffen nur die Projektarbeit. Beweismaterial kommt aus dem Gruppenprojekt.  <br>

## FACHKOMPETENZ (40 Punkte)

# Die Studierenden kennen die Grundelemente der prozeduralen Programmierung. (10)
- Der Gauß Algorithmus funktioniert im Test. <br>
```  
def gauss_elimination(matrix):
    rows, cols = matrix.shape  # matrix.shape returns a tuple with the number of rows and columns
    steps = []  # Store the steps of Gaussian elimination

    for i in range(min(rows, cols)):  # Iterate over the minimum of the number of rows and columns
        pivot_idx = np.argmax(np.abs(matrix[i:, i])) + i  # Find the index of the maximum absolute value in the column
        matrix[[i, pivot_idx]] = matrix[[pivot_idx, i]]  # Swap the rows to move the pivot element to the diagonal

        if matrix[i, i] == 0:  # Skip if the pivot element is already zero
            continue  # Skip if the pivot element is already zero

        step = f"Pivot element: {matrix[i, i]}\n"  # Store the pivot element
        for j in range(i + 1, rows):  # Iterate over the rows below the pivot element
            factor = matrix[j, i] / matrix[
                i, i]  # Calculate the factor to eliminate the element below the pivot element
            matrix[j, i:] -= factor * matrix[i, i:]  # Eliminate the element below the pivot element
            step += f"Row {j + 1} -= {factor} * Row {i + 1}\n"  # Store the step
            step += f"Matrix\n{matrix}\n\n"  # Store the matrix
        steps.append(step)  # Store the step

    return matrix, steps  # Return the reduced matrix and the steps of Gaussian elimination
```


- Anmerkung zur Benutzeroberfläche: -Ikon, Buttons, welche die Größe der Matrix eingeben wären umsetzbar <br>

# Sie können die Syntax und Semantik von Python (10)
- Der Quellcode ist übersichtilich (mit Kommentaren versehen) gestaltet und eingerückt. <br>
- Mit der Funktion def gauss_elimination beispielsweise ("MatrixCalc.py") wird der Gauss'sche Lösungsalgorithmus eingebaut. <br>

# Sie können ein größeres Programm selbständig entwerfen, programmieren und auf Funktionsfähigkeit testen (Das Projekt im Team) (10)
- nutzen besispielsweise Unittest und eine GUI <br>


# Sie kennen verschiedene Datenstrukturen und können diese exemplarisch anwenden. (10)
- sie nutzen eine  .astype Funktion um Datentypen umzuwandeln. Außerdem auch Listen, Dictionarys und Tuple<br>
- "parse_vector_input(input_str)" um mit Buchstaben beispielsweise symbolisch zu rechnen <br>


## METHODENKOMPETENZ (10 Punkte)

# Die Studierenden können eine Entwicklungsumgebung verwenden um Programme zu erstellen (10)
- Das Programm ist strukturiert und auf Funktionsfähigkeit getestet. Es wurde GITHUB COPilot genutzt.  <br>

## PERSONALE UND SOZIALE KOMPETENZ (20 Punkte)

# Die Studierenden können ihre Software erläutern und begründen. (5)
- Dies wird besonders durch die Kommentare im Quellcode ersichtlich. <br> 

# Sie können existierenden Code analysieren und beurteilen. (5)
- Bei der Nutzung von Copilot und anderen Tools ist es "wichtig" den generierten Code zu verstehen um diesen zu erweitern oder anzupassen. <br>

# Sie können sich selbstständig in Entwicklungsumgebungen und Technologien einarbeiten und diese zur Programmierung und Fehlerbehebung einsetzen. (10)
-(Habe einmal gesehen das sie debuggen mussten und auch wie sie versucht haben zu Testen) <br>

## ÜBERGREIFENDE HANDLUNGSKOMPETENZ (30 Punkte)

# Die Studierenden können eigenständig Problemstellungen der Praxis analysieren und zu deren Lösung Programme entwerfen (30)
- Sie haben den Gauss'schen Lösungsalgorithmus programmiert und geben die Lösungsschritte mit der Lösung aus. <br> 

## Kenntnisse in prozeduraler Programmierung:

# - Algorithmenbeschreibung
- Der Quellcode ist mit Kommentaren beschrieben. <br>

# - Datentypen
- Vorallem Numpy arrays, aber auch Listen, Dicts … <br>

# - E/A-Operationen und Dateiverarbeitung
- Sie haben eine Gui über die man die Größe und die einzelnen Stellen der Matrixdynamisch eingeben kann. Anschließend werden die Schritte des Gaussverfahrens in lesbarem Text ausgegeben. <br>

# - Operatoren
- +,-,*,/,==

# - Kontrollstrukturen
- Zb. Überprüfung des Pivotelements in gauss_elimination <br>

# - Funktionen
- Eine Datei mit den Funktionen (MatrixCalc.py) und eine GUI-Main in der sie aufgerufen werden. <br>

# - Stringverarbeitung
Ja z.B. die Speicherung der Strings des Lösungsweges des Gaussverfahrens <br>
# - Strukturierte Datentypen
Ja z.B. Dictionarys und Listen (z.B. steps in Gauss_elimination) <br>
