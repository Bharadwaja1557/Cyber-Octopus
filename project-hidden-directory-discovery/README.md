# INSTRUCTIONS

1. Copy both files in this project into a single folder.

2. Open a terminal **inside that folder**.

3. Run the Python script in Kali Linux:

    ```bash
    python3 hidden-directories.py
    ```

4. When prompted, enter:

    - The target **URL**
    - The **common directories wordlist file** (e.g., `common.txt`)

5. The script will compare the entries in the wordlist with the target website and list all directories that exist on the server.

6. On Kali Linux, a common wordlist file (`common.txt`) is usually located at:

    ```
    /usr/share/dirb/wordlists/
    ```

7. After getting the output, you can explore sub‑directories of the discovered paths.

8. Example workflow:

    - Suppose the script finds:  
      `directory1`, `directory2`, `directory3` for the website `abc.com`
    - To explore deeper, run the script again and enter:  
      `abc.com/directory1`  
      instead of just `abc.com`

    This allows you to recursively inspect further sub‑paths on the website.
