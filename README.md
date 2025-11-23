### 🧪 Lab Instructions — 3.2 Searching and Extracting Data from Files

---

>💬 **Tip:** Paste this study guide into ChatGPT and ask for **more instructions** by specifying:  
>- “Provide step-by-step lab instructions for this objective.”  
>- “Include which Linux distro to use (Debian/Ubuntu or RHEL/Fedora).”  
>- “Show examples of installing, verifying, and managing desktop and server applications.”  
>- “Include minimal command-line practice for package management and development tools.”  
>- “Focus only on what is most important for passing the LPI Linux Essentials exam.”  

>This will prompt ChatGPT to give **practical, exam-focused lab steps** for each section.

---

**Objective:** Practice searching, filtering, and extracting data from files in your home directory.  

**Steps:**  

1. 📁 **Create a test directory and files**  
   - `mkdir ~/search_lab`  
   - `cd ~/search_lab`  
   - `echo -e "apple\nbanana\ncherry\nApple\napricot" > fruits.txt`  
   - `echo -e "dog\ncat\nmouse\ndog\nparrot" > animals.txt`  

2. 🕵️ **Search with `grep`**  
   - `grep "apple" fruits.txt` → Case-sensitive search  
   - `grep -i "apple" fruits.txt` → Case-insensitive search  
   - `grep -r "dog" ./` → Search recursively in directory  

3. 📖 **View files with `less`**  
   - `less fruits.txt` → Scroll with arrows, `q` to quit  

4. 📜 **Display portions of files with `cat`, `head`, `tail`**  
   - `cat fruits.txt` → Show all lines  
   - `head -n 3 animals.txt` → First 3 lines  
   - `tail -n 2 animals.txt` → Last 2 lines  
   - `tail -f animals.txt` → Follow file as it grows  

5. 🔢 **Sort file contents with `sort`**  
   - `sort fruits.txt` → Alphabetical order  
   - `sort -r fruits.txt` → Reverse order  

6. ✂️ **Extract fields with `cut`**  
   - Create a colon-delimited file: `echo -e "user1:1000:1000\nuser2:1001:1001" > users.txt`  
   - `cut -d ":" -f1 users.txt` → Extract first field (username)  

7. 🧮 **Count with `wc`**  
   - `wc fruits.txt` → Lines, words, characters  
   - `wc -l animals.txt` → Only line count  

8. 🔄 **Combine commands with pipes**  
   - `cat fruits.txt | grep "a" | sort` → Filter lines containing "a" and sort  

9. ⬇️ **Redirect output to a file**  
   - `grep "dog" animals.txt > results.txt` → Save search results  

**⚡ Tips:**  
- Practice using regex symbols with `grep`:  
  - `.` → any single character  
  - `[ ]` → any character in brackets  
  - `*` → zero or more of preceding character  
  - `?` → zero or one of preceding character  
- Experiment combining `grep`, `sort`, `cut`, `wc` with pipes and redirection
