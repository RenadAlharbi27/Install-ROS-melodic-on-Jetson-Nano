## 🚀 Installing ROS Melodic on Jetson Nano  

### 🛠️ 1. Installing **ROS Noetic**  

#### 🔹 Prerequisites  
Ensure you have **Ubuntu 20.04** installed before proceeding.  

#### 📌 Steps  

1️⃣ **Add ROS GPG keys:**  
```bash
sudo apt update
sudo apt install curl
curl -sSL 'http://repo.ros2.org/repos.key' | sudo apt-key add -
```

2️⃣ **Add ROS repositories:**  
```bash
sudo sh -c 'echo "deb http://packages.ros.org/ros/ubuntu $(lsb_release -sc) main" > /etc/apt/sources.list.d/ros-latest.list'
```

3️⃣ **Update packages and install ROS Noetic:**  
```bash
sudo apt update
sudo apt install ros-noetic-desktop-full
```

4️⃣ **Set up the ROS environment:**  
```bash
echo "source /opt/ros/noetic/setup.bash" >> ~/.bashrc
source ~/.bashrc
```

5️⃣ **Install additional tools:**  
```bash
sudo apt install python3-rosdep python3-rosinstall python3-rosinstall-generator python3-wstool build-essential
```

6️⃣ **Initialize rosdep:**  
```bash
sudo rosdep init
rosdep update
```

7️⃣ **Verify the installation:**  
```bash
roscore
```

---

### 🛠️ 2. Installing **ROS2 Humble**  

#### 🔹 Prerequisites  
Ensure you have **Ubuntu 22.04** installed before proceeding.  

#### 📌 Steps  

1️⃣ **Add ROS2 GPG keys:**  
```bash
sudo apt update && sudo apt install curl -y
sudo curl -sSL 'http://repo.ros2.org/repos.key' | sudo apt-key add -
```

2️⃣ **Add ROS2 repositories:**  
```bash
sudo sh -c 'echo "deb http://packages.ros.org/ros2/ubuntu $(lsb_release -cs) main" > /etc/apt/sources.list.d/ros2-latest.list'
```

3️⃣ **Update packages and install ROS2 Humble:**  
```bash
sudo apt update
sudo apt install ros-humble-desktop
```

4️⃣ **Set up the ROS2 environment:**  
```bash
echo "source /opt/ros/humble/setup.bash" >> ~/.bashrc
source ~/.bashrc
```

5️⃣ **Verify the installation:**  
```bash
ros2 run demo_nodes_cpp talker
```

---

### 📄 3. Documenting the Installation Steps on GitHub  

#### 🛠️ **1. Create a Repository on GitHub**  
🔹 Visit [GitHub](https://github.com) and create a new repository.  
🔹 Name the repository **ros-installation-guide**.  
🔹 Choose whether to make it **public or private** based on your preference.  

#### 🛠️ **2. Upload the Files to GitHub**  

1️⃣ **Initialize the repository locally:**  
```bash
git init
git remote add origin https://github.com/YOUR_USERNAME/ros-installation-guide.git
```

2️⃣ **Create a `README.md` file and document the guide:**  
```bash
echo "# ROS Noetic and ROS2 Humble Installation Guide" > README.md
```

3️⃣ **Add and commit files:**  
```bash
git add .
git commit -m "Added installation guide"
```

4️⃣ **Push the files to GitHub:**  
```bash
git branch -M main
git push -u origin main
```

✅ **Congratulations! Your ROS installation guide is now live on GitHub.** 🚀
