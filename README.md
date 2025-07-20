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
 <img width="1038" height="453" alt="image" src="https://github.com/user-attachments/assets/bb354fe2-d9ab-40b4-bac0-24e35d01c0c4" />
      Fig. 1 Creation of vsdsynth file amd addition of first line for shell scripting

<img width="1041" height="456" alt="image" src="https://github.com/user-attachments/assets/788dcca1-1304-4472-87d9-be6d4848399c" />
        Fig. 2 Verifying the creation of file using vim

    <img width="1041" height="456" alt="image" src="https://github.com/user-attachments/assets/b7cc6b65-ed86-453f-a70c-97c188b98be5" />
        Fig. 3 Making the file executable and checking the acccess modification

2.1 **Usage Scenario** 1

<img width="1047" height="459" alt="image" src="https://github.com/user-attachments/assets/da5025b2-3ea2-49ba-88b7-bece54808407" />
    Fig. 4 Script to check if a file is provided

    <img width="1044" height="453" alt="image" src="https://github.com/user-attachments/assets/88181ca4-428b-4574-a05d-9c035622d11d" />
          Fig. 5 Checking both use cases - file not given and file given

2.2 **Usage Scenario 2 and 3**

<img width="1035" height="489" alt="image" src="https://github.com/user-attachments/assets/5815f5a4-8283-4f97-8c79-3ec7459209e0" />
      Fig. 6 Scripts for scenario 2 - user invoking help menu - and scenario 3 - user providing a CSV file that does not exits
<img width="1155" height="489" alt="image" src="https://github.com/user-attachments/assets/d9b2b671-0289-4fa7-9b65-2e06d185b526" />
      Fig. 7 Verification of scenarios 2 and 3

**3 ** Variable Creation**
<img width="1029" height="492" alt="image" src="https://github.com/user-attachments/assets/9c69344b-c754-456a-91ea-c5282040e205" />
            Fig. 8 Creation of .tcl script

<img width="1032" height="495" alt="image" src="https://github.com/user-attachments/assets/a54f9ce1-adf4-406a-bba1-fe277647c795" />

            Fig. 9 Verifyinf creation of file using vim

<img width="1152" height="693" alt="image" src="https://github.com/user-attachments/assets/bb3a9dbd-c317-4175-8422-a1a5a7de371a" />
            Fig. 10 Invoking the tcl script within the shell script

<img width="938" height="512" alt="image" src="https://github.com/user-attachments/assets/b59f2c36-887c-4e11-a6a6-4952da6946f4" />
            Fig. 11 Sample CSV file containing the design details required by the script

<img width="888" height="597" alt="image" src="https://github.com/user-attachments/assets/b16fcf71-5552-4182-9601-9edacc578174" />
            Fig. 12 TCL file containing the logic of extracting CSV data and auto-creating variables

<img width="891" height="597" alt="image" src="https://github.com/user-attachments/assets/05a567c8-5dce-4977-a42d-e608d002db0d" />
            Fig. 13 Verification of variable creation and it's contents

<img width="885" height="597" alt="image" src="https://github.com/user-attachments/assets/ec32929b-132d-46f2-a224-30eac6eeedb7" />
            Fig. 14 Script to verify variable name and contents

<img width="888" height="600" alt="image" src="https://github.com/user-attachments/assets/c26f4c8f-c456-41cb-884f-a08a5727a982" />
            Fig. 15 Verification of variable name and contents

<img width="888" height="798" alt="image" src="https://github.com/user-attachments/assets/c6378b57-0657-48bf-aed0-6fcb75ff8950" />
            Fig. 16 Script to check the correctness of details provided in the CSV file

<img width="891" height="792" alt="image" src="https://github.com/user-attachments/assets/fa1ef071-d3ca-473b-8eb6-0c44637f8a63" />
            Fig. 17 Verification of details - if a wrong path was provided, the script would have thrown an error and exited right away

**4. Processing constraints from the CSV File**

<img width="1063" height="490" alt="image" src="https://github.com/user-attachments/assets/f9f34790-cdea-4a23-88e2-cdc31f97cb0f" />
      Fig. 18 Script to create the CSV file as a matrix, convert into an array and identify number of rows and columns

<img width="632" height="122" alt="image" src="https://github.com/user-attachments/assets/67037a31-92e3-494e-85c8-f74407b377eb" />
      Fig. 19 Verification of matrix creation, array creation and count of R and C

<img width="1059" height="488" alt="image" src="https://github.com/user-attachments/assets/6adc5745-45c5-4112-a895-33f481175992" />
      Fig. 20 Script to extract the positions of port details' start point

<img width="656" height="166" alt="image" src="https://github.com/user-attachments/assets/c984c308-1f53-4e77-986b-cd3e3b3fbcb5" />
      Fig. 21 Verification of the indices

<img width="1845" height="588" alt="image" src="https://github.com/user-attachments/assets/7eaa0cf9-048e-4d9d-819f-d5c9307249d6" />
      Fig. 22 Snip of the constraints CSV file to cross-check

<img width="1796" height="492" alt="image" src="https://github.com/user-attachments/assets/fe4583e1-d3f4-4763-a2b3-8ecda2a2c5ac" />
      Fig. 23 Script to identify start of a particular parameter - clocks' early rise delay in this case

<img width="1022" height="258" alt="image" src="https://github.com/user-attachments/assets/65202a24-cc79-42cc-affe-1017c6c1ea1f" />
      Fig. 24 Verification of the index

<img width="1794" height="491" alt="image" src="https://github.com/user-attachments/assets/359febf1-e2e1-42ce-a7a6-65cb86334239" />
      Fig. 25 Script to idetify multiple parameters

<img width="904" height="229" alt="image" src="https://github.com/user-attachments/assets/8ecda0a6-1a4b-4242-9f99-9902d5a70b36" />
      Fig. 26 Verification of the above case

**5. Processing clock constraints**

<img width="1796" height="723" alt="image" src="https://github.com/user-attachments/assets/961c6c00-02a8-411b-a0de-8a91bf9bf27e" />
      Fig. 27 Script to extract clock constraints in the format that yosys accepts

<img width="878" height="490" alt="image" src="https://github.com/user-attachments/assets/2e873194-bd83-45f1-a1ac-bc15afac1c99" />
      Fig. 28 Verification of working of the code


<img width="1181" height="297" alt="image" src="https://github.com/user-attachments/assets/5a918ea9-38e0-49c0-8756-7bf1990a7f08" />
      Fig. 29 Only the create clock of Fig. 27 was tested and the above output was verified

<img width="1186" height="426" alt="image" src="https://github.com/user-attachments/assets/03f6fdc0-f257-4bcd-83d7-445249ba4e7b" />
      Fig. 30 Successful extration of all clock related constraints

**6. Processing input constraints**

<img width="1850" height="978" alt="image" src="https://github.com/user-attachments/assets/d9250d97-d51c-4b34-9530-c6eb1151eb69" />
      Fig. 31 Script to extract 1. Input latency and slew; 2. Bussed and bit ports using pattern searching


<img width="1852" height="975" alt="image" src="https://github.com/user-attachments/assets/6961712d-c746-41b2-a84d-631738c514c4" />
      Fig. 32 Continuation of Fig. 31 - appending the port name with * if bussed and dumping values into SDC file

<img width="1624" height="850" alt="image" src="https://github.com/user-attachments/assets/59eeea47-4a6b-4258-b4b8-1b083f153c13" />
      Fig. 33 Successful identification and modification of bussed ports

<img width="1854" height="976" alt="image" src="https://github.com/user-attachments/assets/1769a5ad-ea9b-4742-b538-50070356c036" />
      Fig. 34 Path to access sdc file

**7. Processing output constraints**


<img width="1863" height="912" alt="image" src="https://github.com/user-attachments/assets/d47faf77-da12-4207-b04c-2ee024c5cb46" />
      Fig. 35 Script to extract output constraints

<img width="1854" height="978" alt="image" src="https://github.com/user-attachments/assets/fd6224b0-522a-4f20-941b-12e19fc453a0" />
      Fig. 36 Successful extraction of clock, input and output constraints in the SDC format

<img width="1852" height="976" alt="image" src="https://github.com/user-attachments/assets/caf7c7c8-3220-4253-811b-c2730c084d5d" />
      Fig. 37 Illustration of bussed and unbussed output ports

<img width="1854" height="978" alt="image" src="https://github.com/user-attachments/assets/8ff80b28-cda6-4600-bd5a-f20a6004dc2d" />
      Fig. 38 Output constraints in SDC format - can be viewed using commands in Fig. 34

**8. Yosys**
      Yosys is the first full-featured open source software for Verilog HDL synthesis. It supports most of Verilog-2005 and is well tested with real-world designs from the ASIC and FPGA world.


**9. Hierarchy Check**

<img width="1434" height="959" alt="image" src="https://github.com/user-attachments/assets/4d81a301-1aa9-4d4a-a718-74e9554d3ad3" />
      Fig. 39 Script to run hierarchy check - check if all modules referenced within the top module is valid


<img width="1438" height="955" alt="image" src="https://github.com/user-attachments/assets/f9e29192-dac0-46db-9149-33b20268801c" />
      Fig. 40 Successful verification that modules are present

<img width="1440" height="961" alt="image" src="https://github.com/user-attachments/assets/e001bc3a-9ed9-4fa3-a5aa-d8fe233b544c" />
      Fig. 40 (i) - Hierarchy check log file.

<img width="1438" height="958" alt="image" src="https://github.com/user-attachments/assets/27fec8ad-d737-44dd-bd6a-3fc65f21fd0b" />
      Fig. 40 (ii) - Hierarchy check PASS - verified from log

<img width="1435" height="962" alt="image" src="https://github.com/user-attachments/assets/05681cbc-e28a-422a-a5aa-d42da6c4a13f" />
      Fig. 41 Module name modified to check the error handling

<img width="1439" height="962" alt="image" src="https://github.com/user-attachments/assets/8449a5cb-84dd-4068-aaae-67d9340f70bf" />
      Fig. 42 Error flag set to 1, thus the check works

<img width="1439" height="958" alt="image" src="https://github.com/user-attachments/assets/b3efcd1a-905d-4073-8f17-8226fc1baaee" />
      Fig. 43 Error captured in the log file


      <img width="1437" height="963" alt="image" src="https://github.com/user-attachments/assets/7198a1c8-b142-449b-94c8-c9bc866ce1d5" />
            Fig. 44 Debugging statements printed to identify and modify hierarchy faults

<img width="1440" height="958" alt="image" src="https://github.com/user-attachments/assets/2fb6bc5d-c7ce-4d8f-8104-1733050cd57b" />
            Fig. 45 Heirarchy PASS after rectifying the error


**10. Synthesis using Yosy**

<img width="1680" height="846" alt="image" src="https://github.com/user-attachments/assets/36c5c622-4ff8-4aeb-a11e-380f73b8f0e8" />

Fig. 46 Script to run synthesis using yosys - which creates a script to feed to the yosys tool

<img width="1680" height="851" alt="image" src="https://github.com/user-attachments/assets/ecce263b-08b3-45aa-b284-c77c6c7ab588" />

Fig. 47 Successful creation of yosys script

<img width="1678" height="850" alt="image" src="https://github.com/user-attachments/assets/fd8fe76d-257f-4d61-aa6e-2c009433d8e2" />

Fig. 48 Preview of the yosys script

<img width="1678" height="850" alt="image" src="https://github.com/user-attachments/assets/d22ff37a-7cbb-4e09-bd41-a954caffc414" />

Fig. 49 Script to invoke yosys tool with our design and catch errors

<img width="1681" height="854" alt="image" src="https://github.com/user-attachments/assets/50e3243c-6f1a-4636-8d21-d3a938ac929e" />

Fig. 50 Successful synthesis

<img width="1680" height="850" alt="image" src="https://github.com/user-attachments/assets/4ab14219-b359-4d43-a87d-07245a058eb9" />

Fig. 51 Snip of the synthesis log


**11. Procs**
Procedures are nothing but code blocks with series of commands that provide a specific reusable functionality. It is used to avoid same code being repeated in multiple locations. Procedures are equivalent to the functions used in many programming languages and are made available in Tcl with the help of proc command.

<img width="1461" height="709" alt="image" src="https://github.com/user-attachments/assets/4f97fb40-f31b-4767-b85c-5b3aff6cc1da" />
Fig. 52 Proc to set library files for STA

<img width="1855" height="979" alt="image" src="https://github.com/user-attachments/assets/76465e5f-7617-4780-988e-718e1d22ca80" />

Fig. 53 (i) Proc to modify SDC constraints to suit Opentimer requirements

<img width="1855" height="979" alt="image" src="https://github.com/user-attachments/assets/7e7a3fe2-79de-40a4-a293-dfc95f4bc684" />

Fig. 53 (ii) contd.

<img width="1854" height="975" alt="image" src="https://github.com/user-attachments/assets/5bdd7f1b-7add-4ca6-8897-45d0afaa6eb4" />

Fig. 53 (iiI) contd.

<img width="1855" height="977" alt="image" src="https://github.com/user-attachments/assets/b118984e-8632-4df4-80b7-8fa3505d8fd3" />

Fig. 53 (iv) contd.

<img width="1464" height="872" alt="image" src="https://github.com/user-attachments/assets/f8d371e4-e8f1-47c0-afe7-bd909572024c" />

Fig. 54 Proc to set netlist directory

<img width="1463" height="868" alt="image" src="https://github.com/user-attachments/assets/47ef20df-a3c8-4077-a471-6e756e447e88" />

Fig. 55 Proc to set Standard Output

<img width="1465" height="867" alt="image" src="https://github.com/user-attachments/assets/4195785d-4a1f-496b-bbdc-93782eefa63b" />

Fig. 56 Proc to set number of threads for Opentimer to access while running
<img width="872" height="654" alt="image" src="https://github.com/user-attachments/assets/a991290f-36a3-419e-aa1f-cee4a89d9e75" />
Fig. 57 Sample TCl script to illustrate use of a proc
<img width="871" height="647" alt="image" src="https://github.com/user-attachments/assets/3e275d06-e9fa-41db-8c5a-ec97e9618c4b" />
Fig. 58 Execution of the test script

**12. Netlist and SDC processing for Opentimer**
<img width="1794" height="870" alt="image" src="https://github.com/user-attachments/assets/9e1c33ee-1e8a-4cb7-9a73-4955ef7a20a8" />
Fig. 59 (i) Verilog file generated after synthesis. Contains * and \ which are unwanted - needs to be removed before its fed into Opentimer
<img width="1792" height="870" alt="image" src="https://github.com/user-attachments/assets/262eee84-75d7-45d2-83bf-facf73f269c8" />
Fig. 59 (ii) Unwanted "" encountered
<img width="1852" height="982" alt="image" src="https://github.com/user-attachments/assets/24808afa-e15c-4e85-a477-fc4275ddff34" />
Fig. 60 Script to remove unwanted lines and characters
<img width="1854" height="982" alt="image" src="https://github.com/user-attachments/assets/eba777fd-be86-4ccb-a1b4-096ab8549741" />

Fig. 61 Successful netlist preparation for STA
<img width="735" height="489" alt="image" src="https://github.com/user-attachments/assets/3cb33cbe-b178-4a69-959c-32bd42e8865f" />
Fig. 62 Script to use procs to process constraints in the SDC file and prepare the .spef and .conf file for Opentimer
<img width="1707" height="706" alt="image" src="https://github.com/user-attachments/assets/8e2ebe28-243e-4ef6-8f68-0811168a2e66" />

Fig. 63 Successful preparation of files required

**13. Static Timing Analysis (STA) and Quality of Results (QOR)**

<img width="1704" height="705" alt="image" src="https://github.com/user-attachments/assets/4c0d417f-e219-4e1c-902c-c2fa3c162550" />

Fig. 64 Script to invoke Opentimer and dump log and results

<img width="1705" height="705" alt="image" src="https://github.com/user-attachments/assets/9370c5ff-dd9a-4570-a123-951f70a97dba" />

Fig. 65 Result file generated by Opentimer

<img width="1705" height="705" alt="image" src="https://github.com/user-attachments/assets/0389b63c-cefc-4b65-a08f-4b52b6ff497f" />

Fig. 66 (i) Script to extract parameters from results file

<img width="1854" height="979" alt="image" src="https://github.com/user-attachments/assets/83eca8d1-fb1d-4ed5-8024-07c09b61357a" />

Fig. 66 (ii) contd and script to format results while displaying

<img width="1854" height="975" alt="image" src="https://github.com/user-attachments/assets/09a5f966-5850-4684-be1b-677ea37a6aea" />

Fig. 67 Final Result





**14. Conclusion**

A TCL toolbox was created to which the design details were fed. The design details were extracted. The constraints given were processed to suit the requirements of the yosys tool. Synthesis was carried out using yosys. The synthesised netlist was modified to suit the needs of Opentimer. The SDC constraints were processed using procs to suit the Opentimer model. Static Timing Analysis (STA) was performed and the results were extracted and formatted and finnaly displayed to the user.

**Acknowledgement**

The above work was carried out as a part of the 5-day workshop on TCL Programming organised by VLSI System Design. I am greatly indebted to Kunal Ghosh (course instructor), Geetima Kachari (TA) and the entire VSD Team for this great learning experience and immense guidance provided throughout the workshop.


















            













