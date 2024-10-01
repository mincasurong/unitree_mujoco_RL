\documentclass{article}
\usepackage{hyperref}

\begin{document}

\title{Unitree Mujoco Reinforcement Learning Integration}
\author{mincasurong}
\date{\today}
\maketitle

\section*{Overview}

This repository builds upon the original Unitree MuJoCo repository, adding integration with reinforcement learning (RL) capabilities. The goal is to simulate and enhance the behaviors of Unitree quadruped robots using advanced machine learning algorithms within the MuJoCo environment.

Original repository link: 
\begin{itemize}
    \item \href{https://github.com/unitreerobotics/unitree_mujoco}{Unitree MuJoCo Original Repository}
\end{itemize}

Forked and enhanced repository: 
\begin{itemize}
    \item \href{https://github.com/mincasurong/unitree_mujoco_RL/tree/main}{mincasurong's Unitree MuJoCo RL Integration}
\end{itemize}

\section*{Features Added}
\begin{itemize}
    \item \textbf{Reinforcement Learning (RL) Environment}: Integrated support for reinforcement learning, enabling the use of RL agents to train and optimize the behavior of Unitree robots.
    \item \textbf{ROS2 Communication}: Enhanced interaction between the MuJoCo simulation and ROS2, facilitating real-time control and state feedback.
    \item \textbf{New Motion Capabilities}: Included support for various robotic behaviors, such as stand up, balance, velocity move, and trajectory following, simulated in the MuJoCo environment.
    \item \textbf{Sport Mode Integration}: Added the functionality to use the sport mode commands, enabling dynamic movement control in the MuJoCo simulation.
\end{itemize}

\section*{Requirements}

\begin{itemize}
    \item \textbf{MuJoCo}: You need to have MuJoCo installed and properly configured. For installation instructions, refer to the \href{https://github.com/unitreerobotics/unitree_mujoco}{original Unitree MuJoCo repository}.
    \item \textbf{Python 3.x}: Python is required for running the simulation scripts and reinforcement learning integration.
    \item \textbf{ROS2 Humble or Rolling}: For real-time robot control, ROS2 Humble or Rolling is recommended.
    \item \textbf{Unitree SDK}: Ensure that the Unitree SDK dependencies are installed.
\end{itemize}

\section*{Installation}

\begin{enumerate}
    \item \textbf{Clone the repository:}
    \begin{verbatim}
    git clone https://github.com/mincasurong/unitree_mujoco_RL.git
    cd unitree_mujoco_RL
    \end{verbatim}

    \item \textbf{Install Dependencies:}
    Ensure all the necessary Python libraries are installed. Run the following command:
    \begin{verbatim}
    pip install -r requirements.txt
    \end{verbatim}

    \item \textbf{MuJoCo Setup:}
    Follow the original \href{https://github.com/unitreerobotics/unitree_mujoco}{Unitree MuJoCo repository} instructions for configuring MuJoCo.

    \item \textbf{Set Environment Variables:}
    Configure the environment variables for MuJoCo and ROS2 if necessary:
    \begin{verbatim}
    export MUJOCO_PY_MJKEY_PATH=~/.mujoco/mjkey.txt
    export MUJOCO_PY_MUJOCO_PATH=~/.mujoco/mujoco210
    \end{verbatim}
\end{enumerate}

\section*{Usage}

\begin{itemize}
    \item \textbf{Run the Simulation:}
    The MuJoCo simulation can be started by running the \texttt{unitree\_mujoco.py} script:
    \begin{verbatim}
    python unitree_mujoco.py
    \end{verbatim}

    \item \textbf{Test Sport Mode Commands:}
    To test the sport mode capabilities, run the \texttt{sportmode\_test.py} script:
    \begin{verbatim}
    python sportmode_test.py
    \end{verbatim}

    \item \textbf{Integrate Reinforcement Learning:}
    RL can be integrated using any supported RL library, such as Stable-Baselines3 or PyTorch. Train the model to control the robot's trajectory:
    \begin{verbatim}
    python train_rl_agent.py
    \end{verbatim}
\end{itemize}

\section*{Directory Structure}

\begin{itemize}
    \item \textbf{unitree\_mujoco.py}: The main MuJoCo simulation script for the Unitree quadruped.
    \item \textbf{sportmode\_test.py}: A script for testing sport mode functionality.
    \item \textbf{config.py}: Configuration file for setting simulation parameters.
    \item \textbf{rl/}: Contains scripts and modules for reinforcement learning integration.
    \item \textbf{README.md}: Documentation for the project.
\end{itemize}

\section*{Configuration}

The \texttt{config.py} file can be edited to adjust the following:
\begin{itemize}
    \item \texttt{ROBOT\_SCENE}: Path to the MuJoCo scene XML file.
    \item \texttt{ENABLE\_ELASTIC\_BAND}: Boolean to enable/disable elastic band control.
    \item \texttt{USE\_JOYSTICK}: Set to True if a joystick is being used.
    \item \texttt{SIMULATE\_DT}: Time step for simulation.
    \item \texttt{VIEWER\_DT}: Time step for the viewer.
\end{itemize}

\section*{Future Work}

\begin{itemize}
    \item \textbf{Advanced Reinforcement Learning Algorithms}: Integrate more sophisticated RL algorithms to improve the adaptability of the robot.
    \item \textbf{Gazebo and ROS2 Support}: Plan to add support for running the simulation in Gazebo for a more realistic testing environment.
    \item \textbf{Multiple Agent Collaboration}: Extend the simulation to include multiple robots collaborating.
\end{itemize}

\section*{Contributing}

Contributions are welcome! Please open an issue or a pull request if you would like to add features or fix bugs.

\section*{License}

This project is licensed under the \textbf{MIT License}. For more information, please refer to the \texttt{LICENSE} file.

\section*{Acknowledgements}

The original repository is developed and maintained by \textbf{Unitree Robotics}. This repository extends the capabilities of their software to include advanced RL functionalities.

\end{document}
