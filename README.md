# Cowrie Honeypot Setup (Cybersecurity Project)
This project demonstrates the setup of Cowrie SSH Honeypot on Debian/Kali Linux using VMware.
It simulates a vulnerable server and logs attacker activity like login attempts and commands.

⚙️ Setup Steps

1. Clone repository
git clone https://github.com/cowrie/cowrie.git

2. Create virtual environment
python3 -m venv cowrie-env

3. Activate environment
source cowrie-env/bin/activate

4. Install dependencies
pip install -r requirements.txt
pip install -e .

5. Configure
cp etc/cowrie.cfg.dist etc/cowrie.cfg

6. Run Cowrie
twistd -n cowrie

🧪 Testing

ssh root@localhost -p 2222

📊 Output

login attempt [root/root] failed
login attempt [root/admin] succeeded
New connection: 127.0.0.1

🎯 Features

- Captures login attempts
- Logs attacker commands
- Simulates Linux server
- Records SSH sessions
