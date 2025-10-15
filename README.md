# LEARNING_PCB

# 🚀 KiCad 7 Full Installation Script for Ubuntu 24.04 / 22.04
# -------------------------------------------------------------
# Step 1: Update system and fix any broken dependencies
sudo apt update && sudo apt upgrade -y
sudo apt --fix-broken install -y
sudo apt install -f -y

# Step 2: Remove any old or partial KiCad installations (optional but recommended)
sudo apt remove --purge kicad* -y
sudo apt autoremove -y
sudo apt clean

# Step 3: Add official KiCad PPA (stable version)
sudo add-apt-repository --yes ppa:kicad/kicad-7.0-releases
sudo apt update

# Step 4: Install KiCad core software
sudo apt install kicad -y

# Step 5: Install official KiCad libraries (symbols, footprints, 3D models, templates)
sudo apt install kicad-symbols kicad-footprints kicad-packages3d kicad-templates -y

# Step 6: (Optional) Verify installation paths
echo "Checking KiCad library paths..."
ls /usr/share/kicad || ls /snap/kicad/current/share/kicad

# Step 7: Launch KiCad to verify installation
kicad &

# -------------------------------------------------------------
# ✅ DONE: KiCad + All Libraries Installed Successfully!
# You can now start your first project using:
#   KiCad → File → New Project → "My_First_PCB"
# -------------------------------------------------------------
