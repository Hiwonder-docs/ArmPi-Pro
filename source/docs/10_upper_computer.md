# 5. PC Software Action Editing Course

## 5.1 Start PC Software

### 5.1.1 Start with Desktop Icon

* **Start with Desktop Icon** 

Double-click the <img style="width:50px" src="../_static/media/chapter_10/section_1/image2.png"  /> on desktop. 

* **Start with Command Line** 

(1) Power on the robot and use VNC Viewer to connect to the remote desktop.

<img class="common_img" src="../_static/media/chapter_10/section_1/image3.png"  />

(2) click <img src="../_static/media/chapter_10/section_1/image4.png" style="width:0.32292in;height:0.30208in" /> in the upper left corner of the system desktop to open the "**Terminator**".

(3) Enter the following command to start the PC software program. 

```bash
python3 software/armpi_pro_control/main.py
```

### 5.1.2 Software Interface Distribution

The PC software interface is as follow:

<img class="common_img" src="../_static/media/chapter_10/section_1/image7.png"  alt="loading" />

The **"Normal Mode"** interface is divided into several areas, as the figure shown below:

<img class="common_img" src="../_static/media/chapter_10/section_1/image8.png"  alt="loading" />

(1) Servo Control Area 

The Servo Control Area displays the corresponding servo icons of robotic arm. You can control the servos by dragging slider bar.

| Icon | Instruction |
|:--:|:--:|
| <img src="../_static/media/chapter_10/section_1/image9.png" style="width:1.52639in;height:0.22292in" alt="loading" /> | The ID number of servo. Here is ID1. |
| <img src="../_static/media/chapter_10/section_1/image10.png" style="width:1.40347in;height:0.76736in" alt="loading" /> | Adjust servo position. The minimum value is 0 and the maximum value is 1000. |
| <img src="../_static/media/chapter_10/section_1/image11.png" style="width:1.44792in;height:0.28125in" alt="loading" /> | Adjust servo deviation. The minimum value is -125 and the maximum value is 125. |

(2) Action Data List

The Action Data List displays the running time and servo value of each action of current action group.

<img class="common_img" src="../_static/media/chapter_10/section_1/image12.png"  alt="loading" />

| **Icon** | Instruction |
|:--:|:--:|
| <img src="../_static/media/chapter_10/section_1/image13.png" style="width:in;height:in" alt="loading" /> | Action group number. |
| <img src="../_static/media/chapter_10/section_1/image14.png" style="width:in;height:in" alt="loading" /> | The running time of action. |
| <img src="../_static/media/chapter_10/section_1/image15.png" style="width:in;height:in" alt="loading" /> | Modify the value corresponding to the ID number. Double-click <img src="../_static/media/chapter_10/section_1/image16.png" style="width:0.80208in;height:0.16667in" alt="loading" />to modify directly. |

(3) Action Setting Area

<table class="docutils-nobg" border="1">
<colgroup>
<col width="30%">
</colgroup>
<tbody>
<tr>
<td style="text-align: center;"><strong>Icon</strong></td>
<td style="text-align: center;"><strong>Instruction</strong></td>
</tr>
<tr>
<td style="text-align: center;"><img src="../_static/media/chapter_10/section_1/image17.png"  alt="loading" /></td>
<td style="text-align: center;">The time for running single action. Click<img src="../_static/media/chapter_10/section_1/image18.png" style="width:0.40139in;height:0.27153in" alt="loading" />to modify.</td>
</tr>
<tr>
<td style="text-align: center;"><img src="../_static/media/chapter_10/section_1/image19.png" alt="loading" /></td>
<td style="text-align: center;">The total time for running the action group.</td>
</tr>
<tr>
<td style="text-align: center;"><img src="../_static/media/chapter_10/section_1/image20.png" style="width:1.22917in;height:0.47917in" /></td>
<td style="text-align: center;">Click this button to loose robot's joint and then the joint can be twisted.</td>
</tr>
<tr>
<td style="text-align: center;"><img src="../_static/media/chapter_10/section_1/image21.png" style="width:1.19792in;height:0.4375in" /></td>
<td style="text-align: center;">Read the angle information after twisting the robotic arm. (This button need to use with "**Motor power off**".)</td>
</tr>
<tr>
<td style="text-align: center;"><img src="../_static/media/chapter_10/section_1/image22.png" style="width:1.13542in;height:0.45833in" /></td>
<td style="text-align: center;">Add the current servo values in servo control area to the last line of action data list.</td>
</tr>
<tr>
<td style="text-align: center;"><img src="../_static/media/chapter_10/section_1/image23.png" style="width:1.19792in;height:0.48958in" /></td>
<td style="text-align: center;"><p>Delete action: delete the selected action in action data list.
Delete all: delete all the actions in action data list</p></td>
</tr>
<tr>
<td style="text-align: center;"><img src="../_static/media/chapter_10/section_1/image24.png" style="width:1.125in;height:0.44792in" /></td>
<td style="text-align: center;"><p>Replace the selected action in action data list.</p>
<p>(The selected action will be replaced by the current servo value in servo control area and the running time will be replaced by the time set in "**Action Time**".)</p></td>
</tr>
<tr>
<td style="text-align: center;"><img src="../_static/media/chapter_10/section_1/image25.png" style="width:1.11458in;height:0.4375in" /></td>
<td style="text-align: center;"><p>Insert a action before the selected action.</p></td>
</tr>
<tr>
<td style="text-align: center;"><img src="../_static/media/chapter_10/section_1/image26.png" style="width:1.13542in;height:0.4375in" /></td>
<td style="text-align: center;">Exchange the selected action with the previous one.</td>
</tr>
<tr>
<td style="text-align: center;"><img src="../_static/media/chapter_10/section_1/image27.png" style="width:1.10417in;height:0.44792in" /></td>
<td style="text-align: center;">Exchange the selected action with the next one.</td>
</tr>
<tr>
<td style="text-align: center;"><img src="../_static/media/chapter_10/section_1/image28.png" style="width:0.75in;height:1.38542in" /></td>
<td style="text-align: center;"><p>Click to run action group in action data list once.</p>
<p>(If click "**loop**", robot will run the action group repeatedly)</p></td>
</tr>
<tr>
<td style="text-align: center;"><img src="../_static/media/chapter_10/section_1/image29.png" style="width:1.29167in;height:0.54167in" /></td>
<td style="text-align: center;"><p>Click to open the selected action group and then display in action data list.</p>
<p>(The path to action group file："**/home/ubuntu/software/armpi_pro_control/ActionGroups**")</p></td>
</tr>
<tr>
<td style="text-align: center;"><img src="../_static/media/chapter_10/section_1/image30.png" style="width:1.30208in;height:0.54167in" /></td>
<td style="text-align: center;"><p>Save the current action in action action list to the specific location.</p>
<p>(/home/ubuntu/software/armpi_pro_control/ActionGroups)</p></td>
</tr>
<tr>
<td style="text-align: center;"><img src="../_static/media/chapter_10/section_1/image31.png" style="width:1.29167in;height:0.55208in" /></td>
<td style="text-align: center;">After opening an action group, click this button and then open another action group file to integrate two action groups into a new one.</td>
</tr>
<tr>
<td style="text-align: center;"><img src="../_static/media/chapter_10/section_1/image32.png" style="width:1.83333in;height:0.4375in" /></td>
<td style="text-align: center;">Display the saved action group in PC software.</td>
</tr>
<tr>
<td style="text-align: center;"><img src="../_static/media/chapter_10/section_1/image33.png" style="width:0.78125in;height:0.52083in" /></td>
<td style="text-align: center;">Click to refresh.</td>
</tr>
<tr>
<td style="text-align: center;"><img src="../_static/media/chapter_10/section_1/image34.png" style="width:1.38542in;height:0.48958in" /></td>
<td style="text-align: center;">Delete the current action group file</td>
</tr>
<tr>
<td style="text-align: center;"><img src="../_static/media/chapter_10/section_1/image35.png" style="width:1.13542in;height:0.5in" /></td>
<td style="text-align: center;">(Caution) Delete all action group files.</td>
</tr>
<tr>
<td style="text-align: center;"><img src="../_static/media/chapter_10/section_1/image36.png" style="width:1.40625in;height:0.47917in" /></td>
<td style="text-align: center;">Perform the selected action group once.</td>
</tr>
<tr>
<td style="text-align: center;"><img src="../_static/media/chapter_10/section_1/image37.png" style="width:1.16667in;height:0.51042in" /></td>
<td style="text-align: center;">Stop the running action group.</td>
</tr>
<tr>
<td style="text-align: center;"><img src="../_static/media/chapter_10/section_1/image38.png" style="width:1.05208in;height:0.4375in" /></td>
<td style="text-align: center;">Exit the current PC software interface.</td>
</tr>
</tbody>
</table>

(4) Deviation Settings Area (For reference only)

| Icon | Instruction |
|:--:|:--:|
| <img src="../_static/media/chapter_10/section_1/image39.png" style="width:1.59375in;height:0.59375in" /> | Click to read the saved deviation automatically. |
| <img src="../_static/media/chapter_10/section_1/image40.png" style="width:1.64583in;height:0.60417in" /> | Click to download the deviation that has been adjusted by PC software to robot. |
| <img src="../_static/media/chapter_10/section_1/image41.png" style="width:1.64583in;height:0.55208in" /> | Click to restore all servos in servo control area to the position corresponding to the value of 500. |

## 5.2 Call Action Group

### 5.2.1 Realization

ArmPi Pro has built-in action groups which are saved in `/home/ubuntu/software/armpi_pro_control/ActionGroups`. We can check and call the built-in action group by PC software or command line. 
The action file must be saved in `/home/ubuntu/software/armpi_pro_control/ActionGroups` for calling.

<img class="common_img" src="../_static/media/chapter_10/section_2/image2.png"  />

### 5.2.2 Call Action Group

* **PC sotfware** 

(1) Double click <img src="../_static/media/chapter_10/section_2/image3.jpeg" style="width:n;height:in" alt="loading" /> to enter PC software, as the figure shown below:

<img class="common_img" src="../_static/media/chapter_10/section_2/image4.png"  alt="loading" />

(2) Then click **"Open action file"**.

<img class="common_img" src="../_static/media/chapter_10/section_2/image5.png"  alt="loading" />

(3) Then select the action group to be executed and click "**Open**".

<img class="common_img" src="../_static/media/chapter_10/section_2/image6.png"  />

(4) Now, the running time and servo value of each action will be displayed in action data list.

<img class="common_img" src="../_static/media/chapter_10/section_2/image7.png"  alt="loading" />

(5) Click "**Run**" to run this action group. If want to repeatedly run the action group, you can click "**loop**".

<img class="common_img" src="../_static/media/chapter_10/section_2/image8.png"  alt="loading"/>

* **Command line** 

(1) Power on the robot and use VNC Viewer to connect to the remote desktop.

<img class="common_img" src="../_static/media/chapter_10/section_2/image9.png"  />

(2) Click <img src="../_static/media/chapter_10/section_2/image10.png" style="width:0.32292in;height:0.30208in" /> in the upper left corner of the system desktop to open the "Terminator".

<img class="common_img" src="../_static/media/chapter_10/section_2/image11.png" style="width:100%;" />

(3) Enter the following command in the opened terminal interface to switch to the directory of PC software. 

```bash
cd software/armpi_pro_control
```

(4) Enter the command "**ls**" to check all files under this directory. The action group file is stored in the directory "**ActionGroups**" as shown below:

<img class="common_img" src="../_static/media/chapter_10/section_2/image13.png" style="width:100%;" />

<p id="execute_single_action">

* **Execute single action** 

If want perform single action, you need to modify the program file for calling action.

(1) Enter the following command and press "**Enter**" to open the program file for calling action via vim editor.

```bash
vim control_demo.py
```

<img class="common_img" src="../_static/media/chapter_10/section_2/image15.png"  />

(2) Then press "**i**" to switch to the program editing mode.

<img class="common_img" src="../_static/media/chapter_10/section_2/image16.png" style="width:100%;" />

(3) Next, we can find that the program will perform "**wave_pro**" action by default.

<img class="common_img" src="../_static/media/chapter_10/section_2/image17.png" style="width:100%;" />

(4) Take changing the default action group to **"grab-forward_pro"** as example. Replace **"wave_pro"** in parenthesis with **"grab-forward_pro"**.

<img class="common_img" src="../_static/media/chapter_10/section_2/image18.png" style="width:100%;" />

:::{Note}
The action name must be consistent with the file name, otherwise, it will be failed to call!
:::

(5) Press "**Esc**" , and enter "**:wq**". Then press "**Enter**" to save and exit.

<img class="common_img" src="../_static/media/chapter_10/section_2/image19.png" style="width:100%;" />

(6) Enter the following command and press "**Enter**" to execute "**grab_forward_Pro**" action once.

:::{Note}
 If no action action file is saved in the path, LX terminal will prompt "**no action group file is found**". Therefore, please make sure the action group to be called is save in the correct path.
:::

* **Call several action groups** 

If want to call several action groups, please refer to the following operation steps. This section will call "**wave_Pro**" and "**grab-forward_Pro**" actions as example:

(1) According to the operation steps in"[**5.2.2 Call Action Group -> Execute Single Action**](#execute_single_action)", enter the following command  to enter program file and editing mode.

```bash
vim control_demo.py
```

<img class="common_img" src="../_static/media/chapter_10/section_2/image21.png" style="width:100%;" />

(2) Then copy `controller.runAction('')` function. Please note that the parameters in function should be consistent with the action group name, otherwise, the action can not be performed .

<img class="common_img" src="../_static/media/chapter_10/section_2/image22.png" style="width:100%;" />

(3) There is another tip for you. For example, after performing two actions above, it there are other action files to be performed, you can select the function in 27 line, press "**Y**" twice and then press "**P**" to copy the function. (Before this step, you need to press "**Esc**" to exit the editing mode.)

<img class="common_img" src="../_static/media/chapter_10/section_2/image23.png" style="width:100%;" />

(4) Now, modify the parameter in function with the name of action group to be performed. Then, save and exit. Finally, enter command.

```bash
python3 control_demo.py
```

## 5.3 Action Programming

The values set in this lesson is just for reference, you can adjust them according to the actual situation.

### 5.3.1 Program Goal

Action editing refers to adjusting the angles of corresponding servos based on the target action to achieve the action, and multiple actions are combined into the action group.
Create an action group to allow robotic arm to transport the block to the left side.

### 5.3.2 How to realize it?

* **Action Design** 

(1) Double-click <img src="../_static/media/chapter_10/section_3/image1.jpeg" style="width:0.57917in;height:0.73333in" alt="loading" /> to open PC software (normal mode).

<img class="common_img" src="../_static/media/chapter_10/section_3/image2.png"  alt="loading" />

(2) Click **"Open action file"** and select **"start"** action group file in **"/home/ubuntu/software/armpi_pro_control/ActionGroups"**. Then click "**Open**" to import this action group into action date list to set an initial posture for ArmPi Pro.

<img class="common_img" src="../_static/media/chapter_10/section_3/image3.png"  />

<img class="common_img" src="../_static/media/chapter_10/section_3/image1.png"  />

(3) Click  <img src="../_static/media/chapter_10/section_3/image0.png"  /> in front of No.1 action to update the servo angel information in servo control area. 

<img class="common_img" src="../_static/media/chapter_10/section_3/image4.jpeg"  alt="loading" />

(4) Drag the bar slider of No.5 servo to allow robotic arm to move down to the block.

<img class="common_img" src="../_static/media/chapter_10/section_3/image5.png"  alt="loading"  />

(5) Set the running time as 800ms and click "**Add action**" to get the second action.

<img class="common_img" src="../_static/media/chapter_10/section_3/image6.png"  alt="loading" />

(6) To make action group smoother, add a transition action after setting an action and set the running time as 100ms. Then click "**Add action**" to get No.3 action.

<img class="common_img" src="../_static/media/chapter_10/section_3/image7.png"  alt="loading" />

(7) Then drag the sliders of No.1 and No.5 servos to allow the gripper open and move to the block.

<img class="common_img" src="../_static/media/chapter_10/section_3/image8.png"  alt="loading"  />

(8) Set the running time as 500ms and click "**Add action**" to get No.4 action.

<img class="common_img" src="../_static/media/chapter_10/section_3/image9.png"  alt="loading" />

(9) Add a transition action. Set the running time as 200ms and click "**Add action**" to get No.5 action.

<img class="common_img" src="../_static/media/chapter_10/section_3/image10.png"  alt="loading" />

(10) Then drag the slider of No.5 servo to point the gripper at the block.

<img class="common_img" src="../_static/media/chapter_10/section_3/image11.png"  alt="loading" />

(11) The running time is set as 600ms and click "**Add action**" to get No.6 action.

<img class="common_img" src="../_static/media/chapter_10/section_3/image12.png"  alt="loading" />

(12) Then add a transition action. Set the running time as 200ms and click "**Add action**" to get No.7 action.

<img class="common_img" src="../_static/media/chapter_10/section_3/image13.png"  alt="loading" />

(13) Drag the slider under ID1 servo to grip the block.

<img class="common_img" src="../_static/media/chapter_10/section_3/image14.png"  alt="loading"  />

(14) The running time is set as 600ms and then click "**Add action**" to get No.8 action.

<img class="common_img" src="../_static/media/chapter_10/section_3/image15.png"  alt="loading" />

(15) Then adjust the value of No.4 and No.5 servos to raise the robotic arm. 

<img class="common_img" src="../_static/media/chapter_10/section_3/image16.png"  alt="loading"  />

(16) The running time is set as 700ms and then click "**Add action**" to get No.9 action.

<img class="common_img" src="../_static/media/chapter_10/section_3/image17.png"  alt="loading" />

(17) Add a transition action and set the running time as 200ms.

<img class="common_img" src="../_static/media/chapter_10/section_3/image18.png"  alt="loading" />

(18) Then adjust the value of No.6 servo to allow the robotic arm to move the block to the left side.

<img class="common_img" src="../_static/media/chapter_10/section_3/image19.png"  alt="loading"  />

(19) The running time is set as 800ms and then click "**Add action**" to get No.11 action.

<img class="common_img" src="../_static/media/chapter_10/section_3/image20.png"  alt="loading" />

(20) Add a transition action and set the running time as 200ms.

<img class="common_img" src="../_static/media/chapter_10/section_3/image21.png"  alt="loading" />

(21) After moving the block to the specific position, put it down. This step need to adjust the value of No.3, No.4 and No.5 servos.

<img class="common_img" src="../_static/media/chapter_10/section_3/image22.png"  alt="loading"  />

(22) Then set the running time as 600ms and click "**Add action**" to get No.13 action.

<img class="common_img" src="../_static/media/chapter_10/section_3/image23.png"  alt="loading" />

(23) Add an transition action and its running time is set to 100ms.

<img class="common_img" src="../_static/media/chapter_10/section_3/image24.png"  alt="loading" />

(24) The drag the slider of ID1 servo to loose the block.

<img class="common_img" src="../_static/media/chapter_10/section_3/image25.png"  alt="loading"  />

(25) After completing this action, let robotic arm back to the initial posture. Adjust the value of ID1, ID3, ID4 and ID5 servos to close the gripper and lift the robotic arm.

<img class="common_img" src="../_static/media/chapter_10/section_3/image27.png"  alt="loading"  />

(26) Set the time to 00ms, and then click "**Add action**" to get No.16 action.

<img class="common_img" src="../_static/media/chapter_10/section_3/image28.png"  alt="loading" />

(27) Add an transition action and set its running time to 100ms.

<img class="common_img" src="../_static/media/chapter_10/section_3/image29.png"  alt="loading" />

(28) Finally, return the robotic arm to initial posture. No need to adjust the servo value. Find No.1 action and click <img src="../_static/media/chapter_10/section_3/image30.jpeg" style="width:0.59028in;height:0.37917in" alt="loading" />。

<img class="common_img" src="../_static/media/chapter_10/section_3/image31.png"  alt="loading" />

In meantime, the servo control area at left side will update the value of No.1 action, as the figure shown below:

<img class="common_img" src="../_static/media/chapter_10/section_3/image32.png"  alt="loading"  />

(29) Finally, set the running time as 800 and click "**Add action**" to get No.18 action.

<img class="common_img" src="../_static/media/chapter_10/section_3/image33.png"  alt="loading" />

OK, the entire of this action has been programmed completely, as the figure shown below.

<img class="common_img" src="../_static/media/chapter_10/section_3/image34.png"  alt="loading" />

(30) Next, let's look at the performance. Select No.1 action and click "**Run**". If want to execute this action cyclically, you can check "**Loop**".

<img class="common_img" src="../_static/media/chapter_10/section_3/image35.png"  alt="loading" />

**3.2.2 Save Action**

:::{Note}
The action name can not contain space key. It is recommended to use "**\_**" instead of space key.
:::

For facilitate debugging sometime, save the completed action group. Click "**Save action file**" and save to the path: **/home/ubuntu/software/armpi_fpv_control/ActionGroups**

Here name the action group as  `transfer_to_left`  and click  `Save` to save action.

<img class="common_img" src="../_static/media/chapter_10/section_3/image36.png"  />

## 5.4 Integrate Action File

### 5.4.1 Program Goal

This lesson will teach you how to integrate two action groups into a new action group.

### 5.4.2 Operation Steps

(1) Power on the robot and use VNC Viewer to connect to the remote desktop.

<img class="common_img" src="../_static/media/chapter_10/section_4/image1.png"  alt="loading" />

(2) Click "**Integrate Action File**" in action setting area and select the following path:

<img class="common_img" src="../_static/media/chapter_10/section_4/image2.png"  />

<img class="common_img" src="../_static/media/chapter_10/section_4/image0.png"  />

(3) In the opened interface, select "**grab-forward_pro.d6a**" and double-click to open it.

<img class="common_img" src="../_static/media/chapter_10/section_4/image3.jpeg"  alt="loading" />

(4) At this time, we can see that the action group parameters are shown in action data list. (The image is just a part of screenshot)

<img class="common_img" src="../_static/media/chapter_10/section_4/image4.png"  alt="loading" />

(5) Then click "Integ**rate action file**" again and double click to open "**wave_pro.d6a**". We can find that action group file has been integrated.

<img class="common_img" src="../_static/media/chapter_10/section_4/image5.png"  alt="loading" />

(6) Select No.1 action and click "**Run**" to run the integrated action group once.

<img class="common_img" src="../_static/media/chapter_10/section_4/image6.png"  alt="loading" />

(7) Click "**Save action file**" to save this new action group. 

<img class="common_img" src="../_static/media/chapter_10/section_4/image7.png"  alt="loading"  />

(8) Name the action group. ("**wave_and_grab_forwad**" is a example name)

:::{Note}

The name must be English and not space is included. It is recommended to replace space with  underline.

:::

<img class="common_img" src="../_static/media/chapter_10/section_4/image8.png"  />

## 5.5  Import and Export Action File

ArmPi Pro has built-in action group before delivery, and its action group file is stored in the path of Docker container `/home/ubuntu/software/armpi_pro_ control/ActionGroups`. The action group file in the container can be imported and exported in the form of terminal command line.

<img class="common_img" src="../_static/media/chapter_10/section_5/image1.png"  />

### 5.5.1 Getting Ready

Power on the robot and use VNC Viewer to connect to the remote desktop.

### 5.5.2 Export Action

Take exporting and importing "**transfer_to_left**" action file as example.

(1) Click <img src="../_static/media/chapter_10/section_5/image2.png" style="width:0.32292in;height:0.30208in" /> in the upper left corner of the system desktop to open the "**Terminator**".

<img class="common_img" src="../_static/media/chapter_10/section_5/image3.png"  />

(2) Enter the following command in the opened terminal interface to copy it to the "/home/ubuntu/share/tmp/".

```bash
cp /home/ubuntu/software/armpi_pro_control/ActionGroups/transfer_to_left.d6a /home/ubuntu/share/tmp/
```

(3) Click <img src="../_static/media/chapter_10/section_5/image5.png" style="width:0.42708in;height:0.36458in" /> in the upper left corner of the desktop to find the "**transfer_to_left**" file under this path.

<img class="common_img" src="../_static/media/chapter_10/section_5/image6.png"  />

### 5.5.3 Import File

The process for importing and exporting actions is the same: import the action group file in the corresponding path. 

(1) Import the "**transfer_to_left**" action group file into the shared folder "**/share/tmp/**" between the Docker container and the Raspberry Pi system.

<img class="common_img" src="../_static/media/chapter_10/section_5/image6.png"  />

(2) Click <img src="../_static/media/chapter_10/section_5/image2.png" style="width:0.32292in;height:0.30208in" /> in the upper left corner of the system desktop to open the "**Terminator**".

<img class="common_img" src="../_static/media/chapter_10/section_5/image3.png"  />

(3) Enter the following command in the opened terminal interface 

```bash
cp /home/ubuntu/share/tmp/transfer_to_left.d6a /home/ubuntu/software/armpi_pro_control/ActionGroups/
```

to copy it to the `/home/ubuntu/software/armpi_pro_control/ActionGroups/`.

(4) Now, double-click <img src="../_static/media/chapter_10/section_5/image8.jpeg" style="width:0.51181in;height:0.64792in" alt="loading" /> to enter PC software (Normal mode).

<img class="common_img" src="../_static/media/chapter_10/section_5/image9.png"  alt="loading" />

(5) Click "**Open action file**" and find the imported action file according to the following path.

<img class="common_img" src="../_static/media/chapter_10/section_5/image10.png"  />

<img class="common_img" src="../_static/media/chapter_10/section_5/image0.png"  />

Or click the drop down of action group to select the imported action file.

<img class="common_img" src="../_static/media/chapter_10/section_5/image11.png"  alt="loading"  />

<img class="common_img" src="../_static/media/chapter_10/section_5/image1.0.png"  alt="loading"  />

(6) Click "**Run**" to perform the action group.

<img class="common_img" src="../_static/media/chapter_10/section_5/image12.png" style="" alt="loading" />
