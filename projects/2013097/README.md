# ΙΟΝΙΟ ΠΑΝΕΠΙΣΤΗΜΙΟ 


# ΤΜΗΜΑ ΠΛΗΡΟΦΟΡΙΚΗΣ 


# ΜΑΘΗΜΑ
## Επικοινωνία Ανθρώπου Υπολογιστή

# Επιλογή Εργασίας
## Οπτικοποίηση δεδομένων χορηγιών (UK)

Κυριακή Μουταφίδου
ΑΜ Π2013097

## Παραδοτέο 1
### Ο σύνδεσμος της σελίδας με την εφαρμογή.

https://kikh.github.io/D3js-uk-political-donations/

### Αποθετήριο κώδικα.

https://github.com/kikh/D3js-uk-political-donations

#### 1) Εφαρμόστε τις κατάλληλες αλλαγές έτσι ώστε το url της εφαρμογής σας να μην χρειάζεται να καταλήγει σε "full-viz.html" (π.χ. από Mitsos.github.io/D3js-uk-political-donations/full-viz.html σε Mitsos.github.io/D3js-uk-political-donations/).

Μετονομασία του αρχείου full-viz.html σε index.html

#### 2) Αλλαγή χρωμάτων στις μπάλες με τα δεδομένα, καθώς και στα αντίστοιχα 3 πεδία της ομαδοποίησης Split by party.

Για την αλλαγή των χρωμάτων στις μπάλες με τα δεδομένα, o πιο εύκολος τρόπος είναι από το αρχείο charts.js αλλάζουμε τα χρώματα στη γραμμή “var fill = d3.scale.ordinal().range(["#31A000", "#6C0000", "#000678"]);”. Η αλλαγή των χρωμάτων στα 3 πεδία της ομαδοποίησης split by party γίνετε μέσω css από το αρχείο style css στα id #conservative, #labour και #libbem, αλλάζοντας το background στο καθένα από αυτά.

#### 3) Να ακούγεται ήχος κάθε φορά που ο χρήστης της εφαρμογής κάνει κλικ σε μία από τις επιλογές/κουμπιά ομαδοποίησης των δεδομένων.
Για να ακούγετε ήχος κάθε φορά που ο χρήστης κάνει click στα κουμπιά ομαδοποίησης των δεδομένων, στο αρχείο index.html δημιουργήθηκε ένα audio element με id audio και src το relative path του αρχείου mp3, το οποίο κατεβάστηκε από τη σελίδα https://www.soundjay.com/ και βρίσκετε στον φάκελο data του προσωπικού μου αποθετηρίου. Με τη χρήση javascript δημιουργήθηκε function play(); και σε κάθε ένα από τα κουμπιά προστέθηκε «onclick="play()"»

#### 4) Τροποποιήστε τον κώδικα έτσι ώστε όταν κάνετε κλικ σε κάθε μπάλα να ανοίγει ένα νέο παράθυρο με τα αποτελέσματα της αναζήτησης στο google για τον αντίστοιχο δωρητή.
Για να ανοίγει το νέο παράθυρο με τα αποτελέσματα της αναζήτησης google του δωρητή, στο αρχείο charts.js δημιουργήθηκε function googlesearch χρησιμοποιώντας το window.open της javascript.

#### 5) Ορισμένοι από τους αναγνώστες της εφαρμογής ενδεχομένως να είναι άτομα με περιορισμένη όραση. Τροποποιήστε τον κώδικα της εφαρμογής έτσι ώστε το ποντίκι να λειτουργεί και ως μεγεθυντικός φακός όταν μεταφέρεται επάνω από τις λέξεις του κειμένου.
Για το ερώτημα αυτό χρησιμοποιήθηκε η βιβλιοθήκη lettering.js. Όλα τα απαραίτητα αρχεία είναι στον φάκελο data του προσωπικού μου αποθετηρίου. Με τη χρήση του lettering.js και τον απαραιτητων τροποποιήσεων στο αρχείο style.css, επιτυγχάνετε η μεγέθυνση στης κάθε λέξεις ξεχωριστά όταν περνάει απο πάνω το ποντίκι. Θα μπορούσα να αλλάξω τον κέρσορα σε μεγενθυντικό φακό αλλά θα καλύπτει τα γραμματα.

#### 6) Για τον ίδιο λόγο, τροποποιήστε τον κώδικα της εφαρμογής έτσι ώστε όταν το ποντίκι βρίσκεται μέσα στον κύκλο κάποιου δωρητή, να ακούγεται η ονομασία του δωρητή και το ποσό της δωρεάς.
Για να ακούγετε η ονομασία του δωρητή και το ποσό της δωρεάς όταν το ποντίκι  το ποντίκι βρίσκεται μέσα στον κύκλο κάποιου δωρητή χρησιμοποιήθηκε το responsive voice. To plugin βρίσκετε στον φάκελο data του προσωπικού μου αποθετηρίου του κώδικα της άσκησης. Και ο κώδικας προστέθηκε στα ήδη υπάρχουσα functions του chart.js mouseover και mouseout

#### 7) Δημιουργήστε τουλάχιστον μία ακόμα επιλογή ομαδοποίησης των δεδομένων (π.χ. Split by the amount of the donation).
Επέλεξα την ομαδοποίηση "Split by the amount of the donation". Για την υλοποίηση, στο αρχείο chart.js δημιούργησα function GroupByAmounts και MoveToAmounts και επέλεξα να ομαδοποιήσω τα δεδομένα ως εξής: δωρεές μέχρι 100000, 100000 εως 500000, 500000 εως 1 εκατομμύριο και απο 1 εκατομύριο και πάνω. Χρειάστηκε να αλλάξω και τις μεταβλητές w και h των globals του chart.js για να προσθέσω μερικά pixel στο width και το height του svg.
