# TCL-Workshop
TCL WORKSHOP - Introduction to Advanced Scripting Techniques in Design and Synthesis
![workshop_banner](https://github.com/user-attachments/assets/63291de8-0f0d-44a2-a815-b8008ea9225d)


About
A comprehensive 5 day training workshop that is designed to ignite your passion for TCL and equip you with the skills needed to excel in advanced scripting techniques required in the realm of EDA.

Workshop conducted by VLSI System Design : VSD website

Outline


1. **Introduction**
The name Tcl is derived from "Tool Command Language" and is pronounced "tickle". Tcl is a radically simple open-source interpreted programming language that provides common facilities such as variables, procedures, and control structures as well as many useful features that are not found in any other major language.

For Electronic Design Automation (EDA) applications, TCL has emerged as the de facto industry standard embedded command language. TCL is the ideal option if you need to automate repetitive behavior, expand an application’s capabilities, manage many tools with a single script, or develop a unique GUI.

In this report, a TCL toolbox is created to process a verilog design. Design details and constraints were extracted and the design was synthesised using Yosys. The synthesis output and the SDC were further processed to be fed into the OpenTimer tool for Static Timing Analysis (STA). The prelayout STA results were inferred from the results file and printed to the user.

2. **Synth Toolbox**
3. <img width="1038" height="453" alt="image" src="https://github.com/user-attachments/assets/bb354fe2-d9ab-40b4-bac0-24e35d01c0c4" />
      Fig. 1 Creation of vsdsynth file amd addition of first line for shell scripting

<img width="1041" height="456" alt="image" src="https://github.com/user-attachments/assets/788dcca1-1304-4472-87d9-be6d4848399c" />
        Fig. 2 Verifying the creation of file using vim

    <img width="1041" height="456" alt="image" src="https://github.com/user-attachments/assets/b7cc6b65-ed86-453f-a70c-97c188b98be5" />
        Fig. 3 Making the file executable and checking the acccess modification

2.1 **Usage Scenario** 1

<img width="1047" height="459" alt="image" src="https://github.com/user-attachments/assets/da5025b2-3ea2-49ba-88b7-bece54808407" />
    Fig. 4 Script to check if a file is provided




