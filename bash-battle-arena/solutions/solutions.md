# Level 1: The Basics

mkdir arena
touch arena/warrior.txt arena/mage.txt arena/archer.txt
ls arena

---

# Level 2: Variables and Loops

# Create script.sh
touch script.sh
chmod +x script.sh

# Edit script.sh (example with vim)
vim script.sh

#!/bin/bash
for i in {1..10}
do
    echo $i
done

# To execute the script
./script.sh

---

# Level 3: Conditional Statements

# Create check.sh
touch check.sh
chmod +x check.sh
vim check.sh

#!/bin/bash
if [[ -f "arena/hero.txt" ]]; then
    echo "Hero found!"
else
    echo "Hero missing!"
fi

---

# Level 4: File Manipulation

mkdir -p backup
cp arena/*.txt backup/

---

# Level 5: The Boss Battle – Combining Basics

mkdir battlefield
touch battlefield/knight.txt battlefield/sorcerer.txt battlefield/rogue.txt

if [[ -f "battlefield/knight.txt" ]]; then
    mkdir -p archive
    mv battlefield/knight.txt archive/
fi

ls archive
ls battlefield

---

# Level 6: Argument Parsing

#!/bin/bash
if [ -z "$1" ]; then
    echo "No file provided."
else
    filename=$1
    count=$(wc -l < "$filename")
    echo "There are $count lines in $filename"
fi

