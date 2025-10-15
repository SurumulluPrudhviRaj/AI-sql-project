# AI SQL Query Assistant



Here’s a **complete local installation and run guide** that covers **both Mac/Linux and Windows**, in plain text format.
You can directly paste this into your GitHub `README.md` file or keep it for internal documentation.

---

# Local Installation and Run Guide (Mac/Linux and Windows)

## 1. Install Python (if not already installed)

Ensure Python 3.9 or higher is installed.

Check version:

```bash
python3 --version
```

If not installed, download from:
[https://www.python.org/downloads/](https://www.python.org/downloads/)

For Windows users, make sure to select **“Add Python to PATH”** during installation.

---

## 2. Create a Project Folder

```bash
mkdir ai_sql_app
cd ai_sql_app
```

Place your `.py` file (for example, `ai_sql_chat.py`) inside this folder.

---

## 3. Create a Virtual Environment (Recommended)

This step isolates your dependencies from the global Python environment.

### Mac/Linux

```bash
python3 -m venv venv
source venv/bin/activate
```

### Windows

```bash
python -m venv venv
venv\Scripts\activate
```

After activation, your terminal prompt should show `(venv)` at the beginning.

---

## 4. Install Required Python Packages

```bash
pip install --upgrade pip
pip install streamlit mysql-connector-python openai pandas packaging
```

---

## 5. Configure MySQL

Ensure MySQL is installed and running locally.

Default connection in the Python file:

```python
MYSQL_HOST = "localhost"
MYSQL_USER = "root"
MYSQL_PASS = "welcome@75f"
DEFAULT_DB = "ai_sql_demo"
```

Check connection:

```bash
mysql -u root -p
```

If the database does not exist:

```sql
CREATE DATABASE ai_sql_demo;
```

Load or create your required tables and sample data in this database.

---

## 6. Set Your OpenAI API Key (Optional but Recommended)

Create a `.streamlit` folder and `secrets.toml` file to store your key securely.

### Mac/Linux

```bash
mkdir -p .streamlit
nano .streamlit/secrets.toml
```

### Windows

```bash
mkdir .streamlit
notepad .streamlit\secrets.toml
```

Paste the following in the file:

```toml
OPENAI_API_KEY = "sk-xxxxx"
```

Then in your Python file, replace the hardcoded key with:

```python
OPENAI_API_KEY = st.secrets["OPENAI_API_KEY"]
```

---

## 7. Run the Streamlit App

### Mac/Linux

```bash
python3 -m streamlit run ai_sql_chat.py
```

or

```bash
streamlit run ai_sql_chat.py
```

### Windows

```bash
python -m streamlit run ai_sql_chat.py
```

or

```bash
streamlit run ai_sql_chat.py
```

After running, you’ll see a message similar to:

```
You can now view your Streamlit app in your browser.

Local URL: http://localhost:8501
```

Open this URL in your browser.

---

## 8. Keep the App Running in the Background (Optional)

### Mac/Linux

```bash
nohup streamlit run ai_sql_chat.py &
```

### Windows

Open a new terminal window and run the app separately. You can also use `start`:

```bash
start streamlit run ai_sql_chat.py
```

---

## 9. Stop the App

Press `CTRL + C` in the terminal to stop the app on both Mac/Linux and Windows.

---

## Summary Table

| Step | Action                                                   |
| ---- | -------------------------------------------------------- |
| 1    | Install Python                                           |
| 2    | Create project folder                                    |
| 3    | Create and activate virtual environment                  |
| 4    | Install dependencies                                     |
| 5    | Configure and verify MySQL                               |
| 6    | (Optional) Secure API key in secrets file                |
| 7    | Run the app using Streamlit                              |
| 8    | Keep it running in background if required                |
| 9    | Access at [http://localhost:8501](http://localhost:8501) |

---

## Quick Commands

### Mac/Linux

```bash
pip install mysql-connector-python openai streamlit
python3 -m streamlit run ai_sql_chat.py
```

### Windows

```bash
pip install mysql-connector-python openai streamlit
python -m streamlit run ai_sql_chat.py
```

Video link : 
https://go.screenpal.com/watch/cT6olinbZD3

<img width="1440" height="900" alt="Screenshot 2025-10-15 at 5 26 49 PM" src="https://github.com/user-attachments/assets/85557c38-298c-4abb-94f8-2d58df093704" />

<img width="1440" height="900" alt="Screenshot 2025-10-15 at 5 27 08 PM" src="https://github.com/user-attachments/assets/ca1e25c7-4a38-43ab-8c26-aef45e6556a0" />
<img width="1440" height="900" alt="Screenshot 2025-10-15 at 5 27 17 PM" src="https://github.com/user-attachments/assets/06ef5f4a-cc8a-49dd-9295-01b2669ed9f1" />
<img width="1440" height="900" alt="Screenshot 2025-10-15 at 5 27 17 PM" src="https://github.com/user-attachments/assets/2fb6162f-5107-4807-b2d9-ad59429f4281" />




