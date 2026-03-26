# rs3-pt

**RuneScape 3 Ping Tool**

Bash utility that pings all known RuneScape 3 worlds (members) and returns the
**top 3 fastest (lowest latency)** servers.

---

## Usage

### 1. Clone the repository

```bash
git clone https://github.com/your-username/rs3-pt.git
cd rs3-pt
```

### 2. Make the script executable

```bash
chmod +x rs3-pt.sh
```

### 3. Run it

```bash
./rs3-pt.sh
```

---

## How it works

* The script pings each RuneScape world (`worldX.runescape.com`)
* Extracts the latency (`time=XX ms`)
* Sorts results from lowest to highest
* Displays the **top 3 fastest worlds**

---

## Configuration

You can tweak performance and accuracy:

* **Increase accuracy (more stable results):**

  ```bash
  ping -c 3
  ```

* **Reduce timeout (faster scan):**

  ```bash
  ping -W 1
  ```

* **Enable parallel scanning (recommended):**
  Uses `xargs -P` to ping multiple worlds simultaneously

## License

MIT License.
