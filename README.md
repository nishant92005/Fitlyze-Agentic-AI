Youtube video link --
https://youtu.be/J5WGnPcL-F8?si=jMPjAPuGjQlmSq66

Prerequisites

Install Python 3.10+ and Git.
(Optional) Node.js + npm if you plan frontend tooling.
Quick Windows setup (PowerShell)

1. Open project folder:
cd "C:\path\to\pbl project part 3\pbl project part 3"


2. Create and activate virtualenv:
python -m venv venv
.\venv\Scripts\Activate.ps1


3.  Upgrade pip and install Python dependencies:
python -m pip install --upgrade pip
pip install -r requirements.txt

4. (Optional) install frontend deps:
npm install

5. Database & initial configuration

Check the instance folder for config templates. Create instance/config.py (or set env vars) with SECRET_KEY and DB connection (e.g., SQLALCHEMY_DATABASE_URI).
Run setup/migration scripts (try in this order):


python quick_setup.py
python migrate_db.py
python reset_db.py    # only if you want a fresh DB
python fix_db.py      # optional fixes/seeds



If your project uses Flask-Migrate, run flask db upgrade after setting FLASK_APP (see below).



Run the app:
python app.py
