# Instructions to Generate an SSH Key and Add it to Your GitHub Account

1. **Open your terminal**  
   (Command Prompt, PowerShell, or Git Bash).

2. **Generate a new SSH key**  
   Run the following command:  
   ```bash
   ssh-keygen -t rsa -b 4096 -C "your_email@example.com"
   ```  
   *(Replace `your_email@example.com` with the email address associated with your GitHub account.)*

3. **Specify the file location**  
   When prompted to "Enter a file in which to save the key," press **Enter** to accept the default file location.

4. **Set a passphrase**  
   You will then be prompted to enter a passphrase. You can either enter a secure passphrase or leave it empty for no passphrase.

5. **Add the SSH key to the ssh-agent**  
   Run the following commands:  
   ```bash
   eval "$(ssh-agent -s)"
   ssh-add ~/.ssh/id_rsa
   ```

6. **Copy the SSH key to your clipboard**  
   Use the following command:  
   ```bash
   clip < ~/.ssh/id_rsa.pub
   ```  
   *(Use `pbcopy < ~/.ssh/id_rsa.pub` on macOS or `xclip -sel clip < ~/.ssh/id_rsa.pub` on Linux.)*

7. **Go to your GitHub account**  
   Navigate to **Settings**.

8. **Access SSH and GPG keys**  
   In the left sidebar, click on **SSH and GPG keys**.

9. **Add a new SSH key**  
   Click the **New SSH key** button.

10. **Title your key**  
    In the "Title" field, add a descriptive label for the new key.

11. **Paste your key**  
    Paste your key into the "Key" field.

12. **Save the key**  
    Click **Add SSH key** to save.

Congratulations! You have successfully generated an SSH key and added it to your GitHub account!  