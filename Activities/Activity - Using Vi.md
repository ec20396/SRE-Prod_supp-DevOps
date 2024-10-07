# Activity: Using Vi

**Description:**
Complete the following activities using a Linux interface, using skills covered in Linux Lesson 8. This activity involves editing text files with `vi`, including tasks like running word counts, replacing text, and editing lines.

**Key Features:**
- Editing files with `vi`.
- Running word counts and replacing text.
- Practicing `vi` navigation and editing commands.

## Part 1: Avengers

Practice the `vi` commands presented in the Lesson 8 slides before completing these exercises.

1. Open a new file named `avengers` in your home directory in your editor and paste in the following text:
    ```
    Six stones, three teams, one shot. Five years ago, we lost. All of us. We lost friends. We lost family. We lost a part of ourselves. Today, we have a chance to take it all back. You know your teams. You know your missions. Get the stones. Get them back. One round trip each. No mistakes. No do-overs. Most of us are going somewhere we know, that doesn’t mean we should know what to expect. Be careful. Look out for each other. This is the fight of our lives, and we’re gonna win. Whatever it takes. Good luck.
    ```

    ```sh
    vi avengers
    ```
    Press `i` to enter insert mode, paste the text, then press `Esc` to exit insert mode.

2. Exit and save the file.
    ```sh
    :wq
    ```

3. Run a word count on the file.
    ```sh
    :%!wc -w
    ```

4. Edit the file to add a blank line and type in "word count" followed by the value you just got.
    ```sh
    :%s/^/word count X\n/  # Replace X with the actual word count
    ```

5. Now use search and replace within the editor to replace every instance of the word `the` with `THE`. Ensure that you only catch the word `the` and not words that contain the letters `the` (like them).
    ```sh
    :%s/\bthe\b/THE/g
    ```

6. Copy the first line of the file and paste it after your word count entry at the bottom of the file.
    ```sh
    gg"zyyGop
    ```

7. Delete the first line of the file.
    ```sh
    ggdd
    ```

8. Undo that deletion.
    ```sh
    u
    ```

9. Insert at the top of the file the text "Captain America – Endgame" followed by an empty line.
    ```sh
    ggO  # Uppercase 'O' to open a new line above
    Captain America – Endgame
    ```

10. Save the changes and exit the editor.
    ```sh
    :wq
    ```

11. Find out the number of lines in the file now.
    ```sh
    :%!wc -l
    ```

12. Write the number of lines into the file on one line above the word count with the text "line count" plus the value.
    ```sh
    ggO  # Uppercase 'O' to open a new line above
    line count X  # Replace X with the actual line count
    ```

13. Delete "Good luck" wherever it occurs in the file.
    ```sh
    :%s/Good luck//g
    ```

14. Save and exit the file.
    ```sh
    :wq
    ```

15. Submit a file named `avengers.<yourname>.txt` that includes the contents of this file.

## Part 2: Log Files

Run the `fixGenerator.sh` script again from your home directory using the following commands:

```sh
cd ~
./fixGenerator.sh &
