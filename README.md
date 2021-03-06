<!-- PROJECT SHIELDS -->
<!--
*** I'm using markdown "reference style" links for readability.
*** Reference links are enclosed in brackets [ ] instead of parentheses ( ).
*** See the bottom of this document for the declaration of the reference variables
*** for contributors-url, forks-url, etc. This is an optional, concise syntax you may use.
*** https://www.markdownguide.org/basic-syntax/#reference-style-links
-->
[![MIT License][license-shield]][license-url]
[![LinkedIn][linkedin-shield]][linkedin-url]



<!-- PROJECT LOGO -->
<br />
<p align="center">
  
  <h1 align='center' class="header-title" style="font-family:'Raleway';"><a href="http://rail.eecs.berkeley.edu/deeprlcourse/">CS285</a></h1>
  
  <p align="center">
    Tensorflow Version of homework assignments of Deep Reinforcement Learning Course <br/>Presented by Dr. Sergey Levin at University of California, Berkeley 
    <br />
    <br />
    <a href="https://github.com/erfanMhi/Deep-Reinforcement-Learning-CS285-Pytorch/issues">Report Bug</a>
  </p>
</p>



<!-- TABLE OF CONTENTS -->
## Table of Contents

* [About the Project](#about-the-project)
* [Getting Started](#getting-started)
* [Usage](#usage)
* [Roadmap](#roadmap)
* [License](#license)
* [Contact](#contact)



<!-- ABOUT THE PROJECT -->
## About The Project

In this project, we aim to solve the assignments of CS285 course.

<!-- GETTING STARTED -->
## Getting Started

Unfortunately, the current version of this repository is not compatible with the latest versions of libraries, such as Tensorflow and Mojocu-py. As a result, installing the proper versions of these libraries, which can enable you to contribute to this repo, could be a hard challenge. However, since I have been faced with this problem before, I designed a certain number of steps that you can take to install the right versions of these libraries. 



1. Create a new Conda environment based on Python 3.5 and install matplotlib, ipython, and pytorch. Then, activate it.
```sh
conda create -n cs285_env python=3.5 matplotlib ipython pytorch=1.5.0
source activate cs285_env
```
2. Clone this repository
2. Install mujoco-py
    1. Get mujoco license key file from <a href="https://www.roboti.us/license.html">its website</a>
    2. Create a .mujoco folder in the home directory and copy the given mjpro150 directory and your license key into it
      ```sh
      mkdir ~/.mujoco/
      cd <location_of_your_license_key>
      cp mjkey.txt ~/.mujoco/
      cd <this_repo>/mujoco
      cp -r mjpro150 ~/.mujoco/
      ```
    3. Add the following line to bottom of your .bashrc file: 
      ```sh
      export LD_LIBRARY_PATH=~/.mujoco/mjpro150/bin/
      ```
    4. Build and install mujoco-py 1.50.1.1. It can be downloaded from <a href="https://github.com/openai/mujoco-py/archive/1.50.1.1.tar.gz">this link</a>.
      ```sh
      tar -xzf mujoco-py-1.50.1.1.tar.gz 
      cd mujoco-py-1.50.1.1
      python setup.py install
      ```
3. Install rest of the libraries given in contribution_requirements.txt file using pip
 ```sh
 pip install --user --requirement contribution_requirements.txt
 ```
4. At last, it should be considered that before executing scripts of each homework folder (e.g., hw1), you should allow your code to be able to see 'cs285' by executing the following lines:
 ```sh
 cd <path_to_hw>
 pip install -e .
 ```


<!-- USAGE EXAMPLES -->
## Usage

The instructions for execution of all of these assignments are given in the Readme documents that are located in each of the homework directories.

<!-- ROADMAP -->
## Roadmap

See the [open issues](https://github.com/erfanMhi/Deep-Reinforcement-Learning-CS285-Pytorch/issues/) for a list of known issues.


<!-- LICENSE -->
## License

Distributed under the MIT License. See `LICENSE` file for more information.


<!-- CONTACT -->
## Contact

Erfan Miahi - [@erfan_mhi](https://twitter.com/erfan_mhi) - miahi@ualberta.com

Project Link: [https://github.com/erfanMhi/Deep-Reinforcement-Learning-CS285-Pytorch](https://github.com/erfanMhi/Deep-Reinforcement-Learning-CS285-Pytorch)



<!-- MARKDOWN LINKS & IMAGES -->
<!-- https://www.markdownguide.org/basic-syntax/#reference-style-links -->
[license-shield]: https://img.shields.io/github/license/othneildrew/Best-README-Template.svg?style=flat-square
[license-url]: https://github.com/erfanMhi/Deep-Reinforcement-Learning-CS285-Pytorch/blob/master/LICENSE
[linkedin-shield]: https://img.shields.io/badge/-LinkedIn-black.svg?style=flat-square&logo=linkedin&colorB=555
[linkedin-url]: https://www.linkedin.com/in/erfan-miahi-8637a1130/
